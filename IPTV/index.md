# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: IPTV     

**A mérést végző neve:** Orosz Szabolcs  
**A mérés tárgya:**  IPTV vételi rendszer kiépítése     
**A mérés száma:** 02. mérés    
**A mérés dátuma:** 2025. 02. 03.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1   
**Helyszín:** V3 Labor  


### Feladat célja   
A földfelszíni digitális TV vételi rendszer kiépítése, a megfelelő adótorony kiválasztása, a jel mérésének és elosztásának elvégzése, és az IPTV rendszer konfigurálása.  

### Felhasznált eszközök  
- Antenna: Kültéri antenna (Iskra P2845) 
- Fejállomás: LEMCO SCL-824CT (8darab bemenet, 4darab kimenet)
- Set-top box: MAG IPTV  
- Hálózati eszköz: TP-Llink Archer C7
- METEK HDD digitális jelmérő
- Koaxiális kábelek és csatlakozók 
- Jelosztó: Ekselans RF16  osztó 5-2400MHz
- UTP kábelek
- Szerelési eszközök: csavarhúzó, villáskulcs, kábelvágó, iránytű, dőlésszögmérő

## Feladat menete  
Minden előtt reseteltem mindent és alapbeállításról kezdtem az egészet, hogy ne legyen zavaró tényező.  
Ezután megnéztem az **fmdx.hu** oldalon az avasi torony csatornakiosztását.   

Megkerestem a **Miskolc Városi TV** adást, ami **634MHz-en** lévő csatornán helyezkedik el. Azért választottuk ezt a csatornát mivel ez sugároz a leggyengébben (**0,126kW**), és ha ezen a csatornán jó a vétel, akkor a többin is jó lesz.  

