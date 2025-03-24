# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: Műhold

**A mérést végző neve:** Orosz Szabolcs  
**A mérés tárgya:**  Műholdas vételi rendszer kiépítése     
**A mérés száma:** 09. mérés    
**A mérés dátuma:** 2025. 03. 24.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1   
**Helyszín:** V3 Labor, kisudvar    

## Feladat célja   
Egy szabadon fogható (FTA) csatorna véletének beállítása, műholdas vételi rendszer kiépítése és vizsgálata, majd optimális vételi jel csatlakoztatása egy set op boxba, amin keresztül képet jelenítünk meg.  



## Felhasznált eszközök   
- Parabolaantenna: D80 Mesh 
- Műholdvevő fej (LNB):Ekselans SATCR LNB
- Set-top box:  AMIKO HYBRID E2 VIPER 4K V40
- METEK HDD jelmérő
- Koaxiális kábelek és csatlakozók
- 2-es műholdas jelosztó
- Szerelési eszközök: csavarhúzó, villáskulcs, iránytű, dőlésszögmérő


## Feladat menete  
Internetes műholdvevő adatbázisból (lyngsat.com) kikerestem a(z) FTA csatornákat és választottam egyet, amely végül a(z) Thor 5 műhold lett.  
Iránytű segítségével beállítottam az antenna dőlésszögét, polarizációját és a METEK HDD segítségével a lehető legjobb jelet próbáltam venni. Finomhangolást követően a antenna szögállása 210°, a dőlésszöge 31° , és az LNB szöge 18° lett.   
Csatlakoztattam egymással az LNB vevőfejet és a set top boxot, mindezek után csatlakoztattam a set top boxot egy monitorra.  
Beállítottam a megfelelő régiót, országot és végrehajtottam a manuális csatornakeresést.   

![image](https://github.com/user-attachments/assets/17d23c9c-efe0-4876-8cf2-958f2b87f4e6)

### Információk

- **Frekvencia:** 1530.0 MHz  
- **Műhold:** Thor 5/6  
- **Transzponder:** 12130H28000  
- **Moduláció:** DVB-S / QPSK / 7/8  
- **Jelszint (Power):** 85.5 dBuV  
- **Noise Margin:** 5.6 dB  
- **MER (Modulation Error Ratio):** 13.1 dB  
- **Csomaghibák (Packet Errors):** 0  


![image](https://github.com/user-attachments/assets/9365606b-d021-406a-9efa-6eed9419c01d)

### Fontosabb Információk (Galaxy4)

- **Service ID:** 2710  
- **Csatorna neve:** Galaxy4  
- **Felbontás (Resolution):** 720x576  
- **VPID / Bitrate:** 601 / 1.748085 Mb/s  
- **APID / Bitrate:** 834 / 0.089645 Mb/s  
- **Szolgáltatás típusa:** FREE (szabadon fogható)

## A következő képek a TV-ről készült adatokat mutatja  

![image](https://github.com/user-attachments/assets/c8c21690-2a59-4c5b-a16c-25be2b5b1cb3)

### Jelerősség és műhold adatok

### Paraméterek  
- **SNR (Signal-to-Noise Ratio):** 100 %
- **AGC (Automatic Gain Control):** 77 %
- **BER (Bit Error Rate):** 0  
## Tuner:
- **Tuner típusa:** Tuner A: DVB-S2 NIM (DVB-S2X)
## Műhold:
- **Pozíció:** 0.8W
- **Műhold:** Ku-band Thor 5/6/7 & Intelsat 10-02
- **Transzponder:** 12130 H 28000 7/8


![IMG_20250324_122547](https://github.com/user-attachments/assets/c9156f06-b763-4874-9f26-e7393721ccf4)

- **Felbontás**: 720x576p25
- **Kódolás**: MPEG2 H.262
- **Átvitel**: DVB-S 12130 MHz H 28000 7/8 QPSK 0.8°W
- **Időtartam**: 115 perc
- **Képarány**: 16:9
- **Jelerősség (SNR)**: 100%


