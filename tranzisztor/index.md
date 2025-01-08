# MÉRÉSI JEGYZŐKÖNYV   
## Méréstechnikai Feladat: Tranzisztor működésének vizsgálata  
A mérést végző neve: Orosz Szabolcs  
A mérés tárgya: Tranzisztor működésének vizsgálata  
A mérés száma: 05. mérés  
A mérés dátuma: 2025. 01. 08  
A mérést vezette: Sándor Péter  

Évfolyam: 13. E  
Csoport: GYAK 2  
Helyszín: V3 Labor  

## Feladat célja:   
Tranzisztor kimeneti feszültségének és a kollektor áramának kiszámítása a megadott ellenállás értékekkel.  

## Elméleti háttér:   
A tranzisztor egy félvezető eszköz, amelyet elsősorban erősítésre és kapcsolásra használnak az elektronikai áramkörökben. Működése a félvezető anyagok, például szilícium vagy germánium tulajdonságain alapul, amelyek képesek az elektromos áram vezetésére és szigetelésére is, attól függően, hogy milyen típusú szennyező anyagokat adnak hozzá. A tranzisztor három fő részből áll: az emitterből, a bázisból és a kollektorból.   

## Feladatban használt eszközök:   
 - Ellenállások  
     - Rc = 220 Ω  
     - Rbe = 1,5k Ω  
 - Tranzisztor
     - β = 81
 - LED  
 - Metex m-3800  
      - Gyártási szám : 736015
 - NI MYDAQ


## Falstadban készített áramkör   
![circuit-20250108-1259](https://github.com/user-attachments/assets/f901c380-e224-44d1-95f5-a3bce1555f82)  

## Mérési táblázat 

| Ube [V]   | Urc [V]  | Ic   [mA]  | 
| --------- | -------  | ---------- | 
| 0         | 0        |      0     | 
| 0,1       | 0        |      0     | 
| 0,2       | 0        |     0      | 
| 0,3       | 0        |      0     |
| 0,4       | 0.1m     |    0,14    | 
| 0,5       | 3.1m     |    0,52    | 
| 0,6       | 113,9m   |       4,06 |
| 0,7       | 894      |       9,64 | 
| 0,8       | 2,12     |      11,73 | 
| 0,9       | 2,58     |      11,86 |   
| 1         | 2,61     |      11,95 |   
| 1,1       | 2,63     |        12  |   
| 1,2       | 2,64     |    12,05   |   


## Valóságban összetett áramkör
![IMG_20250108_131114](https://github.com/user-attachments/assets/6a6f9a24-ecf7-4968-b728-9873e940cca5)

## Megjegyzések:
A feladat során számos nehézséggel találkoztam, amelyek befolyásolták és lassították a megoldás folyamatát.A nevezetes és a mért adatok nem sokkal tértek el. Megfigyelhető, hogy 0 - 0,5 V-ig az áramkör zárt állásban volt. Mindezek után 0,6V értéknél nyílt ki a tranzisztor és kezdett világítani a LED. 1,2 V értéktől kezdett stabilizálódni és változatlan maradt az ellenálláson eső feszültség.

