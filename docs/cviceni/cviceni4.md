# Souř. připojení prostorových dat (práce s externími daty Excel, CSV), join

## Cíl cvičení

## Základní pojmy

- [**slope**](https://pro.arcgis.com/en/pro-app/latest/tool-reference/3d-analyst/slope.htm)
- [**aspect**](https://pro.arcgis.com/en/pro-app/latest/tool-reference/3d-analyst/aspect.htm)
- [**hillshade**](https://pro.arcgis.com/en/pro-app/latest/tool-reference/3d-analyst/hillshade.htm)
- [**raster surface toolset**](https://pro.arcgis.com/en/pro-app/latest/tool-reference/3d-analyst/an-overview-of-the-raster-surface-toolset.htm)
- [**aspect-slope**](https://pro.arcgis.com/en/pro-app/latest/help/analysis/raster-functions/aspect-slope-function.htm)


## Náplň cvičení
Vaším úkolem bude na základě rastrových dat vybraného území analyzovat, které svahy mají předpoklady být lavinového rázu. K vyhodnocení lavinového svahu potřebujete znát sklonitost a expozici svahu, nadmořskou výšku či krajinný pokryv. Podmínky pro vznik lavin lze tedy shrnout v následujících bodech:

1. Nadmořská výška
Laviny se zpravidla vyskytují ve vyšších nadmořských výškách. Jako území vhodné pro vznik lavin volte lokality, které se nachází v nejvyšší třetině všech nadmořských výšek v rámci zájmového území.

2. Sklon svahu
Základní předpoklad pro uvolnění laviny je sklon svahu, s jehož růstem se zvyšuje pravděpodobnost a riziko vzniku lavin. Laviny suchého sněhu vzácně vznikají na svazích již od 25° sklonu a se vzrůstajícím sklonem jejich četnost narůstá, zejména ve svazích nad 30° sklonu. Pro účely práce tedy zvolte mezní hodnotu v tomto intervalu.

3. Expozice svahu
Uprostřed zimy bývají kritické zejména stinné svahy v severní expozici.

4. Krajinný pokryv
Riziko vzniku lavin nastává na otevřených plochách bez většího vegetačního porostu. Hodnoty krajinného pokryvu jsou obsaženy ve sloupci *Code 18* (CLC 2018). Vyhovujícími hodnotami jsou 2.X.X a 3.X.X. (vyjma 3.1.1., 3.1.2 a 3.1.3.).

## Použité datové podklady
- DMR5G
- CORINE Land Cover 2018

## Zadání domácího úkolu k semestrální práci
