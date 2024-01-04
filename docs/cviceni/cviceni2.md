---
icon: material/numeric-2-box
title: Cvičení 2
---

# Tvorba digitálního modelu terénu + hydrologická analýza

## Cíl cvičení
Představení tvorby digitálního modelu reliéfu pomocí GIS.

- představení cuzk geoprohlizece vyskopisu

- tvorba TIN z vrstevnic

- terrain dataset, související datové vrsrvy

- tvorba dmt pomocí model builderu

- topo to raster

## Základní pojmy
- **DMT (digitální model terénu)** – digitální reprezentace prostorových objektů (obecný pojem obsahující různé způsoby vyjádření terénního reiéfu nebo povrchu)
- **DMR (digitální model reliéfu)** – digitální reprezentace zemského povrchu (NEbsahuje vegetaci, lidské stavby)
- **DMP (digitální model povrchu)** – digitální reprezentace zemského povrchu (obsahuje vegetaci, lidské stavby, které jsou pevně spojené s reliéfem)
- [**TIN**](https://pro.arcgis.com/en/pro-app/3.1/help/data/tin/tin-in-arcgis-pro.htm) – trojúhelníková nepravidelná síť

???+ note "&nbsp;<span style="color:#448aff">Digitální modely terénu České republiky</span>"
     - **DMP 1G** – Digitální model povrchu České republiky 1. generace (DMP 1G) představuje zobrazení území včetně staveb a rostlinného pokryvu ve formě nepravidelné sítě výškových bodů (TIN) s úplnou střední chybou výšky **0,4 m** pro přesně vymezené objekty (budovy) a **0,7 m** pro objekty přesně neohraničené (lesy a další prvky rostlinného pokryvu). Model vznikl z dat pořízených metodou leteckého laserového skenování výškopisu území České republiky v letech 2009 až 2013. 
     - **DMR 4G** – Digitální model reliéfu České republiky 4. generace (DMR 4G) představuje zobrazení přirozeného nebo lidskou činností upraveného zemského povrchu v digitálním tvaru ve formě výšek diskrétních bodů v pravidelné síti (5 x 5 m) bodů o souřadnicích X,Y,H, kde H reprezentuje nadmořskou výšku ve výškovém referenčním systému Balt po vyrovnání (Bpv) s úplnou střední chybou výšky **0,3 m** v odkrytém terénu a **1 m** v zalesněném terénu. Model vznikl z dat pořízených metodou leteckého laserového skenování výškopisu území České republiky v letech 2009 až 2013.
     - **DMR 5G** – Digitální model reliéfu České republiky 5. generace (DMR 5G) představuje zobrazení přirozeného nebo lidskou činností upraveného zemského povrchu v digitálním tvaru ve formě výšek diskrétních bodů v nepravidelné trojúhelníkové síti (TIN) bodů o souřadnicích X,Y,H, kde H reprezentuje nadmořskou výšku ve výškovém referenčním systému Balt po vyrovnání (Bpv) s úplnou střední chybou výšky **0,18 m** v odkrytém terénu a **0,3 m** v zalesněném terénu. Model vznikl z dat pořízených metodou leteckého laserového skenování výškopisu území České republiky v letech 2009 až 2013. Dokončen byl k 30. 6. 2016 na celém území ČR. 

## Aplikace Analýzy výškopisu 
Pro analýzu výškopisu ve webovém prostředí slouží mapová aplikace Analýzy výškopisu od Českého úřadu zeměměřického a katastrálního. Aplikace umožňuje provádějí základních výškových analýz nad daty DMP 1G, DMR 4G a DMR 5G. Pro každou datovou sadu nabízí několik rastrových funkcí (Stínovaný reliéf, Z-faktor apod.). Do rozhraní je možné přidat i vlastní data, a tedy zefektivnit používání aplikace v reálné praxi.

[<span></span>https://ags.cuzk.cz/av/<br>Analýzy výškopisu ČÚZK](https://ags.cuzk.cz/av/){ .md-button .md-button--primary .button_larger .external_link_icon target="_blank"}
{: .button_array}

<figure markdown>
  ![Analýzy výškopisu](../assets/cviceni5/av_cuzk.png "Analýza pole viditelnosti ze zadaného bodu vypočteného nad DMR 5G"){ width="900"}
  <figcaption>Analýza pole viditelnosti ze zadaného bodu vypočteného nad DMR 5G</figcaption>
</figure>

## Použité datové podklady

## Náplň cvičení

## Postup
