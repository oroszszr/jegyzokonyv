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
|                  | IKUSI FLASHD C48 | -49.2          | 34.2     | 8.0 - 10.3         |
| **722 MHz**      | Iskra P20        | -55.5          | 32.2     | 8.1 - 9.6          |
|                  | ISKRA P2845      | -52.3          | 30.9     | 7.7 - 9.5          |
|                  | IKUSI FLASHD C48 | -53.2          | 33.3     | 7.4 - 10.6         |
| **834 MHz**      | Iskra P20        | -55.3          | 24.6     | 7.8 - 9.5          |
|                  | ISKRA P2845      | -51.7          | 26.1     | 7.8 - 9.5          |
|                  | IKUSI FLASHD C48 | -65.2          | 23.3     | 7.8 - 9.3          |

##  Mérési eredmények 
Az adatok alapján az alábbi következtetéseket lehet levonni:
- **Jelszint (dBm)**: Az **ISKRA P2845** és az **IKUSI FLASHD C48** antennák általában jobban teljesítettek a jelszint tekintetében, különösen a 570 MHz frekvencián. Az **ISKRA P20** antenna alacsonyabb jelszintet produkált mindhárom frekvencián.
- **MER (Modulation Error Ratio)**: A **MER** értékek alapján az **IKUSI FLASHD C48** antenna mutatta a legjobb teljesítményt, különösen a középső frekvencián (722 MHz), ahol a **MER** értéke 34.2 dB volt. Az **ISKRA P2845** antenna szintén jó **MER** értékeket ért el, de az **ISKRA P20** kicsit alulmaradt.
- **Bitsebesség**: A bitsebesség szintén magasabb volt az **ISKRA P2845** és az **IKUSI FLASHD C48** esetében, míg az **ISKRA P20** antennánál kicsit alacsonyabb értékeket tapasztaltunk. A legmagasabb bitsebességet 722 MHz-en az **ISKRA P2845** érte el (10.6 Mbps).

##  Tapasztalatok
A végzett mérések alapján az **ISKRA P2845** antenna bizonyult a legerősebbnek a jelszint, a MER és a bitsebesség szempontjából egyaránt, kivéve a legmagasabb (824MHz) frekvencián. Az **IKUSI FLASHD C48** szintén jól teljesített, míg az **ISKRA P20** gyengébb eredményeket mutatott. Az antennák közötti eltérések egyértelműen megfigyelhetők a különböző frekvenciákon, különösen **618** MHz-en, ahol a legnagyobb teljesítménykülönbség volt észlelhető.

##  Grafikus ábrázolás
A jelszint és a MER értékek vizuális megjelenítését az alábbi diagramok szemléltetik:

## Ajánlások
Az **IKUSI FLASHD C48** antenna ajánlott elsődleges használatra, mivel a legtöbb frekvencián magasabb jelszintet és jobb jelminőséget biztosított. Ha költséghatékonyabb megoldásra van szükség, az **ISKRA P2845** szintén megfelelő alternatíva lehet. Az **ISKRA P20** csak alacsonyabb frekvenciákon ajánlott, ahol még elfogadható teljesítményt nyújt.

## P-20 Képek:
<details>
<summary>Kattins a részletekért</summary>

**722MHz Mért Képek**
![its_snapshot_0021](https://github.com/user-attachments/assets/4cb4c9c1-b9d1-4886-9cd6-85c5d16ca6a1)  


---

**834MHz Mért Képek**
![its_snapshot_0022](https://github.com/user-attachments/assets/bf1d54d9-cda0-498d-93b2-1ac54792ba82)  

---

</details>

## FlashHD C-48 Képek:
<details>

<summary>Kattins a részletekért</summary>

**618Mhz Mért Képek:**
 ![its_snapshot_0026](https://github.com/user-attachments/assets/c6fa5ee6-0ab8-4ef5-8d43-68fb212e1ef0)


---

**722MHz Mért Képek**
  ![its_snapshot_0027](https://github.com/user-attachments/assets/551790d3-753d-4aba-b1a1-38d63aa39ea4)

---

**834MHz Mért Képek**
 ![its_snapshot_0028](https://github.com/user-attachments/assets/542fd9a3-5724-433b-9637-72d5bf6be518)

---

</details>

## P-2845 Képek:
<details>

<summary>Kattins a részletekért</summary>

**618Mhz Mért Képek:**
![its_snapshot_0025](https://github.com/user-attachments/assets/c644303f-8c7c-4ab9-8892-fbdfe678f168)


---

**722MHz Mért Képek**
![its_snapshot_0024](https://github.com/user-attachments/assets/65449345-39f6-4b31-9c99-602bc66658b5)


---

**834MHz Mért Képek**
![its_snapshot_0023](https://github.com/user-attachments/assets/acf267d9-503e-4d2f-831a-59cc1db31b1a)


---

</details>

