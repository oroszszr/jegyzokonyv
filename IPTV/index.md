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


## Feladat célja   
A földfelszíni digitális TV vételi rendszer kiépítése, a megfelelő adótorony kiválasztása, a jel mérésének és elosztásának elvégzése, és az IPTV rendszer konfigurálása.  

## Felhasznált eszközök  
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


Mindezek után megprónáltam beállítani a lehető legjobb jelerősséget minden zavaró tényező ellenére (ami végül az antenna szögállás: Délnyugat 234°), mint például;  
Környezeti tényezők:  

- Páratartalom:  68%
- Légnyomás: 1027 mBar 
- Hőmérséklet: 5°C 
- Szélerősség: 3,2 m/s



## Metek HDD adatok:  
- Jelszint: 51dB
- MER érték: 25dB
- Moduláció: DVBT/QPSK/8K/1/32
  
## DVB-T csatornák keresése:  

Multiplex C-t és D-t nem kötjük be mert kódolt csatornák vannak rajtuk, amik fizetősök.   

Multiplex A, B, E és Miskolc város TV-t fogjuk be, ami 4 darab bemenet lefoglalását jelenti.  

Megkerestük az ingyenesen fogható csatornákat és a lehető legtöbbet prübáltuk fogni a fejállomás bemenetinek segítségével.  
Egyetlen darab antennajelet fogunk 4 részre osztani ami lehetséges, hogy nem fog adni elég jelerősséget, de mivel most egy nagyobb nyereségű, erősebb antennát használtunk, ezáltal van elég jelerősség.  

## Fejállomás konfigurálása:  

Mindezek után a **program selection** fülre megyünk és konfiguráljuk  az **output** csatornakiosztás szerint.  
TS: (Transport Stream) amiből 4darab van belőle ezten az eszközön, és 1 csatornakiosztás 30Mbps maximális adatot képes továbbítani.  

Csatlakoztattam egy laptopot UTP kábel segítségével a fejállomásra **control portra**, hogy tudjam konfigurálni.   
Először konfiguráltam a laptop interfészt, amelynek egy tartoményba kell essen a **Lemco** ip címével. ( Jelen esetben 192.168.1.1 /24-et állítottunk be, és az alapértelmezett átjárót 192.168.1.200-ra )  
A **LEMCO** alap ip címe 192.168.1.200. Alap név és jelszó: **admin** és a kód **12345**.  

Az input fülön konfiguráltuk a csatornákat, először Multiplex A-val kezdtük, aminek vagy a frekvenciáját, vagy a csatornáját állítjuk át.(Jelen esetben a csatornát.) Ha már **lock**-olt állapotban van, akkor **unlock**-olni kell, és akkor változik meg a csatornakiosztás. Ugyanezen lépéseket meg kell ismételni a B, E és Miskolci Város TV-n is.  


## Hibakeresés:
Nem tudtuk elérni a konfigugációs oldalt, mint kiderült nem volt rendesen bedugva az UTP kábel.   
Nem volt M1, ezért újra kellett konfigurálni az input1en lévő 634 MHz csatornát 666 MHz-re.  

