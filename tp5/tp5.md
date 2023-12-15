# I. First steps

### 🌞 Déterminez, pour ces 5 applications, si c'est du TCP ou de l'UDP

```
netflix.com 
PORT : UDP
IP : 86.64.231.163
port serveur : 443
port local : 59914


youtube.com
PORT : UDP
IP : 142.250.178.138
Port serveur : 443
port local : 63676


crunchyroll.com
PORT : UDP
IP : 91.68.254.14
port serveur : 433
port local : 53036


gmail.com
port : TCP
IP : 216.58.214.165
port serveur : 443
port local : 59957


app.envoituresimone.com
port : TCP
IP : 172.217.20.206
port serveur : 433
port local : 60015
```

### 🌞 Demandez l'avis à votre OS

```
PS C:\WINDOWS\system32> netstat -a -n -b

Connexions actives

  Proto  Adresse locale         Adresse distante       État
  TCP    0.0.0.0:135            0.0.0.0:0              LISTENING
  RpcSs
 [svchost.exe]
  TCP    0.0.0.0:445            0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    0.0.0.0:902            0.0.0.0:0              LISTENING
 [vmware-authd.exe]
  TCP    0.0.0.0:912            0.0.0.0:0              LISTENING
 [vmware-authd.exe]
  TCP    0.0.0.0:5040           0.0.0.0:0              LISTENING
  CDPSvc
 [svchost.exe]
  TCP    0.0.0.0:5357           0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    0.0.0.0:7680           0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    0.0.0.0:49664          0.0.0.0:0              LISTENING
 [lsass.exe]
  TCP    0.0.0.0:49665          0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    0.0.0.0:49666          0.0.0.0:0              LISTENING
  Schedule
 [svchost.exe]
  TCP    0.0.0.0:49667          0.0.0.0:0              LISTENING
  EventLog
 [svchost.exe]
  TCP    0.0.0.0:49668          0.0.0.0:0              LISTENING
  SessionEnv
 [svchost.exe]
  TCP    0.0.0.0:49669          0.0.0.0:0              LISTENING
 [spoolsv.exe]
  TCP    0.0.0.0:49671          0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    0.0.0.0:54297          0.0.0.0:0              LISTENING
 [AsusLinkNear.exe]
  TCP    0.0.0.0:54298          0.0.0.0:0              LISTENING
 [AsusLinkNear.exe]
  TCP    10.3.1.1:139           0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    10.3.2.1:139           0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    10.33.51.143:139       0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    10.33.51.143:51737     20.199.120.151:443     ESTABLISHED
  WpnService
 [svchost.exe]
  TCP    10.33.51.143:59505     20.199.120.182:443     ESTABLISHED
 [OneDrive.exe]
  TCP    10.33.51.143:60367     104.115.83.91:443      LAST_ACK
 [SearchHost.exe]
  TCP    10.33.51.143:60393     13.107.246.42:443      LAST_ACK
 [SearchHost.exe]
  TCP    10.33.51.143:60394     192.229.221.95:80      LAST_ACK
 [SearchHost.exe]
  TCP    10.33.51.143:60742     204.79.197.239:443     TIME_WAIT
  TCP    10.33.51.143:60743     204.79.197.239:443     TIME_WAIT
  TCP    10.33.51.143:60746     20.199.120.182:443     ESTABLISHED
 [msedge.exe]
  TCP    10.33.51.143:60747     20.50.73.9:443         ESTABLISHED
 [OneDrive.exe]
  TCP    10.33.51.143:60748     8.8.4.4:443            TIME_WAIT
  TCP    10.33.51.143:60753     8.8.4.4:443            TIME_WAIT
  TCP    10.33.51.143:60760     8.8.8.8:443            TIME_WAIT
  TCP    10.33.51.143:60761     8.8.4.4:443            TIME_WAIT
  TCP    10.33.51.143:60763     8.8.4.4:443            TIME_WAIT
  TCP    10.33.51.143:60764     8.8.4.4:443            TIME_WAIT
  TCP    10.33.51.143:60766     94.245.104.56:443      TIME_WAIT
  TCP    10.33.51.143:60767     212.82.100.137:443     TIME_WAIT
  TCP    10.33.51.143:60768     216.58.214.165:443     TIME_WAIT
  TCP    10.33.51.143:60769     212.82.100.137:443     TIME_WAIT
  TCP    10.33.51.143:60770     204.79.197.203:443     TIME_WAIT
  TCP    10.33.51.143:60776     18.155.129.121:443     TIME_WAIT
  TCP    10.33.51.143:60778     142.250.179.106:443    TIME_WAIT
  TCP    10.33.51.143:60779     216.58.214.165:443     TIME_WAIT
  TCP    10.33.51.143:60782     216.58.214.174:443     TIME_WAIT
  TCP    10.33.51.143:60783     172.217.18.202:443     TIME_WAIT
  TCP    10.33.51.143:60784     172.217.18.202:443     TIME_WAIT
  TCP    10.33.51.143:60785     216.58.215.45:443      TIME_WAIT
  TCP    10.33.51.143:60786     142.250.178.138:443    TIME_WAIT
  TCP    10.33.51.143:60787     142.250.179.74:443     TIME_WAIT
  TCP    10.33.51.143:60788     142.250.178.138:443    TIME_WAIT
  TCP    10.33.51.143:60789     142.250.179.74:443     TIME_WAIT
  TCP    10.33.51.143:60790     142.250.178.133:443    TIME_WAIT
  TCP    10.33.51.143:60791     142.250.178.133:443    TIME_WAIT
  TCP    10.33.51.143:60792     216.58.214.170:443     TIME_WAIT
  TCP    10.33.51.143:60798     40.90.136.179:443      ESTABLISHED
 [OneDrive.exe]
  TCP    10.33.51.143:60799     20.60.59.33:443        ESTABLISHED
 [OneDrive.exe]
  TCP    10.33.51.143:60800     20.209.90.130:443      ESTABLISHED
 [OneDrive.exe]
  TCP    10.33.51.143:60804     216.58.214.163:443     TIME_WAIT
  TCP    10.33.51.143:60805     204.79.197.239:443     TIME_WAIT
  TCP    10.33.51.143:60806     152.199.19.161:80      ESTABLISHED
  BITS
 [svchost.exe]
  TCP    10.33.51.143:60807     172.217.20.170:443     TIME_WAIT
  TCP    10.33.51.143:60808     216.58.215.45:443      TIME_WAIT
  TCP    10.33.51.143:60809     216.58.215.46:443      TIME_WAIT
  TCP    10.33.51.143:60810     64.233.167.101:443     TIME_WAIT
  TCP    10.33.51.143:60811     172.217.20.163:443     TIME_WAIT
  TCP    10.33.51.143:60812     66.102.1.188:5228      ESTABLISHED
 [chrome.exe]
  TCP    10.33.51.143:60813     8.8.8.8:443            TIME_WAIT
  TCP    10.33.51.143:60814     8.8.4.4:443            TIME_WAIT
  TCP    10.33.51.143:60816     8.8.4.4:443            TIME_WAIT
  TCP    10.33.51.143:60818     8.8.8.8:443            TIME_WAIT
  TCP    10.33.51.143:60820     172.67.68.178:443      TIME_WAIT
  TCP    10.33.51.143:60821     172.217.20.170:443     TIME_WAIT
  TCP    10.33.51.143:60822     172.217.20.202:443     TIME_WAIT
  TCP    10.33.51.143:60824     8.8.8.8:443            TIME_WAIT
  TCP    10.33.51.143:60825     142.250.74.238:443     TIME_WAIT
  TCP    10.33.51.143:60826     172.217.20.200:443     TIME_WAIT
  TCP    10.33.51.143:60827     142.250.179.74:443     TIME_WAIT
  TCP    10.33.51.143:60828     104.18.72.113:443      TIME_WAIT
  TCP    10.33.51.143:60829     163.70.128.23:443      TIME_WAIT
  TCP    10.33.51.143:60830     104.26.2.64:443        TIME_WAIT
  TCP    10.33.51.143:60831     95.217.77.219:443      TIME_WAIT
  TCP    10.33.51.143:60832     104.16.53.111:443      TIME_WAIT
  TCP    10.33.51.143:60833     216.58.215.45:443      TIME_WAIT
  TCP    10.33.51.143:60835     3.162.38.8:443         TIME_WAIT
  TCP    10.33.51.143:60837     3.162.38.245:443       TIME_WAIT
  TCP    10.33.51.143:60838     204.79.197.200:443     TIME_WAIT
  TCP    10.33.51.143:60839     142.250.201.162:443    TIME_WAIT
  TCP    10.33.51.143:60841     216.58.215.51:443      TIME_WAIT
  TCP    10.33.51.143:60842     216.58.214.162:443     TIME_WAIT
  TCP    10.33.51.143:60848     216.239.34.36:443      TIME_WAIT
  TCP    10.33.51.143:60851     20.54.232.160:443      ESTABLISHED
  CDPUserSvc_1e10a891
 [svchost.exe]
  TCP    10.33.51.143:60858     212.82.100.137:443     TIME_WAIT
  TCP    10.33.51.143:60859     87.248.119.251:443     TIME_WAIT
  TCP    10.33.51.143:60860     212.82.100.137:443     TIME_WAIT
  TCP    10.33.51.143:60861     104.18.34.202:443      TIME_WAIT
  TCP    10.33.51.143:60862     104.18.34.202:443      TIME_WAIT
  TCP    10.33.51.143:60863     216.58.214.170:443     TIME_WAIT
  TCP    10.33.51.143:60864     99.86.90.76:443        TIME_WAIT
  TCP    10.33.51.143:60866     99.86.90.76:443        TIME_WAIT
  TCP    10.33.51.143:60868     172.217.20.200:443     TIME_WAIT
  TCP    10.33.51.143:60869     104.18.34.202:443      TIME_WAIT
  TCP    10.33.51.143:60870     44.233.232.118:443     TIME_WAIT
  TCP    10.33.51.143:60871     44.233.232.118:443     TIME_WAIT
  TCP    10.33.51.143:60872     44.233.232.118:443     TIME_WAIT
  TCP    10.33.51.143:60873     44.233.232.118:443     TIME_WAIT
  TCP    10.33.51.143:60874     44.233.232.118:443     TIME_WAIT
  TCP    10.33.51.143:60875     35.159.7.5:443         TIME_WAIT
  TCP    10.33.51.143:60877     172.217.20.170:443     TIME_WAIT
  TCP    10.33.51.143:60878     3.162.38.85:443        TIME_WAIT
  TCP    10.33.51.143:60880     44.233.232.118:443     TIME_WAIT
  TCP    10.33.51.143:60881     172.217.20.163:443     TIME_WAIT
  TCP    10.33.51.143:60882     212.82.100.137:443     TIME_WAIT
  TCP    10.33.51.143:60883     3.162.38.85:443        TIME_WAIT
  TCP    10.33.51.143:60884     216.58.214.86:443      TIME_WAIT
  TCP    10.33.51.143:60885     95.217.77.219:443      TIME_WAIT
  TCP    10.33.51.143:60886     216.58.215.46:443      TIME_WAIT
  TCP    10.33.51.143:60887     172.217.20.198:443     TIME_WAIT
  TCP    10.33.51.143:60890     216.58.205.46:443      TIME_WAIT
  TCP    10.33.51.143:60891     216.58.213.74:443      TIME_WAIT
  TCP    10.33.51.143:60892     216.58.213.70:443      TIME_WAIT
  TCP    10.33.51.143:60893     142.250.75.238:443     TIME_WAIT
  TCP    10.33.51.143:60894     172.217.20.193:443     TIME_WAIT
  TCP    10.33.51.143:60895     172.217.20.195:443     TIME_WAIT
  TCP    10.33.51.143:60896     142.250.179.97:443     TIME_WAIT
  TCP    10.33.51.143:60897     142.250.178.130:443    TIME_WAIT
  TCP    10.33.51.143:60901     216.58.214.165:443     TIME_WAIT
  TCP    10.33.51.143:60902     216.58.214.165:443     TIME_WAIT
  TCP    10.33.51.143:60903     142.250.179.67:443     TIME_WAIT
  TCP    10.33.51.143:60905     142.250.179.110:443    TIME_WAIT
  TCP    10.33.51.143:60907     216.58.214.165:443     TIME_WAIT
  TCP    10.33.51.143:60908     216.58.214.174:443     TIME_WAIT
  TCP    10.33.51.143:60909     172.217.18.202:443     TIME_WAIT
  TCP    10.33.51.143:60910     172.217.18.202:443     TIME_WAIT
  TCP    10.33.51.143:60911     216.58.215.45:443      TIME_WAIT
  TCP    10.33.51.143:60912     142.250.75.234:443     TIME_WAIT
  TCP    10.33.51.143:60914     172.217.20.170:443     TIME_WAIT
  TCP    10.33.51.143:60915     142.250.75.234:443     TIME_WAIT
  TCP    10.33.51.143:60916     172.217.20.170:443     TIME_WAIT
  TCP    10.33.51.143:60917     142.250.178.138:443    TIME_WAIT
  TCP    10.33.51.143:60918     172.217.20.202:443     TIME_WAIT
  TCP    10.33.51.143:60919     142.250.178.133:443    TIME_WAIT
  TCP    10.33.51.143:60920     142.250.178.133:443    TIME_WAIT
  TCP    10.33.51.143:60921     142.250.178.138:443    TIME_WAIT
  TCP    10.33.51.143:60923     51.104.182.209:443     ESTABLISHED
 [RuntimeBroker.exe]
  TCP    10.33.51.143:60924     51.104.182.209:443     ESTABLISHED
 [RuntimeBroker.exe]
  TCP    10.33.51.143:60925     54.155.246.232:443     ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60926     54.77.61.253:443       ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60927     52.30.44.60:443        TIME_WAIT
  TCP    10.33.51.143:60928     192.229.221.95:80      ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60929     54.77.61.253:443       ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60930     62.39.148.63:443       ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60931     62.39.148.63:443       ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60932     62.39.148.63:443       ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60933     52.109.28.50:443       ESTABLISHED
 [StartMenuExperienceHost.exe]
  TCP    10.33.51.143:60934     104.115.83.91:443      ESTABLISHED
 [SearchHost.exe]
  TCP    10.33.51.143:60935     86.64.231.161:443      ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60936     62.39.148.63:443       ESTABLISHED
 [wwahost.exe]
  TCP    10.33.51.143:60938     216.58.214.165:443     ESTABLISHED
 [chrome.exe]
  TCP    10.33.51.143:60939     52.97.135.50:443       SYN_SENT
 [SearchHost.exe]
  TCP    10.33.51.143:60940     13.107.246.254:443     ESTABLISHED
 [SearchHost.exe]
  TCP    10.33.51.143:60941     162.247.243.29:443     ESTABLISHED
 [chrome.exe]
  TCP    10.33.51.143:60942     13.107.246.42:443      ESTABLISHED
 [SearchHost.exe]
  TCP    10.33.51.143:60943     95.100.203.82:443      ESTABLISHED
 [SearchHost.exe]
  TCP    10.33.51.143:60944     204.79.197.222:443     ESTABLISHED
 [SearchHost.exe]
  TCP    192.168.32.1:139       0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    192.168.56.1:139       0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    192.168.136.1:139      0.0.0.0:0              LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    [::]:135               [::]:0                 LISTENING
  RpcSs
 [svchost.exe]
  TCP    [::]:445               [::]:0                 LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    [::]:5357              [::]:0                 LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    [::]:7680              [::]:0                 LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    [::]:49664             [::]:0                 LISTENING
 [lsass.exe]
  TCP    [::]:49665             [::]:0                 LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    [::]:49666             [::]:0                 LISTENING
  Schedule
 [svchost.exe]
  TCP    [::]:49667             [::]:0                 LISTENING
  EventLog
 [svchost.exe]
  TCP    [::]:49668             [::]:0                 LISTENING
  SessionEnv
 [svchost.exe]
  TCP    [::]:49669             [::]:0                 LISTENING
 [spoolsv.exe]
  TCP    [::]:49671             [::]:0                 LISTENING
 Impossible d’obtenir les informations de propriétaire
  TCP    [::1]:42050            [::]:0                 LISTENING
 [Microsoft.SharePoint.exe]
  TCP    [::1]:49670            [::]:0                 LISTENING
 [jhi_service.exe]
  UDP    0.0.0.0:123            *:*
  W32Time
 [svchost.exe]
  UDP    0.0.0.0:500            *:*
  IKEEXT
 [svchost.exe]
  UDP    0.0.0.0:3702           *:*
 [dashost.exe]
  UDP    0.0.0.0:3702           *:*
 [dashost.exe]
  UDP    0.0.0.0:3702           *:*
  FDResPub
 [svchost.exe]
  UDP    0.0.0.0:3702           *:*
  FDResPub
 [svchost.exe]
  UDP    0.0.0.0:4500           *:*
  IKEEXT
 [svchost.exe]
  UDP    0.0.0.0:5050           *:*
  CDPSvc
 [svchost.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
 [chrome.exe]
  UDP    0.0.0.0:5353           *:*
  Dnscache
 [svchost.exe]
  UDP    0.0.0.0:5355           *:*
  Dnscache
 [svchost.exe]
  UDP    0.0.0.0:49195          172.217.20.170:443
 [chrome.exe]
  UDP    0.0.0.0:49664          142.250.179.110:443
 [chrome.exe]
  UDP    0.0.0.0:49665          142.250.75.234:443
 [chrome.exe]
  UDP    0.0.0.0:49692          142.250.179.67:443
 [chrome.exe]
  UDP    0.0.0.0:49897          172.217.20.193:443
 [chrome.exe]
  UDP    0.0.0.0:50869          216.58.214.86:443
 [chrome.exe]
  UDP    0.0.0.0:51482          *:*
 [dashost.exe]
  UDP    0.0.0.0:51669          *:*
  Dnscache
 [svchost.exe]
  UDP    0.0.0.0:51850          172.217.20.162:443
 [chrome.exe]
  UDP    0.0.0.0:52200          172.217.20.194:443
 [chrome.exe]
  UDP    0.0.0.0:52420          172.217.20.202:443
 [chrome.exe]
  UDP    0.0.0.0:52971          216.58.214.174:443
 [chrome.exe]
  UDP    0.0.0.0:53550          8.8.4.4:443
 [chrome.exe]
  UDP    0.0.0.0:53740          142.250.201.162:443
 [chrome.exe]
  UDP    0.0.0.0:53810          77.136.192.89:443
 [chrome.exe]
  UDP    0.0.0.0:54097          216.58.213.70:443
 [chrome.exe]
  UDP    0.0.0.0:54450          142.250.75.228:443
 [chrome.exe]
  UDP    0.0.0.0:54681          216.58.215.45:443
 [chrome.exe]
  UDP    0.0.0.0:54986          172.217.20.198:443
 [chrome.exe]
  UDP    0.0.0.0:55082          142.250.178.130:443
 [chrome.exe]
  UDP    0.0.0.0:55309          216.58.215.46:443
 [chrome.exe]
  UDP    0.0.0.0:55938          216.58.214.174:443
 [chrome.exe]
  UDP    0.0.0.0:56293          216.58.213.74:443
 [chrome.exe]
  UDP    0.0.0.0:56382          172.217.20.162:443
 [chrome.exe]
  UDP    0.0.0.0:56847          142.250.178.131:443
 [chrome.exe]
  UDP    0.0.0.0:57045          216.58.215.46:443
 [chrome.exe]
  UDP    0.0.0.0:57217          172.217.18.202:443
 [chrome.exe]
  UDP    0.0.0.0:57303          142.250.178.138:443
 [chrome.exe]
  UDP    0.0.0.0:57830          172.217.20.162:443
 [chrome.exe]
  UDP    0.0.0.0:57844          *:*
  FDResPub
 [svchost.exe]
  UDP    0.0.0.0:57968          142.250.75.234:443
 [chrome.exe]
  UDP    0.0.0.0:58301          142.250.179.67:443
 [chrome.exe]
  UDP    0.0.0.0:58629          142.250.179.67:443
 [chrome.exe]
  UDP    0.0.0.0:58931          *:*
  Dnscache
 [svchost.exe]
  UDP    0.0.0.0:59020          172.217.18.202:443
 [chrome.exe]
  UDP    0.0.0.0:59304          142.250.178.138:443
 [chrome.exe]
  UDP    0.0.0.0:59727          172.217.20.198:443
 [chrome.exe]
  UDP    0.0.0.0:60005          216.58.205.46:443
 [chrome.exe]
  UDP    0.0.0.0:60528          8.8.8.8:443
 [chrome.exe]
  UDP    0.0.0.0:60554          142.250.178.138:443
 [chrome.exe]
  UDP    0.0.0.0:60952          172.217.20.170:443
 [chrome.exe]
  UDP    0.0.0.0:61490          142.250.179.97:443
 [chrome.exe]
  UDP    0.0.0.0:63417          172.217.20.162:443
 [chrome.exe]
  UDP    0.0.0.0:63687          216.58.214.161:443
 [chrome.exe]
  UDP    0.0.0.0:64321          142.250.75.238:443
 [chrome.exe]
  UDP    0.0.0.0:64556          216.58.214.78:443
 [chrome.exe]
  UDP    0.0.0.0:64653          142.250.179.67:443
 [chrome.exe]
  UDP    0.0.0.0:64718          172.217.20.170:443
 [chrome.exe]
  UDP    0.0.0.0:64732          142.250.178.131:443
 [chrome.exe]
  UDP    0.0.0.0:65139          216.58.214.163:443
 [chrome.exe]
  UDP    10.3.1.1:137           *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    10.3.1.1:138           *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    10.3.1.1:1900          *:*
  SSDPSRV
 [svchost.exe]
  UDP    10.3.1.1:2177          *:*
  QWAVE
 [svchost.exe]
  UDP    10.3.1.1:49249         *:*
  SSDPSRV
 [svchost.exe]
  UDP    10.3.2.1:137           *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    10.3.2.1:138           *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    10.3.2.1:1900          *:*
  SSDPSRV
 [svchost.exe]
  UDP    10.3.2.1:2177          *:*
  QWAVE
 [svchost.exe]
  UDP    10.3.2.1:49250         *:*
  SSDPSRV
 [svchost.exe]
  UDP    10.33.51.143:137       *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    10.33.51.143:138       *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    10.33.51.143:1900      *:*
  SSDPSRV
 [svchost.exe]
  UDP    10.33.51.143:2177      *:*
  QWAVE
 [svchost.exe]
  UDP    10.33.51.143:49253     *:*
  SSDPSRV
 [svchost.exe]
  UDP    127.0.0.1:1900         *:*
  SSDPSRV
 [svchost.exe]
  UDP    127.0.0.1:49254        *:*
  SSDPSRV
 [svchost.exe]
  UDP    127.0.0.1:51050        *:*
 [EDesktop.exe]
  UDP    127.0.0.1:53623        127.0.0.1:53623
  iphlpsvc
 [svchost.exe]
  UDP    192.168.32.1:137       *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    192.168.32.1:138       *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    192.168.32.1:1900      *:*
  SSDPSRV
 [svchost.exe]
  UDP    192.168.32.1:2177      *:*
  QWAVE
 [svchost.exe]
  UDP    192.168.32.1:49251     *:*
  SSDPSRV
 [svchost.exe]
  UDP    192.168.56.1:137       *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    192.168.56.1:138       *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    192.168.56.1:1900      *:*
  SSDPSRV
 [svchost.exe]
  UDP    192.168.56.1:2177      *:*
  QWAVE
 [svchost.exe]
  UDP    192.168.56.1:49248     *:*
  SSDPSRV
 [svchost.exe]
  UDP    192.168.136.1:137      *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    192.168.136.1:138      *:*
 Impossible d’obtenir les informations de propriétaire
  UDP    192.168.136.1:1900     *:*
  SSDPSRV
 [svchost.exe]
  UDP    192.168.136.1:2177     *:*
  QWAVE
 [svchost.exe]
  UDP    192.168.136.1:49252    *:*
  SSDPSRV
 [svchost.exe]
  UDP    [::]:123               *:*
  W32Time
 [svchost.exe]
  UDP    [::]:500               *:*
  IKEEXT
 [svchost.exe]
  UDP    [::]:3702              *:*
 [dashost.exe]
  UDP    [::]:3702              *:*
 [dashost.exe]
  UDP    [::]:3702              *:*
  FDResPub
 [svchost.exe]
  UDP    [::]:3702              *:*
  FDResPub
 [svchost.exe]
  UDP    [::]:4500              *:*
  IKEEXT
 [svchost.exe]
  UDP    [::]:5353              *:*
 [chrome.exe]
  UDP    [::]:5353              *:*
  Dnscache
 [svchost.exe]
  UDP    [::]:5353              *:*
 [chrome.exe]
  UDP    [::]:5353              *:*
 [chrome.exe]
  UDP    [::]:5353              *:*
 [chrome.exe]
  UDP    [::]:5353              *:*
 [chrome.exe]
  UDP    [::]:5353              *:*
 [chrome.exe]
  UDP    [::]:5355              *:*
  Dnscache
 [svchost.exe]
  UDP    [::]:51483             *:*
 [dashost.exe]
  UDP    [::]:51669             *:*
  Dnscache
 [svchost.exe]
  UDP    [::]:57845             *:*
  FDResPub
 [svchost.exe]
  UDP    [::]:58931             *:*
  Dnscache
 [svchost.exe]
  UDP    [::1]:1900             *:*
  SSDPSRV
 [svchost.exe]
  UDP    [::1]:49247            *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::1c1:6b45:9b7e:293a%9]:1900  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::1c1:6b45:9b7e:293a%9]:2177  *:*
  QWAVE
 [svchost.exe]
  UDP    [fe80::1c1:6b45:9b7e:293a%9]:49242  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::2c62:a90d:4377:c6%10]:1900  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::2c62:a90d:4377:c6%10]:2177  *:*
  QWAVE
 [svchost.exe]
  UDP    [fe80::2c62:a90d:4377:c6%10]:49241  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::3754:39e6:1cd9:dc52%17]:1900  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::3754:39e6:1cd9:dc52%17]:2177  *:*
  QWAVE
 [svchost.exe]
  UDP    [fe80::3754:39e6:1cd9:dc52%17]:49243  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::5e93:4948:226:601e%22]:1900  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::5e93:4948:226:601e%22]:2177  *:*
  QWAVE
 [svchost.exe]
  UDP    [fe80::5e93:4948:226:601e%22]:49244  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::b0e0:21c:e45e:6219%24]:1900  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::b0e0:21c:e45e:6219%24]:2177  *:*
  QWAVE
 [svchost.exe]
  UDP    [fe80::b0e0:21c:e45e:6219%24]:49245  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::bea3:6d81:698c:40d5%4]:1900  *:*
  SSDPSRV
 [svchost.exe]
  UDP    [fe80::bea3:6d81:698c:40d5%4]:2177  *:*
  QWAVE
 [svchost.exe]
  UDP    [fe80::bea3:6d81:698c:40d5%4]:49246  *:*
  SSDPSRV
 [svchost.exe]
```

