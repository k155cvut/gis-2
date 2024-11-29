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

Cílem je používat data přímo od jejich poskytovatelů. Pro okrajové případy a případ technických problémů je ale připraven balíček již připravených dat.
- [data](https://geo.fsv.cvut.cz/vyuka/155gis2/cviceni/8/data.zip)

Přehled dat, které budeme používat:

- [Velkoplošná zvláště chráněná území](https://data.nature.cz/ds/3)  plošné vymezení chráněných oblastí. Data lze načítat přímo ze "ZIP", ale pro další zpracování se doporučuje data rozbalit do pracovního adresáře.
- rastrová data DMT 100x100m generalizovaná za účelem ukázky

## Náplň cvičení

Jako podpůrný materiál budeme používat školící materiály [QGIS pro
začátečníky](https://gismentors.github.io/qgis-zacatecnik) a [QGIS pro pokročilé](https://gismentors.github.io/qgis-pokrocily/) skupiny
[GISMentors](https://gismentors.cz).

### Opakování základního ovládání a práce v QGIS

 
V panelu "Prohlížeč" si najdeme pracovní adresář se staženými daty. Dataset lze načít například "přetažením" datasetu  do mapového okna nebo do panelu vrstev. Načtená data je dobré zkontrolovat, zda se používá sprváný [souřadnicový systém](https://gismentors.github.io/qgis-zacatecnik/intro/import_export.html#vyber-souradnicoveho-systemu).

Vrstvě nastavíme kategorizovanou symbologii podle atributu "KAT".

Základní nástroje jako například obalová zóna jsou k dipozici v horním textovém menu v položce "Vektor", konkrétně obalová zóna je zařazena "Vektor"->"Nástroje geoprocessingu"->"Obalová zóna...". Pracovně si  vygenerujeme obalovou zónu o velikosti 1000m sloučenou pro všechny prvky - "rozpuštěnou".

### Nástoje zpracování

Podklady:

- [Nástroje zpracování](https://gismentors.github.io/qgis-pokrocily/geoprocessing/index.html)

Menu "Nástroje zpracování" obsahuje širokou nabídku jak základních nástrojů, tak i mnoho dalších možností. Například možnost generování obalové zóny v mnohých variantách. Nástroj "Obalová zóna vektorové vrstvy" ze skupiny GDAL nám umožní rozpustit obalové zóny podle atributu.

Vygenerujeme obalovou zónu vrstvy VZCHU o velikosti 1000 m a parametr pro rozpuštění dle atributu nastavíme na atribut "KAT".

V symbologii nastavíme částečně průhlednou barvu. Díky překryvu původní kategorizované sybologie a pokročilé obalové zóny si umíme jednoduše zkontrolovat správnost funkcionality.

Načteme vrstvu DMT, ořežeme podle velkoplošných chráněných území - nástroj "Rastr"->"Extrakce"->"Oříznout rastr podle vrstvy masky". Zároveň použijeme nástroj pro iteraci, který nám vytvoří samostatný výstup pro každý prvek chráněného území.

"Otázka"
Jaký postup by bylo nutné zvolit, aby správce každého území dostal ořezaný rastr svého území spolu s ochranným pásmem?

Další možností je používat nástroje v módu "Dávkové zpracování". Otevřeme nástroj "Obalová zóna vektorové vrstvy" ze skupiny GDAL a pomocí tlačítka "Spustit jako dávkový proces..." se otevře nastavení pro nastavení v řádkovém zápisu. Nastavíme veliksot bufferu na 3km, a rozpuštění podle atributu "KAT". 
Přidáme další 2 řádky, které vyplníme pouze s rozdílem velikosti obalové zóny na 6km a 10km.
V posledním sloupečku se nastavuje způsob výstupu. Přes talčítko lze zvolit výstupní soubor, kam zadáme název výstupního GPKG. Náseldně se dialog zeptá na automatickou výplň, kde zvolíme "Vyplnit hodnotami parametru" a vybereme "Vzdálenost obalové zóny". Doporučujeme manuálně upravit na hodnotu bez desetinného místa. 
Nevýhodou je, že nelze jednoduše uložit do jednoho GPKG jako vícero vrstev.
Zaškrtneme "Načíst vrstvy po dokončení".

Veškeré nastavení je v processingovém menu možné upravit. Rovněž je k dispozici historie procesů, odkud lze jednotlivý proces opakovaně spustit se všemi parametry.

### Grafický modelář

Podklady:

- [Grafický modelář](https://gismentors.github.io/qgis-pokrocily/modeler/index.html)

V tomto prostředí je možné sestavit řetězec algoritmů, které zpracovávají data a ten pak spouštět jako samostatný proces. Jako ukázku si zkusíme sestavit jednoduchý model.

1. Vytvoříme nový model
2. Nastavíme vlastnosti modelu (název, skupina), model uložíme do souboru.
3. Přidáme vstupní parametr typu číslo s popisem "počet bodů", vstup bude celočíselný.
4. Přidáme vstupní parametr typu Rozsah. Díky překladu jsou tam 2 stejné hodnoty, použijeme druhý parametr s popisem "rozsah". Jedná se o parametr typu "Extent".
5. Přidáme algoritmy (náhodné body v rozsahu). Počet bodů a rozsah provážeme se vstupními parametry z bodu 3. a 4. Nastavíme výstup pro kontrolu.
7. Model spusttíme a zkontrolujeme zda se výstup generuje dle zadání.
8. Model upravíme - přídáme vstupní parametr typu číslo pro zadání velikosti obalové zóny. Popis nastavíme jako "velikost obalové zóny" a nastavíme číslo jako desetinné. Výchozí hodnotu nastavíme jako 1000 (metrů).
9. Model upravíme - přídáme algoritmus pro obalovou zónu, která vygeneruje obalovou zónu dle zadané velikosti z vygenerovaných bodů.
10. Model spustíme
11. Upravíme nápovědu modelu
12. Model exportujeme do skriptu
13. Vyzkoušíme spustít model z panelu nástrojů zpracování

## Zadání domácího úkolu k semestrální práci

Vytvořte model pro první část cvičení (Nástoje zpracování).