![image](https://github.com/user-attachments/assets/201cb560-fc7d-4fd2-bc09-a4a3c71415aa)  
 
A képen látható az iskola és az adótorony közötti távolság.    

![image](https://github.com/user-attachments/assets/c292f11f-8834-4c62-890a-2fbab7d1e2d9)  


Mindezek után megpróbáltam beállítani a lehető legjobb jelerősséget minden zavaró tényező ellenére mint például;   
Környezeti tényezők:  

- Páratartalom:  68%
- Légnyomás: 1027 mBar 
- Hőmérséklet: 5°C 
- Szélerősség: 3,2 m/s

Végül az antenna szögállása: Délnyugat 234°  

### Metek HDD adatok:  

![image](https://github.com/user-attachments/assets/bb14acd7-33ab-42c0-a2e5-1fec20f5b9b4)

- Jelszint: 50.3dB
- Noise Margin: 19.8
- MER érték: 26.3dB
- Moduláció: DVBT/QPSK/8K/1/32
  
### DVB-T csatornák keresése:  

Multiplex C-t és D-t nem kötjük be mert kódolt csatornák vannak rajtuk, amik fizetősök.   

Multiplex A, B, E és Miskolc város TV-t fogjuk be, ami 4 darab bemenet lefoglalását jelenti.  


### Fejállomás konfigurálása:   
Megkerestük az ingyenesen fogható csatornákat és a lehető legtöbbet próbáltuk fogni a fejállomás bemenetinek segítségével.   
Egyetlen darab antennajelet fogunk 4 részre osztani ami lehetséges, hogy nem fog adni elég jelerősséget, de mivel most egy nagyobb nyereségű, erősebb antennát használtunk, ezáltal lesz elég jelerősség.   
Először konfiguráltam a laptop interfészt, amelynek egy tartoményba kell essen a **Lemco** ip címével. ( Jelen esetben 192.168.1.1 /24-et állítottunk be, és az alapértelmezett átjárót 192.168.1.200-ra )  
A **LEMCO** alap ip címe 192.168.1.200. Alap név és jelszó: **admin** és a kód **12345**.  

### Router konfigurálása:  

IGMP snooping bekapcsolása.   
Bemenet, kimenet és a laptop interface-t is IPTV-re állítjuk.  
Bridgeltünk LAN1-ről LAN3-ra közvetlenül IPTV-ről.    
Állítunk rá DHCP szervert, ami 192.168.1.100 tól 192.169.1.249-ig oszt IP-t, alapértelmezett átjáró 192.168.1.1.    

## Tesztelések és mérési eredmények:  

A táblázat összegzi a televíziós és rádiós csatornák adatait, a csatornák neveit, azonosítóit, logikai csatorna számát, IP-címét, portját és az adatátviteli protokollt. Ezek az adatok a csatornák jellemzőit és hozzáférhetőségét foglalja össze.  

| Input | Program title              | OriginalService ID | LCN1..1023 | Encrypted | TS Output | OutputService ID | IP address   | IP port | Protocol |
|-------|----------------------------|---------------------|------------|-----------|-----------|------------------|---------------|---------|----------|
| 1     | Input 1                    | M1 HD               | 100        | 0         | FTA       | 1                | 224.0.0.1     | 1001    | UDP      |
| 2     | Input 1                    | M4 Sport HD         | 101        | 0         | FTA       | 1                | 224.0.0.1     | 1002    | UDP      |
| 3     | Input 1                    | Duna HD             | 102        | 0         | FTA       | 1                | 224.0.0.1     | 1003    | UDP      |
| 4     | Input 1                    | DunaW/M4Sport+      | 103        | 0         | FTA       | 2                | 224.0.0.1     | 1004    | UDP      |
| 5     | Input 1                    | Kossuth Radio       | 130        | 0         | FTA       | 4                | 224.0.0.1     | 1005    | UDP      |
| 6     | Input 1                    | Petofi Radio        | 131        | 0         | FTA       | 4                | 224.0.0.1     | 1006    | UDP      |
| 7     | Input 1                    | Bartok Radio        | 132        | 0         | FTA       | 4                | 224.0.0.1     | 1007    | UDP      |
| 8     | Input 1                    | Danko Radio         | 133        | 0         | FTA       | 4                | 224.0.0.1     | 1008    | UDP      |
| 10    | Input 2                    | M2 HD               | 200        | 0         | FTA       | 1                | 224.0.0.1     | 1010    | UDP      |
| 11    | Input 2                    | M5 HD               | 201        | 0         | FTA       | 2                | 224.0.0.1     | 1011    | UDP      |
| 12    | Input 2                    | TV2                 | 202        | 0         | FTA       | 1                | 224.0.0.1     | 1012    | UDP      |
| 13    | Input 2                    | RTL                 | 203        | 0         | FTA       | 1                | 224.0.0.1     | 1013    | UDP      |
| 14    | Input 2                    | MAX4                | 206        | 0         | FTA       | 2                | 224.0.0.1     | 1014    | UDP      |
| 15    | Input 2                    | Spektrum Home +     | 207        | 0         | FTA       | 2                | 224.0.0.1     | 1015    | UDP      |
| 16    | Input 2                    | MinDig TV Plusz Info| 208        | 0         | FTA       | 2                | 224.0.0.1     | 1016    | UDP      |
| 37    | Input 3      | HEVC teszt          | 524        | 0         | FTA       | 2                | 224.0.0.1     | 1037    | UDP  |
| 39    | Input 4      | Miskolc TV          | 1000       | 0         | FTA       | 2                | 224.0.0.1     | 1039    | UDP  |



**8 MHz sávszélességgel sugároz mindegyik csatorna.**

Input 1 lett a multiplex A. A be

![image](https://github.com/user-attachments/assets/7a88021a-732e-4971-bdd9-9658415c0aa0)  

Input 2 felel meg multiplex B-ért.

![image](https://github.com/user-attachments/assets/e8fbf4ff-7d67-4cd5-9a08-86bfbd1e7a73)

Input 7 pedig a Miskolc Város TV.

![image](https://github.com/user-attachments/assets/4bae06d4-62bc-4f04-9bca-8dfc6dd3ff38)

Nemutolsó sorban az Input 8 pedig a multiplex E

![image](https://github.com/user-attachments/assets/a11b38c4-2c78-4c71-8d81-e2cb7f00286d)


### Hibakeresés:  
Nem tudtuk elérni a konfigugációs oldalt, mint kiderült nem volt rendesen bedugva az UTP kábel.   
Nem volt M1, ezért újra kellett konfigurálni az input1en lévő 634 MHz csatornát 666 MHz-re.   
1 - 1023-ig a portkiosztást nem fogadta el, 1024-től lehet kiosztani a portokat ahhoz, hogy működjön.  
224.224.244.1-es IP cím nem jó, .2-től működik a kiosztás.  

