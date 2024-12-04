# MÉRÉSI JEGYZŐKÖNYV
## A különböző típusú antennák teljesítménye és a vételi jelminőség összehasonlítása.  

**A mérést végző neve:** Orosz Szabolcs és Csépke Péter  
**A mérés tárgya:** A különböző típusú antennák teljesítménye és a vételi jelminőség összehasonlítása.  
**A mérés száma:** 2. mérés  
**A mérés dátuma:** 2024. 12. 04.  
**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3 Labor  

## Feladat célja
A hallgatók ismerkedjenek meg a különböző antennák sajátosságaival, és mérjék a sugárzott DVB-T jel minőségét a Johansson 8202 DVB-T modulátor segítségével. Az ISKRA P2845, ISKRA P20 LOGPER és IKUSI FLASHD C48 antennák alkalmazásával elemezzék a jelminőség és jelszint értékek változását különböző környezeti feltételek mellett.

## Feladatban használt eszközök  
  - Johansson 8202 DVB-T modulátor  
  - ISKRA P20 LOGPER antenna (vételre)  
  - ISKRA P2845 antenna (vételre)  
  - IKUSI FLASHD C48 antenna (vételre)  
  - Philips SDV5228 (adó oldalra)  
  - RF kábelek  
  - DVB-T vevő (pl. TV vagy mérőműszer)  
  - METEK HD spektrum/jelszint analizátor  
  - Laptop a jegyzőkönyv készítéséhez  

## Antennák teljesítménye különböző frekvenciákon

| Frekvencia (MHz) | Antenna          | Jelszint (dBm) | MER (dB) | Bitsebesség (Mbps) |
| ---------------- | ---------------- | -------------- | -------- | ------------------ |
| **618 MHz**      | Iskra P20        | -65.2          | 25.4     | 7.1 - 9.6          |
|                  | ISKRA P2845      | -50.4          | 32.2     | 5.6 - 9.5          |
|                  | IKUSI FLASHD C48 |         |    |          |
| **722 MHz**      | Iskra P20        | -55.5          | 32.2     | 8.1 - 9.6          |
|                  | ISKRA P2845      | -52.3          | 30.9     | 7.7 - 9.5          |
|                  | IKUSI FLASHD C48 |           |      |          |
| **834 MHz**      | Iskra P20        | -55.3          | 24.6     | 7.8 - 9.5          |
|                  | ISKRA P2845      | -51.7          | 26.1     | 7.8 - 9.5          |
|                  | IKUSI FLASHD C48 |           |         |          |

##  Mérési eredmények 
Az adatok alapján az alábbi következtetéseket lehet levonni:
- **Jelszint (dBm)**: Az **ISKRA P2845** és az **IKUSI FLASHD C48** antennák általában jobban teljesítettek a jelszint tekintetében, különösen a 570 MHz frekvencián. Az **ISKRA P20** antenna alacsonyabb jelszintet produkált mindhárom frekvencián.
- **MER (Modulation Error Ratio)**: A **MER** értékek alapján az **ISKRA P2845** antenna mutatta a legjobb teljesítményt, különösen a középső frekvencián (570 MHz), ahol a **MER** értéke 33.2 dB volt. Az **IKUSI FLASHD C48** antenna szintén jó **MER** értékeket ért el, de az **ISKRA P20** kicsit alulmaradt.
- **Bitsebesség**: A bitsebesség szintén magasabb volt az **ISKRA P2845** és az **IKUSI FLASHD C48** esetében, míg az **ISKRA P20** antennánál kicsit alacsonyabb értékeket tapasztaltunk. A legmagasabb bitsebességet 570 MHz-en az **ISKRA P2845** érte el (10.0 Mbps).

##  Tapasztalatok
A végzett mérések alapján az ISKRA P2845 antenna bizonyult a legerősebbnek a jelszint, a MER és a bitsebesség szempontjából egyaránt. Az IKUSI FLASHD C48 szintén jól teljesített, míg az ISKRA P20 gyengébb eredményeket mutatott. Az antennák közötti eltérések egyértelműen megfigyelhetők a különböző frekvenciákon, különösen 618 MHz-en, ahol a legnagyobb teljesítménykülönbség volt észlelhető.
