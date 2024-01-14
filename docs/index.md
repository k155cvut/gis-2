
# GIS 2 {: .page_title}

Předmět navazující na [předchozí kurz](https://k155cvut.github.io/gis-1/ "GIS 1 (1551GIS)") představuje hlubší ponoření do světa geografických informačních systémů. Zaměřuje se na pokročilejší dovednosti v manipulaci s __rastrovými daty__, __interpolaci__, __rastrovou algebru__ nebo __tvorbu digitálních modelů terénu__. Pokračuje úvodem do __vzdálenostních__ a __síťových analýz__, které pomáhají nacházet nejkratší a nejlevnější cesty mezi lokacemi s využitím tzv. rastru nákladů. Opět je využíván především program __:simple-arcgis: ArcGIS Pro__, nicméně pestrosti přidá i zmínka o podobných procesech ve free programu __:simple-qgis: QGIS__.

Kurz vrcholí seznámením s __ArcPy__, knihovnou Pythonu systému ArcGIS, která posouvá __automatizaci GIS úloh__ na ještě vyšší úroveň. Vytvářením vlastních skriptů se student stává __expertem pro efektivní manipulaci a analýzu prostorových dat__.

Kombinací teoretických znalostí a praktických dovedností dává předmět GIS 2 studentům široký obraz o možnostech a aplikacích geografických informačních systémů ve skutečném prostředí.


Naučíte se
{: align=center style="font-size: 1.25rem; font-weight: bold; margin-bottom: 10px;"}

<div class="grid_container" markdown>
<div class="grid_item grid_item_flex" markdown>
:material-cog-counterclockwise:
{: .icon_important}

využívat __automatizační nástroje__ GIS, spouštět __hromadné analýzy__
</div>
<div class="grid_item grid_item_flex" markdown>
:material-thumb-up:
{: .icon_important}

nacházet __nejvhodnější místa__ na základě překryvné analýzy
</div>
<div class="grid_item grid_item_flex" markdown>
:material-grid:
{: .icon_important}

__pokročilou práci s rastry__ – reklasifikaci, interpolaci, tvorbu DMT
</div>
<div class="grid_item grid_item_flex" markdown>
:fontawesome-solid-magnifying-glass-dollar:
{: .icon_important}

pomocí rastru nákladů __nacházet nejlevnější cestu__ mezi body
</div>
<div class="grid_item grid_item_flex" markdown>
:fontawesome-solid-code-branch:
{: .icon_important}

__analyzovat dopravní sítě__ pomocí síťových analyzačních nástrojů
</div>
<div class="grid_item grid_item_flex" markdown>
:material-language-python:
{: .icon_important}

implementovat nástroje GIS do jazyka __Python__
</div>
</div>





<div class="gallery_container" markdown>
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/01.png){: .no-filter .off-glb }
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/02.jpg){: .no-filter .off-glb }
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/03.png){: .no-filter .off-glb }
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/04.png){: .no-filter .off-glb }
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/05.jpg){: .no-filter .off-glb }
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/06.png){: .no-filter .off-glb }
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/07.png){: .no-filter .off-glb }
![](https://geo.fsv.cvut.cz/data/cehak/MkDocs/gis-2/index/08.png){: .no-filter .off-glb }
</div>

## Doporučená literatura

1. Kolář, J.: Geografické informační systémy 10. Vydavatelství ČVUT, Praha 1998.
2. Rapant, P. (2006): Geoinformatika a geoinformační technologie. VŠB-TU Ostrava, 500 str. ISBN 80-248-1264-9.
3. Břehovský, M., Jedlička, K. (2005): Přednáškové texty pro Úvod do GIS. ZČU Plzeň, 116 s.
4. Hrubý M.: Geografické Informační Systémy (GIS) - Studijní opora. VÚT v Brně, 91 str.
5. Tuček J.: Geografické informační systémy, Praha Computer Press, 1998.

## Přednášky {: style="margin-bottom:0;"}

účast doporučená
{: style="opacity:50%;margin-top:0;"}

<!-- Přednášející:  -->![](https://geomatics.fsv.cvut.cz/wp-content/uploads/2022/01/03-edit_export@0.5x-2.jpg){: .off-glb .no-filter style="height: 1.5em; vertical-align: -.4em; clip-path: circle();"} 
__prof. Ing. Lena Halounová, CSc.__

1. GeoWeb, Web 3.0, normy, terminologie
2. Mapová algebra, globální, lokální zonální, fokální statistika, NULL data
3. Reklasifikace, měření vzdálenosti, obalová zóna v rastru, povrchy nákladů, nejlevnější cesta
4. Parametry povrchu terénu, křivost, časová řada v povrchu terénu
5. Interpolace a extrapolace 2D
6. Voronoiovy polygony, Delauneyovy trojúhelníky, 3D lokálních odhady v prostoru, IDW
7. Lokální výběr bodů, RBF, izoline. Geostatistika - semivariogram
8. Empirický a teoretický semivariogram, kriging, příklady, interpolace spliny
9. Analytická geometrie pro GIS
10. Statistický popis prostorových bodových dat
11. Průzkumová analýza bodových dat - EDA, Q-Q graf, outliers
12. Statistický popis prostorových liniových a plošných dat
13. Úvod do teorie grafů, aplikace grafů v síťové analýze, optimalizační úlohy

## Harmonogram {: style="margin-bottom:0;"}

odkaz pro připojení kalendáře: [:material-calendar-month:](https://outlook.office365.com/owa/calendar/4aa3e6ac783f4ae6bbcf3a50e0e59f01@fsv.cvut.cz/496c9f7d60b0483a8fb5d920d636374b16197507547842865833/calendar.ics){: .md-button .md-button--primary .button_smaller }
{: style="color:#aaa;margin-top:0;"}

<iframe src="https://outlook.office365.com/owa/calendar/4aa3e6ac783f4ae6bbcf3a50e0e59f01@fsv.cvut.cz/496c9f7d60b0483a8fb5d920d636374b16197507547842865833/calendar.html" style="border: 0" width="100%" height="600" frameborder="0" scrolling=“no”></iframe>


<!-- <iframe src="https://calendar.google.com/calendar/embed?height=600&wkst=2&bgcolor=%23ffffff&ctz=Europe%2FPrague&showTitle=1&showTz=0&showCalendars=0&showTabs=0&showPrint=0&showDate=1&showNav=1&title=155GIS1%3A%20GIS%201&src=dHFhajdoNWRiaHFhdjNvbXE2bTRib3I0YTg5dWVkMGRAaW1wb3J0LmNhbGVuZGFyLmdvb2dsZS5jb20&color=%23D50000" style="border-width:0" width="100%" height="600" frameborder="0" scrolling="no"></iframe> -->


<br><br><br>