# II. Setup Virtuel

## 1. SSH

### 🌞 Examinez le trafic dans Wireshark

-ssh utilise tcp

### 🌞 Demandez aux OS

```
PS C:\Users\celes> netstat

Connexions actives

  Proto  Adresse locale         Adresse distante       État
  TCP    10.5.1.1:61845         10.5.1.11:ssh          ESTABLISHED
```

```
[matis@node1 ~]$ ss -t
State   Recv-Q   Send-Q     Local Address:Port     Peer Address:Port   Process
ESTAB   0        52             10.5.1.11:ssh          10.5.1.1:61845
```

# II. Setup Virtuel

## 1. SSH

### 🌞 Examinez le trafic dans Wireshark

- déterminez si SSH utilise TCP ou UDP : TCP

voir fichier tp5_trafic.pcapng

### 🌞 Demandez aux OS

- repérez, avec une commande adaptée (netstat ou ss), la connexion SSH depuis votre machine

```
PS C:\Users\celes> netstat

Connexions actives

  Proto  Adresse locale         Adresse distante       État
  TCP    10.5.1.1:28517         10.5.1.11:ssh          ESTABLISHED
```

- ET repérez la connexion SSH depuis la VM

```
[matis@node ~]$ ss -t
State        Recv-Q        Send-Q               Local Address:Port               Peer Address:Port        Process
ESTAB        0             52                       10.5.1.11:ssh                    10.5.1.1:28517
```

