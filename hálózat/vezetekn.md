# Nagytávolságú IP-Hálózatok   

**A feladatot végző neve:** Orosz Szabolcs   
**A feladat tárgya:** Vezeték nélküli hálózat kiépítése  
**A feladat száma:** 02. mérés   
**A feladat dátuma:** 2025. 02. 06.   
**A feladatot vezette:** Csontos Dénes  
**Évfolyam:** 13. E  
**Csoport:** GYAK 1   
**Helyszín:** Fizikai labor  


## Projektfeladat célja   
A projektfeladat célja egy működő hálózati topológia kiépítése és vezeték nélküli router által hálózati elérés biztosítása.  

## Feladatban használt eszközök  
  -  HP ProBook 450 G7 eszközök konfigurálására és pingelésekre  
  -  Catalyst 1000 series switch router számára internetelérés biztosítása  
  -  TP-LINK TR-WR841N 300Mbps wireless router hálózati elérés biztosítására  
  -  POCO X3 PRO telefon pingelésre és hálózat minőségének tesztelésére  

## Feladatleírás röviden  
- Hálózati eszközök felkonfigurálása és tesztelése. 
- Hálózati beállítások (LAN, DHCP, Wi-Fi security) elvégzése.
- Jelerősség és hálózati teljesítmény tesztelése különböző eszközökön. pl.: telefon, laptop.
- Parancssori eszközökkel hálózati adatok tesztelése és ellenőrzése (pl. pingelés, útvonal követése, port lista stb).  
 
## Hálózati topológia   

![image](https://github.com/user-attachments/assets/6306094c-c945-4a58-bd0a-b2decedb23b7)

## Router beállítások  

### Quick setup   

A képen látható a hálózat elérésére szolgáló név, a régió, a titkosítás típusa és a jelszó is.  

![image](https://github.com/user-attachments/assets/368ebf63-e743-412d-98cb-8a41360bd889)  

### LAN beállítás   

Láthatjuk a router IP címét, MAC-Adress-ét és az alhálózati maszkot.  

![image](https://github.com/user-attachments/assets/21f1bc5a-cfae-4e3a-902d-a76dc24ae189)  

### DHCP beállítás  

A router DHCP szerverként viselkedik és automatikusan oszt IP címet a rá csatlakozó eszközök számára. 192..168.4.194 - 192.168.4.204 IP címig oszt.  

![image](https://github.com/user-attachments/assets/1fb2d6f8-da4c-4914-8771-aeabb88a6f0a)

### Wireless security  

![image](https://github.com/user-attachments/assets/588f51c2-dbf0-4879-bdb9-4227bc61ac26)

## Hálózati tesztek és szávszélesség analizálás  

![image](https://github.com/user-attachments/assets/aec96ae6-ac13-4aaf-b0fc-4a8420fdf107)

<img src="https://github.com/user-attachments/assets/a27b8105-ffce-4e3e-b9bb-455c5e8a3f7a" width="400" height="850">  

![image](https://github.com/user-attachments/assets/606e1886-c314-4613-b589-c0e14c2a553b)


### Hálózati jelerősség  

**Laptopon vezeték nélkül**

![image](https://github.com/user-attachments/assets/d3b5c37d-871a-4af1-b3ad-742ab3550e38)

**Telefonon vezeték nélkül**

Láthatjuk hogy gyengébb jelerősséggel rendelkezünk telefonon vezeték nélkül, mint laptopon.  

<img src="https://github.com/user-attachments/assets/9abd2f62-b67d-4042-b3a5-34be1ed6fb91" width="400" height="850">  

## Számítógépen parancssor segítségével megjelített adatok  

**Ipconfig**  

![image](https://github.com/user-attachments/assets/f0d26d4d-3c5a-4627-b39c-cf4cd36e2b56)  

**Saját telefon pingelése**  

![image](https://github.com/user-attachments/assets/e8d6bbf2-c4e6-4068-b3d5-f89e37342a08)

**Routing tábla**  

![image](https://github.com/user-attachments/assets/21cec3fb-3512-4e61-8c65-93f02f303d6d)  

**Misrosoft.com pingelése**  

![image](https://github.com/user-attachments/assets/d7fd821f-26c2-4504-91c3-cb4fbf52e4f3)

**ipon.hu szerver felé történő útvonal lekövetése**  

![image](https://github.com/user-attachments/assets/3e4a13b4-5654-41d3-b1d5-92c6213444d1)

**Minden használt port listázása**  

![image](https://github.com/user-attachments/assets/1792757b-a242-4ff0-a15e-642bd917604c)

**DNS szerver aktualizálása**  

![image](https://github.com/user-attachments/assets/edfe8206-aad0-43f2-aea2-4277c2ea06c8)

**Csatolt hálózati meghajtók**  

![image](https://github.com/user-attachments/assets/c6847559-2fe6-4b68-afe4-c70f9ae6c16f)

**ipon.hu szerver tartománynév és IP**   

![image](https://github.com/user-attachments/assets/6e7478a7-38cf-4a2d-b39e-d7eb3454d602)

**FQDN megjelenítése az idegen címek számára**  

![image](https://github.com/user-attachments/assets/6c1841d2-a7c9-4ea8-ae76-c6fad00bd0a7)

**IP cím eldobása**  

![image](https://github.com/user-attachments/assets/2a1e4852-4597-4b8d-963d-0dcac598f3ae)

**Új IP cím kérése**  

![image](https://github.com/user-attachments/assets/924c34e6-94c4-45a9-ad16-ca6d713cbfb8)


## Összegzés  
A vezeték nélküli hálózat készítése közben figyelembe kellett vegyem azt, hogy nem a legideálsiabb körülmények között mértük a jelet.  
Egyszerre több router adott jelet, amik interferenciát okoztak, ezáltal nem a legerősebb jelet fogtuk.  
