---
title: Energy Sector
---
<link rel="stylesheet" href="{{ '/assets/style.css' | relative_url }}"/>

<header class="site-header">
  <div class="header-inner">
    <h1>Bangladesh National Emission Inventory</h1>
    <div class="header-links">
      <a href="https://github.com/mohsinatahmedlaboni/bd-emission-inventory" target="_blank">View on GitHub</a>
      <a href="{{ '/' | relative_url }}">Home</a>
    </div>
  </div>
</header>

<div class="page">

<a class="back-link" href="{{ '/' | relative_url }}">&larr; All Sectors</a>

# Energy Sector
<p class="muted">IPCC Category 1 &middot; Base year 2023 (edit as applicable)</p>

The Energy sector covers greenhouse gas emissions from fuel combustion and fugitive emissions across energy industries, manufacturing and construction, transport, and other stationary/mobile sources. Emissions are calculated for electricity and heat generation, industrial fuel use, road and other transport, and residential/commercial fuel combustion, following IPCC 1A and 1B categories.

<div class="stats-row">
  <div class="stat-box"><div class="stat-label">Total CO₂e (Gg)</div><div class="stat-value">—</div></div>
  <div class="stat-box"><div class="stat-label">Sub-categories</div><div class="stat-value">5</div></div>
  <div class="stat-box"><div class="stat-label">Base Year</div><div class="stat-value">2023</div></div>
  <div class="stat-box"><div class="stat-label">Status</div><div class="stat-value"><span class="status progress">In Progress</span></div></div>
</div>

<div class="tabs">
  <button class="tab-btn active" data-tab="dataset">Emission Dataset</button>
  <button class="tab-btn" data-tab="methodology">Methodology Report</button>
  <button class="tab-btn" data-tab="map">Map</button>
  <button class="tab-btn" data-tab="literature">Literature Review</button>
</div>

<div class="tab-panel active" id="dataset" markdown="1">

### Excel Workbooks

- [energy_1A1_2023.xlsx](../data/energy_1A1_2023.xlsx) — Energy industries combustion calculations
- [energy_1A3_2023.xlsx](../data/energy_1A3_2023.xlsx) — Transport sector calculations

### Results Summary

| Sub-category | CO₂ (Gg) | CH₄ (Gg) | N₂O (Gg) |
|---|---|---|---|
| 1A1 Energy Industries | — | — | — |
| 1A2 Manufacturing & Construction | — | — | — |
| 1A3 Transport | — | — | — |
| 1A4 Other Sectors | — | — | — |
| 1B Fugitive Emissions | — | — | — |

<p class="muted">Fill in results as each sub-category is finalized. Full calculations are in the linked Excel files.</p>

</div>

<div class="tab-panel" id="methodology" markdown="1">

### Approach by Sub-category

| Sub-category | Tier | EF Source | Activity Data Source |
|---|---|---|---|
| 1A1 Energy Industries | Tier 1 | IPCC 2006 default | BPDB Annual Report |
| 1A3 Transport | Tier 2 | Country-specific (see Literature) | BRTA vehicle registration data |

### Key Methodological Decisions

- Note any decision, e.g. why Tier 1 was used for 1A1 despite Tier 2 being available.
- Note how activity data gaps for any year were filled (interpolation, proxy data, etc.)

### Deviations From Default Guidance

Note any places your approach diverges from the guidebook and why.

<p class="muted">See also the <a href="{{ '/methodology.html' | relative_url }}">overall cross-sector methodology</a> for QA/QC and uncertainty approach.</p>

</div>

<div class="tab-panel" id="map" markdown="1">

### Spatial Reference (GIS)

<p class="muted">A facility/source-level map for this sector will be added here, similar in spirit to the <a href="https://environmentalintegrity.org/state-emissions-inventory/" target="_blank">Environmental Integrity Project's state emissions inventory map</a> — clickable/hoverable spatial data linking to underlying source information.</p>

<div class="map-box">
<!-- Replace this block with a video or iframe embed once available, e.g.:
<video controls>
  <source src="../assets/energy_map_demo.mp4" type="video/mp4">
</video>
-->
GIS map coming soon
</div>

</div>

<div class="tab-panel" id="literature" markdown="1">

### Papers & Guidebooks Used for Emission Factors / Assumptions

| Citation | Used For | Key Takeaway |
|---|---|---|
| IPCC 2006 Guidelines, Vol. 2, Ch. 2 | Default EFs | Tier 1 EFs for stationary combustion |
| Author et al. (Year), Journal | Country-specific EF, natural gas | EF X% lower than IPCC default due to [reason] |

### Key Assumptions Derived From Literature

- e.g. Oxidation factor assumed 0.99 for natural gas — per IPCC 2006 Vol. 2, Table 2.5.

<p class="muted">See also the sector-wide <a href="{{ '/emission-factors.html' | relative_url }}">Emission Factors &amp; Guidebooks</a> page.</p>

</div>

</div>

<footer class="site-footer">Bangladesh National Emission Inventory &middot; Maintained by Mohsinat Ahmed Laboni</footer>

<script>
  document.querySelectorAll('.tab-btn').forEach(function(btn) {
    btn.addEventListener('click', function() {
      document.querySelectorAll('.tab-btn').forEach(function(b) { b.classList.remove('active'); });
      document.querySelectorAll('.tab-panel').forEach(function(p) { p.classList.remove('active'); });
      btn.classList.add('active');
      document.getElementById(btn.dataset.tab).classList.add('active');
    });
  });
</script>