## 2. Routage

### 🌞 Prouvez que

- node1.tp5.b1 a un accès internet
```
[matis@node ~]$ ping 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=115 time=26.4 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=115 time=12.3 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=115 time=13.4 ms
^C
--- 8.8.8.8 ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2003ms
rtt min/avg/max/mdev = 12.340/17.368/26.389/6.392 ms
```
- node1.tp5.b1 peut résoudre des noms de domaine publics (comme www.ynov.com)
```
[matis@node ~]$ ping ynov.com
PING ynov.com (104.26.10.233) 56(84) bytes of data.
64 bytes from 104.26.10.233 (104.26.10.233): icmp_seq=1 ttl=55 time=20.9 ms
64 bytes from 104.26.10.233 (104.26.10.233): icmp_seq=2 ttl=55 time=32.6 ms
^C
--- ynov.com ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1002ms
rtt min/avg/max/mdev = 20.872/26.758/32.644/5.886 ms
```

## 3. Serveur Web

### 🌞 Installez le paquet nginx

```
[matis@web ~]$ sudo dnf install nginx -y
```

### 🌞 Créer le site web

```
[matis@web var]$ mkdir www
```

```
[matis@web var]$ sudo mkdir www
```

```
[matis@web site_web_nul]$ sudo nano index.html
```

