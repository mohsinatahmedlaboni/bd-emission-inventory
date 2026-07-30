---
layout: none
title: Home
---
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>{{ page.title }} – Bangladesh National Emission Inventory</title>
<link rel="stylesheet" href="{{ '/assets/style.css' | relative_url }}"/>
</head>
<body>

{% include header.html %}

<div class="page" markdown="1">

## What Is This Project

This project develops a national emission inventory for Bangladesh. 

### What Is Calculated

- Emissions of CO, PM2.5, PM10, NMVOC, SOx, NOx by sector and sub-category

### Data Sources

Activity data and emission factors are drawn from Bangladesh government reports and databases (e.g. BBS, BPDB, DoE), peer-reviewed literature for country-specific emission factors and assumptions, and US EPA/Indian EF/EEA/EMAP guidebooks for default methods and factors. A full, sector-wise reference list is maintained on each sector's Literature Review tab, with a combined [Emission Factors & Guidebooks](emission-factors.html) page listing every EF source used across the inventory.

## About This Site

This site is a VERY DEMO version of nothing for now.

## Sectors

<div class="sector-grid" markdown="0">
  <a class="sector-card" href="{{ '/sectors/energy.html' | relative_url }}">
    <div class="sector-name">Energy</div>
    <div class="sector-code">IPCC Category 1</div>
  </a>
  <a class="sector-card" href="{{ '/sectors/Transport.html' | relative_url }}">
    <div class="sector-name">Transport</div>
    <div class="sector-code">IPCC Category 2</div>
  </a>
  <a class="sector-card" href="{{ '/sectors/agriculture.html' | relative_url }}">
    <div class="sector-name">Agriculture</div>
    <div class="sector-code">IPCC Category 3</div>
  </a>
</div>

## Other Resources

- [Emission Factors & Inventory Guidebooks](emission-factors.html) — all EF sources used across the inventory, in one place
- [Overall Methodology](methodology.html) — cross-sector approach, QA/QC, uncertainty
- [Master Reference List](references.html) — full bibliography

</div>

{% include footer.html %}

</body>
</html>
