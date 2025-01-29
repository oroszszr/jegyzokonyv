# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: PI Ellenállás-hálózat    

**A mérést végző neve:** Visnyei Sándor  
**A mérés tárgya:**  Mikrotik  
**A mérés száma:** 01. mérés    
**A mérés dátuma:** 2025. 01. 28.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3 Labor  

## Feladat Célja    
Komplex távközlési hálózat tervezése, telepítése és mérése  

## Eszközök:  
  - Mikrotik LHG18 LTE antenna    
  - 2db Mikrotik nRay 60GHz antenna   
  - 1db SOHO router (D-LINK vagy TP-LINK vagy ASUS)  

## Előkészítés és tervezés  

### Eszközök gyári beállításinak visszaállítása (Factory reset)  
- Tápellátásból kihúzzuk
- reset gombot lenyomva tartjuk
- tápellátás visszacsatlakoztatása
- tartsuk lenyomva amíg a STATUS LED villogni nem kezd
- engedje el és visszaáll gyári beállításokra

### Hálózati topológia tervezése és kiépítése  
![image](https://github.com/user-attachments/assets/71bf45c6-ea60-45e6-9ae0-b3d8d9d755b6)

### IP-cím kiosztás:  
- Mikrotik LHG18 LTE: 192.168.88.1  
- Mikrotik nRay 60GHz Master: 192.168.88.2  
- Mikrotik nRay 60GHz Slave: 192.168.88.3  
- Router (AP mód): 192.168.88.4  
- Switch (ha szükséges): 192.168.88.254  
- Kliens laptop: 192.168.88.100-250 (DHCP-ből) 


## Eszközök telepítése és konfigurálása  

### Mikrotik LGH18 LTE:
- Current Operator Telekom HU
- Data Class: LTE
- WAN IP: 100.82.157.99
- RSSI: -52dBm
- RSRP: -83dBm
- SINR: 21dB
- RSRQ: -12dB

###  Mikrotik nRay 60GHz Master:  
Ethernet kábellel csatlakoztam az antennára.   
Megynitottam a WinBox-ot és beírtam a 192.168.88.2 címet   
Felhasználónév: admin, jelszó antennán.   
Beállítottam Master módba.   
Figyeltem a dátum/idő beállításra  

### Mikrotik nRay 60GHz Slave:  
Megismételtemm az előző lépéseket a 192.168.88.3 IP címen   
Ellenőriztem a kapcsolat státuszát és a minőségét    
Készítettem képeket   

### Soho router: 
Routert csak úgy szabad konfigurálni hogy semmi nincs rajta csak a gép
Csatlakoztam a laptophoz etherneten keresztül   
Megnyitottam a cmd-t és beírtam az arp -a parancsot     
Megkerestem a megfelelő IP címet és felmentem a konfigurálási oldalra    
Beállítottam WiFi SSID: GazdaXX (xx = saját azonosító ) Jelszó: G1234567   
AP módba kapcsolzam az eszközt és átkonfiguráltam a 192.168.88.X tartományba hogy ne legyen ütközés   

## Hálózati tesztelés és hibakeresés   
Ha a teszt nem indulna el, a Windows hálózati felderítést be kell kapcsolni


### Ping teszt mérése   

### Sávszélesség mérése iperf használatával  

### Hibakeresés 
100 Mb/s
1000 Mb/s 




