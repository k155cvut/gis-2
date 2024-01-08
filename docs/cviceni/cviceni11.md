---
icon: custom/vc-numeric-11-box
title: Cvičení 11
---

# Skriptování v ArcGIS Pro

## Cíl cvičení

Probloubení znalostí vytváření skriptů v jazyku Python pro platformu ArcGIS Pro.

## Základní pojmy

- **Registrace skriptu v ArcGIS Pro**

<figure markdown>
![CO](../assets/cviceni11/arcgis_skript.png "Registrace skriptu v prostředí ArcGIS Pro"){ width="500" }
    <figcaption>Registrace skriptu v prostředí ArcGIS Pro</figcaption>
</figure>

- **PyCharm**

<figure markdown>
![CO](../assets/cviceni11/pycharm_skript.png "Spuštění skriptu v prostředí Pycharm"){ width="500" }
    <figcaption>Spuštění skriptu v prostředí Pycharm</figcaption>
</figure>

Zvolte cestu k Python interpretu odkazující na ArcGIS: ``C:\Program
Files\ArcGIS\Pro\bin\Python\envs\arcgispro-py3\python.exe``

## Použité datové podklady

- [ArcČR 500](../../data/#arccr-500)

## Náplň cvičení

### Ukázka vytvoření skriptu

Navážeme na znalosti ArcPy:

```py
arcpy.env.workspace = r"C:\users\martin\Documents\GIS2"

# vyber a export dalnic
silnice = r"S:\K155\Public\data\ArcGIS\ArcCR500 3.3\ArcCR500_v33.gdb\Silnice_2015"
dalnice = "dalnice.shp"
arcpy.analysis.Select(silnice, dalnice, "TRIDA = 1")

# buffer kolem dalnic
buffer_dal = "dalnice_buf.shp"
vzdalenost = "5000 meters"
arcpy.analysis.Buffer(dalnice, buffer_dal, vzdalenost, dissolve_option="ALL")

# odstraneni nepotrebnych vrstev
arcpy.management.Delete(dalnice)
```

Dokumentace:

* [Select](https://pro.arcgis.com/en/pro-app/latest/tool-reference/analysis/select.htm)
* [Buffer](https://pro.arcgis.com/en/pro-app/latest/tool-reference/analysis/buffer.htm)
* [Delete](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/delete.htm)

Úkoly:

- Zprovozněte výpočet v Jupyter Notebooku
- Přepište do formy skriptu a registrujte jej v prostředí ArcGISu (New -> Script)

### Práce s rastrovými daty pomocí Numpy

```py
dmt =  r"S:\K155\Public\data\ArcGIS\ArcCR500 3.3\ArcCR500_v33.gdb\DigitalniModelReliefu"

# otestovat nacteni dat
data = arcpy.Describe(dmt)
data.dataType

# nacteni metadat rastru
raster = arcpy.Raster(dmt)
raster.width, raster.height

# nacteni rastrovych hodnot do numpy pole
array = arcpy.RasterToNumPyArray(raster)
type(array)

# rozmer a datovy typ pole
array.shape, array.dtype

# zjisteni minimalni, maximalni hodnoty
array.min(), array.max()

# nastaveni no-data hodnoty
array = arcpy.RasterToNumPyArray(raster, nodata_to_value=-1)
array.min(), array.max()

# cetnost hodnot
unique, counts = numpy.unique(array, return_counts=True)
idx = numpy.where(unique == 200)
counts[idx]

# ukazka mapove algebry
array[(array>=0) & (array<=200)] = 0
array[(array>200)] = 1
numpy.unique(array, return_counts=True)

# zapis numpy pole do rastru
vystup = arcpy.NumPyArrayToRaster(array, value_to_nodata=-1)
vystup.save(r"C:\users\martin\Documents\dmt200.tif")
```

Dokumentace:

- [NumPy](https://numpy.org/)
* [Working with NumPy in ArcGIS](https://pro.arcgis.com/en/pro-app/latest/arcpy/get-started/working-with-numpy-in-arcgis.htm)

### Modul ArcGIS

Dokumentace:

- [ArcGIS API for Python](https://developers.arcgis.com/python/guide/using-the-api/)
- [ArcGIS GIS module](https://developers.arcgis.com/python/api-reference/arcgis.gis.toc.html)
- [Documentation and samples for ArcGIS API for Python](https://github.com/Esri/arcgis-python-api)

#### Inicializujeme mapového okna

```py
import arcgis
gis = arcgis.GIS()

map1 = gis.map()
map1
```

#### Vykreslíme výchozí podkladové mapy v novém mapovém okně

```py
map2 = gis.map(location='Prague, Czech Republic', zoomlevel = 12)
map2
```

#### Vyhledáme online vrstev podle klíčového slova

```py
from IPython.display import display

items = gis.content.search('Praha', item_type="Feature Layer", outside_org=True)
print(len(items))
for item in items[:3]:
    display(item)
```

#### Přídáme vybrané onlive vrstvy do mapového okna

```py
layer = items[0].layers[0]
map2.add_layer(layer)
map2.zoom_to_layer(layer)
```

#### Na závěr vyzkoušíme integraci s knihovnou Pandas:

```py
import pandas
okresy = pandas.DataFrame.spatial.from_featureclass(r"S:\K155\Public\data\ArcGIS\ArcCR500 3.3\AdministrativniCleneni_v13.gdb\OkresyPolygony")
okresy.spatial.plot(map_widget=map1)
map1
```

## Zadání domácího úkolu k semestrální práci

Další ukázky skriptů [zde](https://geo.fsv.cvut.cz/vyuka/155gis2/cviceni/10/arcpy-ulohy/).
