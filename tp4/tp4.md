# I. DHCP Client

### 🌞 Déterminer

```
PS C:\WINDOWS\system32> ipconfig /all

Carte réseau sans fil Wi-Fi :

   Bail obtenu. . . . . . . . . . . . . . : vendredi 8 decembre 2023 19:03:26
   Bail expirant. . . . . . . . . . . . . : samedi 9 
   Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
```
### 🌞 Capturer un échange DHCP

```
PS C:\WINDOWS\system32> ipconfig /release

Configuration IP de Windows

Aucune opération ne peut être effectuée sur Ethernet 2 lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion au réseau local* 1 lorsque
son média est déconnecté.

Carte inconnue Connexion au réseau local :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte Ethernet Ethernet 2 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte Ethernet Ethernet 3 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::2c62:a90d:4377:c6%10
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.56.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet Ethernet 4 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::1c1:6b45:9b7e:293a%9
   Adresse IPv4. . . . . . . . . . . . . .: 10.3.1.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet Ethernet 5 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::3754:39e6:1cd9:dc52%17
   Adresse IPv4. . . . . . . . . . . . . .: 10.3.2.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :

Carte réseau sans fil Connexion au réseau local* 1 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 2 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::bea3:6d81:698c:40d5%4
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet VMware Network Adapter VMnet1 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::5e93:4948:226:601e%22
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet VMware Network Adapter VMnet8 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::b0e0:21c:e45e:6219%24
   Passerelle par défaut. . . . . . . . . :
```

### 🌞 Analyser la capture Wireshark

```
c'est la 2eme tram qui contient tous les infos proposés au client (DHCP offer)
```

### 🦈 tp4_dhcp_client.pcapng

## II. Serveur DHCP

### 🌞 Preuve de mise en place

```

[matis@dhcp ~]$ ping youtube.com
PING youtube.com (142.250.179.110) 56(84) bytes of data.
64 bytes from reflectededge.reflected.net (142.250.179.110): icmp_seq=1 ttl=53 time=15.4 ms
64 bytes from reflectededge.reflected.net (142.250.179.110): icmp_seq=2 ttl=53 time=14.7 ms
64 bytes from reflectededge.reflected.net (142.250.179.110): icmp_seq=3 ttl=53 time=25.1 ms
^C
--- youtube.com ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2004ms
rtt min/avg/max/mdev = 14.719/18.407/25.135/4.764 ms
```

```

[matis@node1 ~]$ ping youtube.com
PING youtube.com (142.250.179.110) 56(84) bytes of data.
64 bytes from 142.250.179.110 (142.250.179.110): icmp_seq=1 ttl=55 time=14.5 ms
64 bytes from 142.250.179.110 (142.250.179.110): icmp_seq=2 ttl=55 time=26.5 ms
64 bytes from 142.250.179.110 (142.250.179.110): icmp_seq=3 ttl=55 time=28.2 ms
^C
--- youtube.com ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2003ms
rtt min/avg/max/mdev = 14.465/23.051/28.193/6.110 ms
```

```
[matis@node2 ~]$ traceroute 8.8.8.8
traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 60 byte packets
 1  _gateway (10.4.1.254)  0.591 ms  0.597 ms  0.546 ms
 2  10.0.3.2 (10.0.3.2)  30.577 ms  30.570 ms  30.505 ms
```

### 🌞 Serveur DHCP


installation du logiciel
```
[matis@dhcp ~]$ dnf -y install dhcp-server
```

### 🌞 Rendu

```
[matis@dhcp ~]$ sudo nano /etc/dhcp/dhcpd.conf
[matis@dhcp ~]$ sudo cat /etc/dhcp/dhcpd.conf

option domain-name     "tp4.dhcp";
authoritative;
subnet 10.4.1.0 netmask 255.255.255.0 {
    range dynamic-bootp 10.4.1.137 10.4.1.237;
    option broadcast-address 10.4.1.255;
}
```

```
[matis@dhcp ~]$ sudo systemctl enable --now dhcpd
Created symlink /etc/systemd/system/multi-user.target.wants/dhcpd.service → /usr/lib/systemd/system/dhcpd.service.
[matis@dhcp ~]$ sudo firewall-cmd --add-service=dhcp
success
[matis@dhcp ~]$ sudo firewall-cmd --runtime-to-permanent
success
```

```
[matis@dhcp ~]$ sudo systemctl status dhcpd
dhcpd.service - DHCPv4 Server Daemon
   Loaded: loaded (/usr/lib/systemd/system/dhcpd).service; enabled; preset>
   Active: active (running) since Fri 2023-10-28 15:29:01 CEST; 4min 48s >
```

### 🌞 Test !

```
[matis@dhcp ~]$ sudo cat /etc/sysconfig/network-scripts/ifcfg-enp0s3
DEVICE=enp0s3

BOOTPROTO=dhcp
ONBOOT=yes
```

### 🌞 Prouvez que

node1 a bien récupéré une IP dynamiquement
```
[matis@localhost ~]$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:de:36:da brd ff:ff:ff:ff:ff:ff
    inet 10.4.1.137/24 brd 10.4.1.255 scope global dynamic noprefixroute enp0s3
       valid_lft 336sec preferred_lft 336sec
    inet6 fe80::a00:27ff:fede:36da/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
```
```
[matis@localhost ~]$ nmcli con show enp0s3
```