### 🌞 Donner les bonnes permissions

```
[matis@web ~]$ sudo chown -R nginx:nginx /var/www/site_web_nul
```

### 🌞 Créer un fichier de configuration NGINX pour notre site web

```
[matis@web ~]$ sudo nano /etc/nginx/conf.d/site_web_nul.conf
```

### 🌞 Démarrer le serveur web !

```
[matis@web ~]$ sudo systemctl start nginx
[matis@web ~]$ sudo systemctl status nginx
● nginx.service - The nginx HTTP and reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; disabled; preset: disabled)
     Active: active (running) since Fri 2023-11-17 22:25:58 CET; 11s ago
    Process: 1374 ExecStartPre=/usr/bin/rm -f /run/nginx.pid (code=exited, status=0/SUCCESS)
    Process: 1375 ExecStartPre=/usr/sbin/nginx -t (code=exited, status=0/SUCCESS)
    Process: 1376 ExecStart=/usr/sbin/nginx (code=exited, status=0/SUCCESS)
   Main PID: 1377 (nginx)
      Tasks: 2 (limit: 4673)
     Memory: 3.2M
        CPU: 28ms
     CGroup: /system.slice/nginx.service
             ├─1377 "nginx: master process /usr/sbin/nginx"
             └─1378 "nginx: worker process"

Nov 17 22:25:58 web.tp5.b1 systemd[1]: Starting The nginx HTTP and reverse proxy server...
Nov 17 22:25:58 web.tp5.b1 nginx[1375]: nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
Nov 17 22:25:58 web.tp5.b1 nginx[1375]: nginx: configuration file /etc/nginx/nginx.conf test is successful
Nov 17 22:25:58 web.tp5.b1 systemd[1]: Started The nginx HTTP and reverse proxy server.
```

### 🌞 Ouvrir le port firewall

```
[matis@web ~]$ sudo firewall-cmd --add-port=80/tcp --permanent
success
[matis@web ~]$ sudo firewall-cmd --reload
success
```

### 🌞 Visitez le serveur web !

```
[matis@node ~]$ sudo curl http://10.5.1.12
<h1>MEOW</h1>
```

### 🌞 Visualiser le port en écoute

```
[matis@web ~]$ ss -atnl
State          Recv-Q         Send-Q                  Local Address:Port                   Peer Address:Port         Process
LISTEN         0              511                           0.0.0.0:80                          0.0.0.0:*
```