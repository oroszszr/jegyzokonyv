# MÉRÉSI JEGYZŐKÖNYV
# Méréstechnikai Feladat: T Ellenállás-hálózat

**A mérést végző neve:** Orosz Szabolcs, Csépke Péter  és nemutolsó sorban Horvát Martin  
**A mérés tárgya:**  T Ellenállás-hálózat  
**A mérés száma:** 01. mérés  
**A mérés dátuma:** 2024. 12. 11.  
**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3 Labor  

## Feladatleírás  
680 Ohm impeddenciához illesztve kiszámítjuk a T-tag ellenállások értékeit, ahhoz, hogy 6 dB csillapítást kapjunk.
A falstad.com szimulációs programban megépítettük az áramkört és leszimuláltuk. Mindezekután ellenőriztük a csillapítást és az áramkör helyes működését.
A legvégén használtunk a magadaott értékekhez legközelebbi ellenállásokat.

## Elmélet
A T pad egy olyan speciális csillapító áramkör az elektronikában, amelynek topológiája a "T" betű formájában van megtervezve.
Az elektronikában a csillapítók a jel szintjének csökkentésére szolgálnak, és párnáknak is nevezik, mivel akusztikailag "lepárolják" a jelet. Lapfrekvenciás csillapítók, amelyek minden frekvenciát egyformán csillapítanak a működési sávban. Feladatuk ellentétes az erősítőkénél, és általában egyszerű szűrőszakaszok topológiáját követik.  

![image](https://github.com/user-attachments/assets/f8a050fe-b4bb-428d-aca4-6a32b5ef768d)  

## Eszközök  
  - Multiméter  
  - Ellenállások  
  - Breadboard  
  - Jelgenerátor  
  - Oszcilloszkóp  
  - vagy NI MYDAQ  

##  Ellenállások értékei:  
  - **számolás alapján:**  
    - Rg = 1.5 kΩ  
    - R1 = 498 Ω  
    - R2 = 2 kΩ  
  - **méréskor használt:**  
    - Rg = 2,2 kΩ X 2,2 kΩ  
    - R1 = 220 + 220 Ω 
    - R2 = 2.2 kΩ

## Számítások:

  $R1,2 = Z \times ( \frac {K - 1} {K + 1} ) = 1500 \times ( \frac {1,9953 - 1}  {1,9953 + 1} ) = 498$  
  
  $R3 = 2Z \times (\frac {K} {K^2 - 1}) = 2 \times 1500 \times (\frac {1,9953} {1,9953^2 - 1}) = 2007$  
  
  Z = 1500 Ω  
  K = 1.9953  
  Csillapítás: 6dB  
  
## Eredmények összehasonlítása: 
A feladatban használt és az elméleti eredmények eltérőek egymástól, mivel nincs ugyanolyan értékű ellenállás és figyelembe kell venni a mérésben felhasznált eszközök belső ellenállásait.


## Szimuláció
T tagú csillapítás szimulációja  
A T-tagú csillapítás szimulációja megmutatja, hogy a T-tag milyen hatékonyan csökkenti a rezgés amplitúdóját.  

## Breadboardon összerakott kapcsolás  
![image](https://github.com/user-attachments/assets/831ca6c4-4a58-4383-bc58-1cc7f7c5b499)

## Elméletben használt adatokkal

![image](https://github.com/user-attachments/assets/0503a83c-e624-4708-952e-9f4090244985)

## Gyakorlatban kiszámolt adatokkal

![image](https://github.com/user-attachments/assets/c217fba1-10b3-4275-9b3a-a2e50861495d)

## Oszcilloszkóppal készült kép

![Képernyőkép 2024-12-11 132340](https://github.com/user-attachments/assets/473fe8b5-d12a-427f-8c9c-4e72bb0e0265)



## Megjegyzések: 
A T csillapító áramkörrel kapcsolatos főbb nehézségek a következők:

Impedancia illesztés: Visszaverődések problémája.  
Frekvencia válasz: Csillapítási eltérések különböző frekvenciákon.  
Hőtermelés: Túlmelegedés kockázata.  
Zaj: Jelminőség romlása.  
Tolerancia: Alkatrészek eltéréseinek hatása.  
Szimmetria: Aszimmetrikus elrendezés következményei.  
Környezet: Hőmérséklet és páratartalom hatásai.  
Ezek a tényezők befolyásolják a rendszer teljesítményét és megbízhatóságát.  
