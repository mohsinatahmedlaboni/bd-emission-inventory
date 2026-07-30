---
layout: none
---

<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Bangladesh National Emission Inventory</title>
<link rel="stylesheet" href="assets/style.css"/>
</head>
<body>

<header class="site-header">
  <div class="header-inner">
    <h1>Bangladesh National Emission Inventory</h1>
    <div class="header-links">
      <a href="https://github.com/mohsinatahmedlaboni/bd-emission-inventory" target="_blank">View on GitHub</a>
      <a href="https://mohsinatahmedlaboni.github.io" target="_blank">Back to Portfolio</a>
    </div>
  </div>
</header>

<div class="page">

  <h2 style="margin-top:0;">What Is This Project</h2>
  <p>
    A national emission inventory is a structured, sector-wise accounting of greenhouse gas (GHG) and air
    pollutant emissions released within a country over a given period, typically a calendar year. It is the
    foundation for national GHG reporting (e.g. to the UNFCCC), climate policy planning, and air quality
    management.
  </p>
  <p>
    This project develops a national emission inventory for Bangladesh, covering the five standard IPCC
    sectors: Energy, Industrial Processes and Product Use (IPPU), Agriculture, Forestry and Other Land Use
    (LULUCF), and Waste. Emissions are calculated following the <strong>2006 IPCC Guidelines for National
    Greenhouse Gas Inventories</strong> (edit if using 2019 Refinement or a different guidebook), using a
    combination of Tier 1 and Tier 2 methods depending on data availability per sector.
  </p>

  <h3>What Is Calculated</h3>
  <ul>
    <li>Emissions of CO₂, CH₄, and N₂O (and other gases as applicable) by sector and sub-category</li>
    <li>Activity data compiled from national statistics, government reports, and international databases</li>
    <li>Emission factors sourced from IPCC default values and, where available, country-specific studies</li>
    <li>Results expressed in Gg and CO₂-equivalent (CO₂e) using standard Global Warming Potentials</li>
  </ul>

  <h3>Data Sources</h3>
  <p>
    Activity data and emission factors are drawn from Bangladesh government reports and databases (e.g.
    BBS, BPDB, DoE), international databases (e.g. IEA, FAOSTAT), peer-reviewed literature for
    country-specific emission factors and assumptions, and IPCC guidebooks for default methods and factors.
    A full, sector-wise reference list is maintained on each sector's Literature Review tab, with a combined
    <a href="emission-factors.html">Emission Factors &amp; Guidebooks</a> page listing every EF source used
    across the inventory.
  </p>

  <h2>About This Site</h2>
  <p>
    This site is a working, presentable version of the inventory — organized by sector so that calculations,
    data sources, methodology, and supporting literature can be reviewed independently for each sector. Click
    into any sector below to see its dataset, methodology report, a spatial reference map (in progress), and
    literature review.
  </p>

  <h2>Sectors</h2>
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

  <h2>Other Resources</h2>
  <ul>
    <li><a href="emission-factors.html">Emission Factors &amp; Inventory Guidebooks</a> — all EF sources used across the inventory, in one place</li>
    <li><a href="methodology.html">Overall Methodology</a> — cross-sector approach, QA/QC, uncertainty</li>
    <li><a href="references.html">Master Reference List</a> — full bibliography</li>
  </ul>

</div>

<footer class="site-footer">Bangladesh National Emission Inventory &middot; Maintained by Mohsinat Ahmed Laboni</footer>

</body>
</html>
