
# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: DVB-T     

**A mérést végző neve:** Orosz Szabolcs  
**A mérés tárgya:**  Belső DVB-T rendszer kiépítése     
**A mérés száma:** 08. mérés    
**A mérés dátuma:** 2025. 03. 19.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1   
**Helyszín:** V3 Labor  


## Feladat célja  
A földfelszíni digitális TV vételi rendszer kiépítése, a megfelelő adótorony kiválasztása, a jel mérésének és csillpításának elvégzése.  

## Feladatban használt eszközök 
- Antenna:   Opticum Smart HD 550 beltéri antenna  
- Set-top box: Amiko  HD8265+  
- METEK HDD digitális jelmérő  
- Koaxiális kábelek és csatlakozók   
- Csillpító tag: Ekselans RF12 osztó 5-2400MHHz
- AOC  22E1Q Monitor  

## Feladat menete  

Először megnéztem az **fmdx.hu** oldalon az avasi torony csatornakiosztását.

Megkerestem a Miskolc Városi TV adást, ami 634MHz-en lévő csatornán helyezkedik el. Azért választottuk ezt a csatornát mivel ez sugároz a leggyengébben (0,126kW), ezért, ha itt a lehető legjobb vételt biztosítjuk, a többi adón elméletileg csak jobb jel lehet, mert erősebben sugároznak és ha ezen a csatornán jó a vétel, akkor a többin is értelem szerűen jó lesz.    

**Miskolc Avas csatornakiosztás**  

![image](https://github.com/user-attachments/assets/6f91d61d-9400-488c-8016-16d213205697)


A képen látható az iskolai építmény és az adótorony közötti távolság.  

![image](https://github.com/user-attachments/assets/049e16d7-b1e0-4158-b01f-1cbbb43793f3)

Minden zavaró tényező ellenére megpróbáltam beállítani a lehető legjobb jelerősséget.   

**Környezeti tényezők:**  
- Páratartalom: 26%
- Légnyomás: 1033 mBar
- Hőmérséklet: 9°C
- Szélerősség: 3 km/h

## Metek HDD adatok, és jelszintmérés   

### Metek HDD-n mért adatok a csillpítótag csatlakoztatása előtt:  

### 530 MHz     
![530sima](https://github.com/user-attachments/assets/951e8a68-bb37-4e53-972d-b34266d47e3d)  

### Adatok:  

- Jelerősség: 62,7dBuV
- Moduláció: 64QAM
- Noise margin: 10,5
- MER érték: 26,7dB


### 554Mhz    
![554sima](https://github.com/user-attachments/assets/4e1ed134-ec3c-4dc4-b2e7-534c5aef08a9)

### Adatok:   

- Jelerősség: 56,2dBuV
- Moduláció: 64QAM
- Noise margin: 11,5
- MER érték: 27,7dB


### 586Mhz  
![586sima](https://github.com/user-attachments/assets/38fd9034-5dbb-4b0e-8324-562851b5c765)

### Adatok: 

- Jelerősség: 56dBuV
- Moduláció: 64QAM
- Noise margin: 13
- MER érték: 29,7dB


### 634MHz (Miskolc Városi TV)  
![634sima](https://github.com/user-attachments/assets/4185ae51-e0c2-4310-94a1-59c9536addb9)

### Adatok: 

- Jelerősség: 47dBuV
- Moduláció: QPSK
- Noise margin: 17,6
- MER érték: 26,7dB


### 666MHz  
![666sima](https://github.com/user-attachments/assets/714aa4a9-c87f-4c85-a2b4-b331c1913ba7)

### Adatok: 

- Jelerősség: 57,7dBuV
- Moduláció: 64QAM
- Noise margin: 7,5
- MER érték: 24,2dB


### 690MHz  
![690sima](https://github.com/user-attachments/assets/65ed0a4a-3da6-4910-b5f5-9b41f703489d)

### Adatok: 

- Jelerősség: 56dBuV
- Moduláció: 64QAM
- Noise margin: 8,4
- MER érték: 24,5dB


### Metek HDD-n mért adatok a csillpítótag csatlakoztatásával:  

### 530Mhz  
![530cs](https://github.com/user-attachments/assets/d0ee7dd0-155c-4d94-9fcf-0f06455ffdbd)

### Adatok: 

- Jelerősség: 60,1dBuV
- Moduláció: 64QAM
- Noise margin: 12,1
- MER érték: 28,2dB

### 554MHz  
![554cs](https://github.com/user-attachments/assets/db4d80b6-b577-4f7a-b402-09fed2a53767)

### Adatok: 

- Jelerősség: 57dBuV
- Moduláció: 64QAM
- Noise margin: 9,7
- MER érték: 25,8dB


### 586MHz  
![586cs](https://github.com/user-attachments/assets/0d1fef5d-d439-43ed-8093-931df7a9b6df)

  ### Adatok: 

- Jelerősség: 56,8dBuV
- Moduláció: 64QAM
- Noise margin: 9,9
- MER érték: 26,5dB

### 634MHz
![634cs](https://github.com/user-attachments/assets/27ad539f-115f-440a-b084-ddac5a230f13)

  ### Adatok: 

- Jelerősség: 56dBuV
- Moduláció: QPSK  
- Noise margin: 16,1
- MER érték: 19,8dB


### 666MHz  
![666cs](https://github.com/user-attachments/assets/8c77c9d7-1dfe-466d-a5a8-1972e88250b8)
Az alábbi csatornán csomegvesztés következett be.  
  ### Adatok: 

- Jelerősség: 52,4dBuV
- Moduláció: 64QAM
- Noise margin: 2,9
- MER érték: 19,6dB
- Packet errors: 230


### 690MHz
![690cs](https://github.com/user-attachments/assets/04800a95-9a0e-4ac5-bd3b-70fcbecf6c4e)

### Adatok: 

- Jelerősség: 53,1dBuV
- Moduláció: 64QAM
- Noise margin: 8,4
- MER érték: 24,6dB



