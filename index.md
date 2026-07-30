---
title: Home
---
<link rel="stylesheet" href="{{ '/assets/style.css' | relative_url }}"/>

<header class="site-header">
  <div class="header-inner">
    <h1>Bangladesh National Emission Inventory</h1>
    <div class="header-links">
      <a href="https://github.com/mohsinatahmedlaboni/bd-emission-inventory" target="_blank">View on GitHub</a>
    </div>
  </div>
</header>

<div class="page">

## What Is This Project

A national emission inventory is a structured, sector-wise accounting of greenhouse gas (GHG) and air pollutant emissions released within a country over a given period, typically a calendar year. It is the foundation for national GHG reporting (e.g. to the UNFCCC), climate policy planning, and air quality management.

This project develops a national emission inventory for Bangladesh, covering the five standard IPCC sectors: Energy, Industrial Processes and Product Use (IPPU), Agriculture, Forestry and Other Land Use (LULUCF), and Waste. Emissions are calculated following the **2006 IPCC Guidelines for National Greenhouse Gas Inventories** (edit if using 2019 Refinement or a different guidebook), using a combination of Tier 1 and Tier 2 methods depending on data availability per sector.

### What Is Calculated

- Emissions of CO₂, CH₄, and N₂O (and other gases as applicable) by sector and sub-category
- Activity data compiled from national statistics, government reports, and international databases
- Emission factors sourced from IPCC default values and, where available, country-specific studies
- Results expressed in Gg and CO₂-equivalent (CO₂e) using standard Global Warming Potentials

### Data Sources

Activity data and emission factors are drawn from Bangladesh government reports and databases (e.g. BBS, BPDB, DoE), international databases (e.g. IEA, FAOSTAT), peer-reviewed literature for country-specific emission factors and assumptions, and IPCC guidebooks for default methods and factors. A full, sector-wise reference list is maintained on each sector's Literature Review tab, with a combined [Emission Factors & Guidebooks](emission-factors.html) page listing every EF source used across the inventory.

## About This Site

This site is a working, presentable version of the inventory — organized by sector so that calculations, data sources, methodology, and supporting literature can be reviewed independently for each sector. Click into any sector below to see its dataset, methodology report, a spatial reference map (in progress), and literature review.

## Sectors

<div class="sector-grid">
  <a class="sector-card" href="sectors/energy.html">
    <div class="sector-name">Energy</div>
    <div class="sector-code">IPCC Category 1</div>
  </a>
  <a class="sector-card" href="sectors/ippu.html">
    <div class="sector-name">IPPU</div>
    <div class="sector-code">IPCC Category 2</div>
  </a>
  <a class="sector-card" href="sectors/agriculture.html">
    <div class="sector-name">Agriculture</div>
    <div class="sector-code">IPCC Category 3</div>
  </a>
  <a class="sector-card" href="sectors/lulucf.html">
    <div class="sector-name">LULUCF</div>
    <div class="sector-code">IPCC Category 3 (Land)</div>
  </a>
  <a class="sector-card" href="sectors/waste.html">
    <div class="sector-name">Waste</div>
    <div class="sector-code">IPCC Category 4</div>
  </a>
</div>

## Other Resources

- [Emission Factors & Inventory Guidebooks](emission-factors.html) — all EF sources used across the inventory, in one place
- [Overall Methodology](methodology.html) — cross-sector approach, QA/QC, uncertainty
- [Master Reference List](references.html) — full bibliography

</div>

<footer class="site-footer">Bangladesh National Emission Inventory &middot; Maintained by Mohsinat Ahmed Laboni</footer>
