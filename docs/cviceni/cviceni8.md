---
icon: material/numeric-8-box
title: Cvičení 8
---

# Síťové analýzy

Ve cvičení se naučíte TBA TBA
{: align=center style="font-size: 1.25rem; font-weight: bold; margin-bottom: 10px;"}

<style>
    .smaller_padding li {padding:.4rem .8rem !important;}
    .primary_color {color:var(--md-primary-fg-color);}
</style>

<div class="grid cards smaller_padding" markdown>

-   :material-map-marker-distance:{ .xxxl .middle }
    {.middle style="display:table-cell;min-width:40px;padding-right:.8rem;"}
    
    že "__jak daleko od sebe__{: .primary_colorx}" znamená mnohem více než počet kilometrů mezi místy na mapě
    {.middle style="display:table-cell;line-height:normal;"}

-   :material-graph-outline:{ .xxxl .middle }
    {.middle style="display:table-cell;min-width:40px;padding-right:.8rem;"}

    jak lze analýzou vzdáleností vytvořit sofistikovanější __modely blízkých a vzdálených míst__{: .primary_colorx}
    {.middle style="display:table-cell;line-height:normal;"}

-   :material-nature-people-outline:{ .xxxl .middle }
    {.middle style="display:table-cell;min-width:40px;padding-right:.8rem;"}

    jak aplikovat koncepty analýzy vzdáleností k zodpovězení __reálných otázek__ týkajících se pohybu v krajině
    {.middle style="display:table-cell;line-height:normal;"}

</div>

## Cíl cvičení

## Základní pojmy

## Použité datové podklady

## Náplň cvičení
Síťová analýza v geografických informačních systémech umožňuje řešit různé otázky spojené s propojením bodů v prostoru pomocí sítě. Narozdíl od vzdálenostních analýz pracujeme s vektorovými daty (resp. používáme tzv. __Network dataset__{: .primary_color})

Některé z hlavních otázek, které lze pomocí síťové analýzy v GIS řešit, zahrnují:

<style>
    .nt-cards.center_align {text-align: center; }
    .nt-card {border-radius: .1rem;}
</style>

<!-- https://www.neoteroi.dev/mkdocs-plugins/cards/ -->
::cards:: cols=3 class_name="center_align"

- title: Nejkratší cesta
  content: Jak najít __nejkratší__ nebo __optimální trasu__ mezi __dvěma body__ na síti?<br><br><br><em class="primary_color no_dec"><span class="twemoji"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M11 15H6l7-14v8h5l-7 14v-8Z"></path></svg></span>například</em>
   plánování tras, doručování zásilek, optimalizace přepravy
  image: ../assets/cviceni8/Best_route.png

- title: Optimalizace tras
  content: Jak __optimalizovat trasu__ při navštěvování __více bodů__ s omezeními jako jsou čas, vzdálenost nebo priorita návštěvy?<br><br><em class="primary_color no_dec"><span class="twemoji"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M11 15H6l7-14v8h5l-7 14v-8Z"></path></svg></span> například</em>
   kurýrní služby, sběr dat nebo technická údržba
  image: ../assets/cviceni8/Planning_routes.png

- title: Analýza dosažitelnosti
  content: Jaké __oblasti jsou dosažitelné z daného bodu__ v určitém časovém nebo vzdálenostním limitu?<br><br><br><em class="primary_color no_dec"><span class="twemoji"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M11 15H6l7-14v8h5l-7 14v-8Z"></path></svg></span> například</em>
   stanovení oblastí pokrytých konkrétním bodem (např. služby, nemocnice)
  image: ../assets/cviceni8/Service_areas.png

- title: Nejbližší středisko obsluhy
  content: Hledá cestu mezi místem (*Incident*) a servisními středisky (*Facilities*), resp. určuje __nejsnáze dosažitelné středisko__ vzhledem k místu incidentu.<br><br><em class="primary_color no_dec"><span class="twemoji"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M11 15H6l7-14v8h5l-7 14v-8Z"></path></svg></span> například</em>
   nejbližší hasičské stanice, které zasahují při požáru
  image: ../assets/cviceni8/Fire.png

::/cards::

<style>
  .no_dec { font-weight: unset; /* in case of using __content__ (double underscore) */
            font-style: unset;  /* in case of using  _content_  (single underscore) */ }
</style>

<hr class="level-1">


## Zadání domácího úkolu k semestrální práci