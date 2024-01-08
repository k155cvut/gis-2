---
icon: material/numeric-9-box
title: Cvičení 9
---

# Výpočetní nástroje QGIS

## Cíl cvičení

Probloubení znalostí platformy QGIS a jeho výpočetních nástrojů.

## Základní pojmy

- [**QGIS**](https://qgis.org) – svobodný a multiplatformní geografický informační systém (GIS)
    - [**Nástroje zpracování**](https://gismentors.github.io/qgis-pokrocily/geoprocessing/index.html)
    - [**Grafický modelář**](https://gismentors.github.io/qgis-pokrocily/modeler/index.html)

## Použité datové podklady

- [data](https://geo.fsv.cvut.cz/vyuka/155gis2/cviceni/8/data.zip)

## Náplň cvičení

Jako podpůrný materiál budeme používat školící materiály [QGIS pro
začátečníky](https://gismentors.github.io/qgis-zacatecnik) a [QGIS pro pokročilé](https://gismentors.github.io/qgis-pokrocily/) skupiny
[GISMentors](https://gismentors.cz).

### Nástoje zpracování

1. Načteme velkoplošná chráněná území a nastavíme souřadnicový systém
2. Vytvoříme obalovou zónu (z menu) - s/bez dissolve
3. Vyzkoušíme variabilní obalovou zónu
4. Načteme DMT, ořežeme podle velkoplošných chráněných území
5. Vyzkoušíme možnost iterace pro každé chraněné území samostatně
6. Použijeme nástroje zpracování, obalová zóna (GDAL, rozpustit podle atributu)
7. Spočítáme obalová zóna (QGIS), spustit jako dávkový proces (3, 6, 10km)
8. Prozkoumáme další možnosti nástrojů zpracování - možnosti (obecné, poskytovatelé, ...), historie

### Grafický modelář

1. Vytvoříme model (generování náhodných bodů)
2. Nastavíme vlastnosti modelu (název, skupina)
3. Nastavíme Vstupy (počet bodů, rozsah)
4. Přidáme algoritmy (náhodné body v rozsahu), provázat vstupy a výstupy
5. Model spusttíme
6. Model upravíme - přídáme obalovou zónu, změníme výsledek, přidáme vstup velikosti zóny
7. Model spustíme
8. Upravíme nápovědu modelu
9. Model exportujeme do skriptu
10. Vyzkoušíme spustít model z panelu nástrojů zpracování

## Zadání domácího úkolu k semestrální práci

Vytvořte model pro první část cvičení (Nástoje zpracování).
