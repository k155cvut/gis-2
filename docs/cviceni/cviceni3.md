---
icon: material/numeric-3-box
title: Cvičení 3
---

# Zpracování LAS

## Cíl cvičení
Zpracování LiDARových dat v prostředí ArcGIS Pro včetně představení možností jejich symbologie a následného využití v GIS analýzách.

## Základní pojmy
- **LiDAR** – metoda dálkového měření vzdálenosti na základě výpočtu doby šíření pulsu laserového paprsku odraženého od snímaného objektu

- **[LAS](https://pro.arcgis.com/en/pro-app/3.1/help/data/las-dataset/las-dataset-in-arcgis-pro.htm)** – datový formát mračna bodů (point cloud) získaných laserovým skenováním

## Použité datové podklady
- [DMR 5G](../../data/#dmr-5g)

- [ortofoto ČÚZK](https://ags.cuzk.cz/arcgis1/rest/services/ORTOFOTO/MapServer)

## Náplň cvičení

### Stažení dat z ČÚZK
Z [Geoportálu ČÚZK](https://ags.cuzk.cz/geoprohlizec/) lze stáhnout data laserového skenování (mračno bodů) pro Česko. Získání dat DMR 5G, DMR 4G či DMP 1G lze provést přes výběr daného podkladu v záložce *Produkty*. Dále po rozkliknutí ikony tří teček příslušné vrstvy v záložce *Seznam vrstev* je možné vybrat buď možnost   *Exportovat data* nebo *Stáhnout data (předpřipravené jednotky)*.

???+ note "&nbsp;<span style="color:#448aff">Možnosti stažení laserových dat z ČÚZK</span>"
     - **Exportovat data** – Touto možností lze data zaslat přímo na email. Zároveň je takto možné stáhnout více kladů dat najednou vlastním výběrem (nakreslením polygonu či nahráním vlastní vrstvy k výběru). Stažená data jsou ve formátu *LAS*.

     - **Stáhnout data (předpřipravené jednotky)** – Takto lze data stáhnout postupně dle předpřipravených kladů. Stažená data jsou ve formátu *LAZ*.

### Převod LAZ do LAS
**1.** Jestliže získáme data ve formátu *ZLAS* nebo *LAZ*, je nutné mračno bodů v ArcGIS Pro konvertovat do formátu *LAS* pomocí funkce [*Convert LAS*](https://pro.arcgis.com/en/pro-app/latest/tool-reference/conversion/convert-las.htm). Takto převedná data již dokáže ArcGIS načíst.

**2.** Do parametru *Input LAS* vložíme z disku vstupní soubor, který chceme převést. Zvolíme adresář výstupních dat *Target Folder* a případně nastavíme parametry převodu.

**3.** Ve druhé části funkce určíme souřadnicový systém mračna bodů. 

<figure markdown>
  ![Convert LAS](../assets/cviceni3/convert_las.png "Convert LAS")
  <figcaption>Hodnoty funkce Convert LAS</figcaption>
</figure>

### Vizualizace LAS
**1.** LAS data je možné zobrazit 2D v mapě nebo 3D ve scéně (ideálně v lokální scéně). Novou scénu vytvoříme v záložce *Insert* – *New Map* – *New Local Scene*.

<figure markdown>
  ![Porovnání mapy a scény](../assets/cviceni3/map_sc.png "Porovnání mapy a scény"){ width="900"}
  <figcaption>Porovnání zobrazení LAS dat ve 2D mapě (vlevo) a ve 3D scéně (vpravo)</figcaption>
</figure>

**2.** Různé možnosti vizualizace LAS jsou dostupné po vybrání vrstvy mračna bodů v záložce *LAS Dataset Layer*. Pod ikonou *Symbology* 

<figure markdown>
  ![Symbologie LAS](../assets/cviceni3/las_s.png "Symbologie LAS"){ width="900"}
  <figcaption>Symbologie LAS</figcaption>
</figure>

**3.** Výše zmíněné možnosti symbologie se dělí na tři typy: Vizualizace dle bodů, terénem či liniově. Bodové vizualizace nabízejí zobrazení barvy mračna bodů na základě jeho nadmořské výšky (*Elevation*) nebo klasifikace dat (*Class*). Mračno bodů je dále možné symbolizovat jako terén, přičemž barva může být určená nadmořskou výškou (*Elevation*), sklonem terénu (*Slope*) nebo sklonem ke světové straně (*Aspect*). Třetí možnost, vizualizace vrstvy pomocí linií, nabízí zobrazení vrstevnic (*Contour*) a hran (*Edges*).

### Obarvení LAS


### Vytvoření digitálního modelu terénu
