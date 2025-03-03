# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: Műhold

**A mérést végző neve:** Orosz Szabolcs  
**A mérés tárgya:**  Műholdas vételi rendszer kiépítése     
**A mérés száma:** 03. mérés    
**A mérés dátuma:** 2025. 03. 03.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1   
**Helyszín:** V3 Labor, kisudvar    

## Feladat célja   
Egy szabadon fogható (FTA) csatorna véletének beállítása, műholdas vételi rendszer kiépítése és vizsgálata, majd optimális vételi jel csatlakoztatása egy set op boxba, amin keresztül képet jelenítünk meg.  

## Felhasznált eszközök   
- Parabolaantenna: D80 Mesh 
- Műholdvevő fej (LNB):Ekselans SATCR LNB
- Set-top box: Amiko HD 8265+
- METEK HDD jelmérő
- Koaxiális kábelek és csatlakozók
- 2-es műholdas jelosztó
- Szerelési eszközök: csavarhúzó, villáskulcs, iránytű, dőlésszögmérő

## Feladat menete  
Mindenekelőtt összeszereltem az antennát, és rátekertem az általam kiválasztott LNB fejegységet (Ekselans SATCR).  
Internetes műholdvevő adatbázisból (lyngsat.com) kikerestem a(z) FTA csatornákat és választottam egyet, amely az Eutelsat 9B máhold sugároz.  
Iránytű segítségével beállítottam az antenna dőlésszögét, polarizációját és a METEK HDD segítségével a lehető legjobb jelet próbáltam megkeresni aminek végül az tetőponti (azimuth) szöge 198 fok lett, emelkedési szöge (elevation) 36 fok és LNB skew (elforgatási) szög 10° lett.  
Csatlakoztattam egymással az LNB vevőfejet és a set top boxot, mindezek után csatlakoztattam a set top boxot egy monitorra.  
Beállítottam a megfelelő régiót, orszgágot és az automatikus csatornakeresést.  

## METEK HDD képek és jelszintmérés  

Az alábbi kép a spektrumanalizátoron lévő műholdas jelszint kijelzőjét mutatja.   

![image](https://github.com/user-attachments/assets/37097f97-6894-45c8-957a-eb51d4acb0b9)   

Fontosabb információk: 
  - A vizsgált frekvencia 1358.0 MHz.
  - A műhold: Eutelsat 9A (9B-vel megegyező csatornakiosztásai vannak).
  - MER (Modulation Error Ratio) érték : 11.9 dB (közepes)
  - Jelszint: 83.2 dBuV (egész erős jel)
  - A beesések interferenciára is utalhatnak

A következő képen pedig láthatóak a csatornainformációk.    

![image](https://github.com/user-attachments/assets/01450615-d799-4418-81a3-4d7ad422f031)  

- Csatorna neve: M1 HD.
- Service ID: 101
- Network ID: 158
- ONID (Original Network ID) érték: 106
- Felbontás: 1920 × 1080 (Full HD)
- VPID (Video PID) és bitráta: 1101 / 3.989220 Mb/s (H.264 tömörítés)
- APID (Audio PID) és bitráta: 1201 / 0.415802 Mb/s (AC3 hangformátum)


## Hibakeresés  
Nem kaptunk képet, mint kiderült hibás UTP kábel végett.  
Beállítottuk a Hot Bird 13-ra a spektrumanalizátort, beállítottuk az antennát a megfelelő szögállásba, finomhangoltuk  és 80dBuV jel ellenére sem kaptunk képet.  
