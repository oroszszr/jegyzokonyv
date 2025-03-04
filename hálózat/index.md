# Nagytávolságú IP-Hálózatok   
**A feladatot végző neve:** Orosz Szabolcs és Csépke Péter  
**A feladat tárgya:** DHCPv4 konfigurálása  
**A feladat száma:** 01. mérés   
**A feladat dátuma:** 2025. 01. 09.   
**A feladatot vezette:** Csontos Dénes  
**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** Fizikai labor  

## Projektfeladat jelenlegi célja:  

Az alábbi projektfeladatban azt oldottuk meg,hogy egy kisirodai hálózatban a végberendezések IP címet kaptak a routertől, amit a DHCP konfigurálás segítségével oldottuk meg, ez felelős az IP címzésért és a megfelelő adatkapcsolatért, ezt szimuláltuk a Cisco Packet Tracer nevezetű alkalmazásban majd megvalósítottuk valóságban is.  

## Hálózati Topológia
  
Az alábbi képen láthatjuk a feladatban szereplő topológiát:  
![image](https://github.com/user-attachments/assets/716f02d5-0442-4d7c-9d10-215abca33d7a)  

## Valóságban  

![image](https://github.com/user-attachments/assets/439bb669-62d7-4b95-9449-5cc44217a3c4)


## Feladatban használt eszközök  
  - 2x HP ProBook 450 G7  
  - 2x Cisco 4200 series router  
  - 2x Catalyst 1000 series switch  
    
## IPv4 címzés  

| **Név** | **Port** | **IP/Maszk** | **Default gateway** |  
| --- | --- | --- | --- |  
| **PC0** | **Fa0/0** | **DHCP** | **DHCP** |  
| **Switch0** | **\-** | **\-** | **\-** |  
| **Router5** | **Gig0/0/0**<br><br>**Gig0/0/1** | **192.168.10.1/24**<br><br>**10.0.0.1/30** | **\-**<br><br>**\-** |  
| **Router6** | **Gig0/0/0**<br><br>**Gig0/0/1** | **192.168.20.1/24**<br><br>**10.0.0.2/30** | **\-**<br><br>**\-** |  
| **Switch1** | **\-** | **\-** | **\-** |  
| **PC1** | **Fa0/0** | **DHCP** | **DHCP** |  
| **Wireless Router0** | **Ethernet 0/1** | **\-** | **\-** |  
| **Smartphone0** | **Wireless0** | **DHCP** | **DHCP** |  

## Ismertetés  
A Wireless Router egy switchként viselkedik a jelenlegi hálózatunkban.  
Beállítottuk konzol jelszónak: „cisco”-t.  
Privilegizált mód jelszavának pedig a „class”-t.  
Titkosítottuk a jelszavakat.  
Beállítottuk a Router5-re napi üzenetet: „Ne nyulj a gepemhez!”  

### DHCP
A DHCP (Dynamic Host Configuration Protocol) egy hálózati protokoll, amely automatikusan kiosztja az IP-címeket és más hálózati konfigurációs információkat a hálózati eszközöknek.  
A DHCP lehetővé teszi, hogy a felhasználók és eszközök könnyen csatlakozzanak a hálózathoz anélkül, hogy manuálisan kellene beállítaniuk az IP-címeket.
A következő képeken a DHCP beállításokat láthatjuk.   
A képen látható, hogy 2 DHCP POOL-unk van 192.168.10.0/24 hálózat, illetve 192.168.20.0/24 hálózat. Ezeknek a hálózatoknak a szerepe hogy IP-t osszanak a PC-k számára. Mindkét hálózat képes 254 ip cím kiosztására.

![image](https://github.com/user-attachments/assets/580bd822-92ff-4c2c-bf88-ca544fa5be42)

![image](https://github.com/user-attachments/assets/ffc252cd-5560-4d86-93e7-14c361d69b9f)

### WIRELESS SETUP   
Vezeték nélküli biztonság beállításai:    
SSID (Service Set Identifier) : WIFI    
WPA2/PSK (Wi-Fi Protected Access 2 / Pre-Shared Key) Biztonsági protokollt használtunk   
Biztonság: AES (Advanced Encryption Standard)   
Passphrase: 293751287351823  

### IP ROUTE

A következő képen a routeren lévő irányító tábla bejegyzést látjuk.  
Ebből a táblából tudhatjuk meg hogy melyek a saját hálózataink és melyek a távoli hálózatok, amelyet egy másik router adott át ennek a routernek.  
A „C” betű a saját hálózatokat jelenti (connected) , míg az az „S” betűvel kezdődő útvonal a távoli hálózatot jelenti, amit a router megkapott a szomszédjától.  
Az IP route tábla egy olyan tábla, amelyet a routerek és a számítógépek használnak az IP-csomagok útvonalának meghatározására. Az útválasztási tábla tartalmazza a hálózati címeket, a következő ugrás (next hop) címét, a hálózati interfészeket és egyéb információkat, amelyek segítik a forgalom irányítását.  

### R6:  
![image](https://github.com/user-attachments/assets/851af274-bcc1-4be9-afac-c8c22db0b625)



### R5:  
![image](https://github.com/user-attachments/assets/636231de-8047-4eea-856f-b08f0d5a418b)


### Tesztelések  

Az adatátvitel tesztelése érdeken pingeltünk a telefonról a pc0-ra, utána pedig a pc0 és a pc1 közötti kapcsolatot vizsgáltuk meg. és látható hogy a kommunikációk sikeresek.  

### Smartphone-PC0 
![image](https://github.com/user-attachments/assets/41fb5f95-fabd-4e18-989c-709c605b8507)


Az alábbi képeken láthatjuk, hogy az első pingelésnél elveszik az adat, de utána hibamentesen fut tovább.  

### PC0-PC1  
![image](https://github.com/user-attachments/assets/849d829a-e462-43c2-b27c-2c72cd85e6db)