node1 a enregistré un bail DHCP

déterminer la date exacte de création du bail
 samedi 28 octobre 2023 16:19:21 GMT+02:00 DST

déterminer la date exacte d'expiration
 samedi 28 octobre 2023 16:47:12 GMT+02:00 DST

déterminer l'adresse IP du serveur DHCP
dhcp_server_identifier = 10.4.1.253

Vous pouvez ping router.tp4.b1 et node2 grâce à cette nouvelle IP récupérée

```
[matis@localhost ~]$ ping 10.4.1.254
PING 10.4.1.254 (10.4.1.254) 56(84) bytes of data.
64 bytes from 10.4.1.254: icmp_seq=1 ttl=64 time=0.285 ms
64 bytes from 10.4.1.254: icmp_seq=2 ttl=64 time=0.395 ms
^C
--- 10.4.1.254 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1036ms
rtt min/avg/max/mdev = 0.285/0.340/0.395/0.055 ms
[dany@localhost ~]$ ping 10.4.1.12
PING 10.4.1.12 (10.4.1.12) 56(84) bytes of data.
64 bytes from 10.4.1.12: icmp_seq=1 ttl=64 time=0.407 ms
64 bytes from 10.4.1.12: icmp_seq=2 ttl=64 time=0.349 ms
^C
--- 10.4.1.12 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1044ms
rtt min/avg/max/mdev = 0.349/0.378/0.407/0.029 ms
```

### 🌞 Bail DHCP serveur

```
[matis@dhcp ~]$ cat /var/lib/dhcpd/dhcpd.leases
# The format of this file is documented in the dhcpd.leases(5) manual page.
# This lease file was written by isc-dhcp-4.4.2b1

# authoring-byte-order entry is generated, DO NOT DELETE
authoring-byte-order little-endian;

lease 10.4.1.137 {
  starts 0 2023/11/05 18:46:37;
  ends 1 2023/11/06 00:46:37;
  tstp 1 2023/11/06 00:46:37;
  cltt 0 2023/11/05 18:46:37;
  binding state active;
  next binding state free;
  rewind binding state free;
  hardware ethernet 08:00:27:de:36:da;
  uid "\001\010\000'\3366\332";
}
server-duid "\000\001\000\001,\332\237\214\010\000'%\270\250";
```

### 🌞 Nouvelle conf !

```
[matis@dhcp ~]$ sudo nano /etc/dhcp/dhcpd.conf
[matis@dhcp ~]$ sudo cat /etc/dhcp/dhcpd.conf
option domain-name     "tp4.dhcp";
option domain-name-servers     1.1.1.1;
default-lease-time 21600;
max-lease-time 21600;
authoritative;
subnet 10.4.1.0 netmask 255.255.255.0 {
    range dynamic-bootp 10.4.1.137 10.4.1.237;
    option broadcast-address 10.4.1.255;
    option routers 10.4.1.254;
}
[matis@dhcp ~]$ sudo systemctl restart dhcpd
```

### 🌞 Test !

vous avez enregistré l'adresse d'un serveur DNS
```
[matis@localhost ~]$ sudo cat /etc/resolv.conf
# Generated by NetworkManager
search tp4.dhcp
nameserver 1.1.1.1
```
vous avez une nouvelle route par défaut qui a été récupérée dynamiquement

```
[matis@localhost ~]$ ip r s
default via 10.4.1.254 dev enp0s3 proto dhcp src 10.4.1.138 metric 100
```

la durée de votre bail DHCP est bien de 6 heures
```
[matis@dhcp ~]$ cat /var/lib/dhcpd/dhcpd.leases
# The format of this file is documented in the dhcpd.leases(5) manual page.
# This lease file was written by isc-dhcp-4.4.2b1

# authoring-byte-order entry is generated, DO NOT DELETE
authoring-byte-order little-endian;

lease 10.4.1.137 {
  starts 0 2023/12/05 19:41:31;
  ends 1 2023/12/06 01:41:31;  
  tstp 1 2023/12/06 01:41:31;
  cltt 0 2023/12/05 19:41:31;
  binding state active;
  next binding state free;
  rewind binding state free;
  hardware ethernet 08:00:27:de:36:da;
  uid "\001\010\000'\3366\332";
}
server-duid "\000\001\000\001,\332\237\214\010\000'%\270\250";
```

prouvez que vous avez un accès Internet après cet échange DHCP
```
[matis@localhost ~]$ ping 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=110 time=29.3 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=110 time=37.0 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=110 time=31.2 ms
^C
--- 8.8.8.8 ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2004ms
rtt min/avg/max/mdev = 29.268/32.503/37.043/3.305 ms
[matis@localhost ~]$ ping youtube.com
PING youtube.com (172.217.18.206) 56(84) bytes of data.
64 bytes from ham02s14-in-f206.1e100.net (172.217.18.206): icmp_seq=1 ttl=115 time=30.7 ms
64 bytes from par10s38-in-f14.1e100.net (172.217.18.206): icmp_seq=2 ttl=115 time=28.9 ms
64 bytes from par10s38-in-f14.1e100.net (172.217.18.206): icmp_seq=3 ttl=115 time=27.8 ms
^C
--- youtube.com ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2004ms
rtt min/avg/max/mdev = 27.813/29.147/30.742/1.209 ms
```