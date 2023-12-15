# I. Setup IP

### 🌞 Mettez en place une configuration réseau fonctionnelle entre les deux machines

```
10.10.10.9
10.10.10.10
255.255.255.252
10.10.10.252
```
### 🌞 Prouvez que la connexion est fonctionnelle entre les deux machines

```
PS C:\Users\celes> ping 10.10.10.10

Envoi d’une requête 'Ping'  10.10.10.10 avec 32 octets de données :
Réponse de 10.10.10.10 : octets=32 temps=25 ms TTL=128
Réponse de 10.10.10.10 : octets=32 temps=18 ms TTL=128
Réponse de 10.10.10.10 : octets=32 temps=54 ms TTL=128
Réponse de 10.10.10.10 : octets=32 temps=43 ms TTL=128

Statistiques Ping pour 10.10.10.10:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 18, Maximum = 54, Moyenne = 35ms
```

### 🌞 Wireshark it

```
ICMP (1) pour l'envoi et le reçu
```

### 🦈 PCAP qui contient les paquets ICMP qui vous ont permis d'identifier les types ICMP (juste quelques-uns)

```
un.pcapng
```

# II. ARP my bro

### 🌞 Check the ARP table

```
PS C:\Users\celes> arp -a

Interface : 192.168.56.1 --- 0x7
  Adresse Internet      Adresse physique      Type
  192.168.56.255        ff-ff-ff-ff-ff-ff     statique
  224.0.0.22            01-00-5e-00-00-16     statique
  224.0.0.251           01-00-5e-00-00-fb     statique
  224.0.0.252           01-00-5e-00-00-fc     statique
  239.255.255.250       01-00-5e-7f-ff-fa     statique
```

```
PS C:\Users\celes
> arp -a

Interface : 192.168.0.24 --- 0x9
  Adresse Internet      Adresse physique      Type
  192.168.0.254         70-fc-8f-6b-e1-72     dynamique
  192.168.0.255         ff-ff-ff-ff-ff-ff     statique
  224.0.0.22            01-00-5e-00-00-16     statique
  224.0.0.251           01-00-5e-00-00-fb     statique
  224.0.0.252           01-00-5e-00-00-fc     statique
  239.255.255.250       01-00-5e-7f-ff-fa     statique
  255.255.255.255       ff-ff-ff-ff-ff-ff     statique
```

```
Carte réseau sans fil Connexion au réseau local* 1 :

   Adresse physique . . . . . . . . . . . : 4A-E7-DA-A7-C7-2F
```

### 🌞 Manipuler la table ARP

```
PS C:\WINDOWS\system32> netsh interface IP delete arpcache
Ok.
```

```
PS C:\WINDOWS\system32> arp -a

Interface : 10.10.10.9 --- 0x4
  Adresse Internet      Adresse physique      Type
  224.0.0.2             01-00-5e-00-00-02     statique
  224.0.0.22            01-00-5e-00-00-16     statique

Interface : 192.168.56.1 --- 0x9
  Adresse Internet      Adresse physique      Type
  224.0.0.2             01-00-5e-00-00-02     statique
  224.0.0.22            01-00-5e-00-00-16     statique
  230.0.0.1             01-00-5e-00-00-01     statique

Interface : 192.168.32.1 --- 0x14
  Adresse Internet      Adresse physique      Type
  224.0.0.2             01-00-5e-00-00-02     statique
  224.0.0.22            01-00-5e-00-00-16     statique

Interface : 192.168.136.1 --- 0x16
  Adresse Internet      Adresse physique      Type
  224.0.0.2             01-00-5e-00-00-02     statique
  224.0.0.22            01-00-5e-00-00-16     statique
```

### 🌞 Wireshark it

```
source adress : 10.10.10.9
destination adress : 10.10.10.1O
```

### 🦈 PCAP qui contient les DEUX trames ARP

```
deux.pcapng
```

