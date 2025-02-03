# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: Hálózat tervezés      

**A mérést végző neve:** Orosz Szabolcs  
**A mérés tárgya:**  Mikrotik  
**A mérés száma:** 01. mérés    
**A mérés dátuma:** 2025. 01. 29.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1  
**Helyszín:** V3 Labor  

## Feladat Célja    
Komplex távközlési hálózat tervezése, telepítése és mérése  

## Felhasznált Eszközök (gyári beállítással):  
  - Mikrotik LHG18 LTE antenna    
  - 2db Mikrotik nRay 60GHz antenna   
  - 1db SOHO router (D-LINK vagy TP-LINK vagy ASUS)  

## Hálózati topológia tervezése és kiépítése  

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

Az alábbi antenna DHCP szerverként is üzemel ahol a következő címek között 192.168.88.100-192.168.88.250 oszt IP-t.

![image](https://github.com/user-attachments/assets/4ab30ad4-85a9-4e8f-8dca-6e6d14bc7d7f)

Az alábbi képen láthatóak a következő adatok:
- IP címünk és alhálózati maszkunk  
- DHCP szerver kiosztása
- Az operátor
- Data Class: LTE
- WAN (Wide area network) IP: 100.88.187.99
- RSSI (Received signal strength indicator): -51dBm
- RSRP (Reference Signals Received Power): -80dBm
- SINR (Signal-to-interference-plus-noise ratio): 23dB
- RSRQ (Reference Signal Received Quality): -13dB

### Soho router: 

Routert csak úgy szabad konfigurálni hogy semmi nincs rajta csak a gép  
Beállítottam WiFi SSID: GazdaXX (xx = saját azonosító ) Jelszó: G1234567   
AP módba kapcsolzam az eszközt és átkonfiguráltam a 192.168.88.X tartományba hogy ne legyen ütközés   

## Hálózati tesztelés és hibakeresés   

Ha a teszt nem indulna el, a Windows hálózati felderítést be kell kapcsolni  

### Mikrohullámú kapcsolat  

Először a mikrohullámú hálózat kapcsolatát végeztük el, nem ideális esetben, nem a legjobb adatátvitellel.  

![image](https://github.com/user-attachments/assets/dfbb5ba1-0a6d-49d1-83f3-9c8ece85b679)

Mindezek után beállítottuk a lehető legjobb átviteli sebességre koncentráltunk és próbáltuk beállítani.
Hálózati interferenciák léphetnek fel, tehát ez még mindig nem a legjobb eset.  

![image](https://github.com/user-attachments/assets/3f916704-0b11-48c0-a1c1-eaaf92108755)



### Google pingelése   

A képen láthat, hogy a google pingelése sikeres és van kapcsolat.  
Láthatjuk a minimális, maximális és az átlag pinget. Nincs csomagvesztés.  

![image](https://github.com/user-attachments/assets/d82f3a1b-bbb3-4089-ba17-973966c1a483)


### Speedtest  

Ezen a képen látható a ping, az internet fel és letöltési sebessége és a kiszolgáló.  

![image](https://github.com/user-attachments/assets/4295a55b-5303-47d0-8cf7-8e5f96f6d1e2)  

### Sávszélesség mérése iperf használatával  

![image](https://github.com/user-attachments/assets/31abd9d8-a13f-4607-9c84-29ae01daef0d)


## Hibakeresés 

Eleinte csak 100 Mb/s adatátvitellel tudtunk csatlakozni és pingelni a laptopok között. Mindezek után sikeresen megoldottuk a problémát és 1000 Mb/s adatátvitellel folytattuk a feladatot.  

<details>
  <summary>Ping tesztelés</summary>
  Pinging 192.168.88.1 with 32 bytes of data:
Reply from 192.168.88.1: bytes=32 time<1ms TTL=64
Reply from 192.168.88.1: bytes=32 time<1ms TTL=64
Reply from 192.168.88.1: bytes=32 time<1ms TTL=64

Ping statistics for 192.168.88.1:

    Packets: Sent = 3, Received = 3, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 0ms, Average = 0ms
    
C:\Users\Admin>ping 192.168.88.2

Pinging 192.168.88.2 with 32 bytes of data:
Reply from 192.168.88.2: bytes=32 time<1ms TTL=64
Reply from 192.168.88.2: bytes=32 time<1ms TTL=64
Reply from 192.168.88.2: bytes=32 time<1ms TTL=64

Ping statistics for 192.168.88.2:
    Packets: Sent = 3, Received = 3, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 0ms, Average = 0ms

C:\Users\Admin>ping 192.168.88.3

Pinging 192.168.88.3 with 32 bytes of data:
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64

Ping statistics for 192.168.88.3:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 1ms, Maximum = 1ms, Average = 1ms





