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
- Ellenállások:
  - R3 = 11,92 kΩ
  - R4 = 1,5 kΩ
- Ni myDAQ 

## Számítások
<img src="https://github.com/oroszszr/jegyzokonyv/blob/main/meres1/falstad1.PNG" width="300" height="170">  

### Csillapítás Kiszámítása

A csillapítást a következő képlettel számolhatjuk ki:  
$$A = 20 \cdot \log_{10}\left(\frac{V_{out}}{V_{in}}\right)$$  

### Megadott Értékek:
- $V_{out} = 6.657 \, \text{mV} = 0.006657 \, \text{V}$  
- $V_{in} = 7.496 \, \text{mV} = 0.007496 \, \text{V}$  

### Kiszámítási Lépések:
1. **Hányados Számítása:**
   $$\frac{0.006657}{0.007496} \approx 0.887$$  

2. **Logaritmus Számítása:**
   $$\log_{10}(0.887) \approx -0.053$$  

3. **Csillapítás Kiszámítása:**
   $$A \approx 20 \cdot (-0.053) \approx -1.06 \, \text{dB}$$

Tehát a csillapítás körülbelül **-1.06 dB**

### Százalékos Csillapítás Kiszámítása:
A százalékos csillapítást a következő képlettel számolhatjuk ki:  
$$\text{Csillapítás (\%)} = \left(1 - \frac{V_{out}}{V_{in}}\right) \times 100$$  

Ez alapján a csillapítás körülbelül **11.3%**.

### A kapcsolási rajz ábrázolja a Ni myDAQ a belső ellenállásával, valamint a Pi csillapítót a kiszámolt ellenállás értékekkel:

<img src="https://github.com/oroszszr/jegyzokonyv/blob/main/meres1/falstad.PNG" width="770" height="400">

## Mérési eredmények

### Bemeneti és Kimeneti Impedancia
- **Bemeneti Impedancia:** [Írd be az értéket] Ω
- **Kimeneti Impedancia:** [Írd be az értéket] Ω

### Csillapítás
- **Csillapítás (dB):** -1.06 dB
- **Csillapítás (%):** 11.3%


