# MÉRÉSI JEGYZŐKÖNYV
# Méréstechnikai Feladat: PI Ellenállás-hálózat

**A mérést végző neve:** Orosz Szabolcs és Csépke Péter  
**A mérés tárgya:** Méréstechnikai Feladat: PI Ellenállás-hálózat  
**A mérés száma:** 1. mérés  
**A mérés dátuma:** 2024. 11. 13  
**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3 Labor  

## Feladat Célja
A PI ellenállás-hálózat jellemzőinek meghatározása a megadott ellenállásértékek alapján. Impedanciaillesztés.  

## Elméleti Háttér
Az áramkör arról kapja a nevét, hogy az ellenállásokat a görög "Π" formájában kötjük össze. Az érétkeket a következő képletekkel számoljuk ki:
A PI ellenállás-hálózat egy egyszerű, de hatékony módja az impedancia illesztésének és a jel csillapításának. Az R3 és R4 ellenállások közötti viszonyok meghatározzák a hálózat teljesítményét és a kimeneti jelet.

## Eszközök
- Elméletbeli Ellenállások:
  - R3 = 2046 Ω
  - R4 = 508 Ω
- Gyakorlati  ellenállások
  - R3 = 2,2 kΩ
  - R4 = 
- Ni myDAQ 

## Számítások
<img src="https://github.com/oroszszr/jegyzokonyv/blob/main/meres1/keplet.PNG" width="300" height="170">  

## Csillapítási Eredmények gyakorlatban 

### Megadott Értékek  
- **Bemeneti Feszültség ($V_{in}$)**: 10.088 V  
- **Kimeneti Feszültség ($V_{out}$)**: 5.366 V  

### Csillapítás Kiszámítása (dB)  
A csillapítást a következő képlettel számoltuk ki:  
$$A = 20 \cdot \log_{10}\left(\frac{V_{out}}{V_{in}}\right)$$  

1. **Hányados Számítása:**  
   $$\frac{V_{out}}{V_{in}} = \frac{5.366}{10.088} \approx 0.532$$  

2. **Logaritmus Számítása:**  
   $$\log_{10}(0.532) \approx -0.273$$  

3. **Csillapítás Kiszámítása:**  
   $$A \approx 20 \cdot (-0.273) \approx -5.46 \, \text{dB}$$  

### Százalékos Csillapítás Kiszámítása  
A százalékos csillapítást a következő képlettel számoltuk ki:  
$$\text{Csillapítás (\%)} = \left(1 - \frac{V_{out}}{V_{in}}\right) \times 100$$  

1. **Csillapítás Kiszámítása:**  
$$\text{Csillapítás (\%)} = \left(1 - 0.532\right) \times 100 \approx 46.8\%$$  

### Eredmények
- **Csillapítás (dB)**: -5.46 dB  
- **Csillapítás (%)**: 46.8%  

### A kapcsolási rajz ábrázolja a Pi csillapítót a gyakorlati ellenállás értékekkel:
<img src="https://github.com/oroszszr/jegyzokonyv/blob/main/meres1/falstad2.PNG" width="770" height="400">

## Csillapítási Eredmények elméletben  

### A kapcsolási rajz ábrázolja a Pi csillapítót az kiszámított ellenállás értékekkel:

### Megadott Értékek
- **Bemeneti Feszültség ($V_{in}$)**: 10 V
- **Kimeneti Feszültség ($V_{out}$)**: 5.011 V

### Csillapítás Kiszámítása (dB)  
A csillapítást a következő képlettel számoltuk ki:  
$$A = 20 \cdot \log_{10}\left(\frac{V_{out}}{V_{in}}\right)$$  

1. **Hányados Számítása:**  
   $$\frac{V_{out}}{V_{in}} = \frac{5.011}{10} = 0.5011$$  

2. **Logaritmus Számítása:**  
   $$\log_{10}(0.5011) \approx -0.299$$  

3. **Csillapítás Kiszámítása:**  
   $$A \approx 20 \cdot (-0.299) \approx -5.98 \, \text{dB}$$  

### Százalékos Csillapítás Kiszámítása  
A százalékos csillapítást a következő képlettel számoltuk ki:  
$$\text{Csillapítás (\%)} = \left(1 - \frac{V_{out}}{V_{in}}\right) \times 100$$  

1. **Csillapítás Kiszámítása:**  
$$\text{Csillapítás (\%)} = \left(1 - 0.5011\right) \times 100 \approx 49.89 \%$$  

### Eredmények
- **Csillapítás (dB)**: -5.98 dB
- **Csillapítás (%)**: 49.89 %

<img src="https://github.com/oroszszr/jegyzokonyv/blob/main/meres1/falstad1.PNG" width="770" height="400">

### Elemzés
A PI csillapító (PI pad) ellenállásos áramkör elemzése során megállapítható, hogy a tervezett áramkör hatékonyan csökkenti a jel amplitúdóját, miközben megőrzi annak formáját. Az áramkör négy fő összetevőből áll: három ellenállásból és egy terhelő ellenállásból. Megfigyelhető, hogy kisebb eltérések vannak a számított és a mért értékek között.

### Következtetések
A PI csillapító áramkör sikeresen megvalósult, és a tesztelési eredmények azt jelzik, hogy a csillapítási teljesítmény összhangban van a tervezett specifikációkkal. A mérések alapján a csillapító hatás a kívánt frekvenciatartományban optimális, és a jelminőség megőrzése is megfelelő. A projekt során szerzett tapasztalatok alapján fontos, hogy a tervezési folyamat során figyelembe vegyük a komponensek toleranciáját és a környezeti hatásokat, mivel ezek jelentős hatással lehetnek az áramkör teljesítményére.

### Aláírás:
Felelős mérő személy: ..............................
Dátum: 2024.11.13 
