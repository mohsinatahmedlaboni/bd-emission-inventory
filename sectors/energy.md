---
layout: none
title: Energy Sector
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

<div class="page">

  <a class="back-link" href="{{ '/' | relative_url }}">&larr; All Sectors</a>

  <h1>Energy Sector</h1>
  <p class="muted">IPCC Category 1 &middot; Base year 2023 (edit as applicable)</p>

  <p style="margin-top:16px;">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla ligula enim, dictum sed arcu in, vestibulum euismod quam. Integer laoreet non dolor id dapibus. Quisque lobortis fringilla tincidunt. Duis purus libero, viverra ultricies mi nec, fringilla volutpat augue. Phasellus eget magna quis ex interdum sagittis et at risus. Aliquam posuere mattis leo. Mauris gravida diam eget dolor aliquam porta. Donec magna metus, viverra eu ante nec, gravida convallis ipsum. Nunc tincidunt enim nec lorem dictum, sed sagittis ex interdum. Phasellus eu vehicula neque. 
  </p>

  <div class="stats-row">
    <div class="stat-box">
      <div class="stat-label">Total CO₂e (Gg)</div>
      <div class="stat-value">—</div>
    </div>
    <div class="stat-box">
      <div class="stat-label">Sub-categories</div>
      <div class="stat-value">5</div>
    </div>
    <div class="stat-box">
      <div class="stat-label">Base Year</div>
      <div class="stat-value">2023</div>
    </div>
    <div class="stat-box">
      <div class="stat-label">Status</div>
      <div class="stat-value"><span class="status progress">In Progress</span></div>
    </div>
  </div>

  <!-- ===== Tabs ===== -->
  <div class="tabs">
    <button class="tab-btn active" data-tab="dataset">Emission Dataset</button>
    <button class="tab-btn" data-tab="methodology">Methodology Report</button>
    <button class="tab-btn" data-tab="map">Map</button>
    <button class="tab-btn" data-tab="literature">Literature Review</button>
  </div>

  <!-- Dataset -->
  <div class="tab-panel active" id="dataset">
    <h3>Excel Workbooks</h3>
    <ul class="download-list">
      <li><a href="{{ '/data/energy_1A1_2023.xlsx' | relative_url }}">energy_1A1_2023.xlsx</a> — Energy industries combustion calculations</li>
      <li><a href="{{ '/data/energy_1A3_2023.xlsx' | relative_url }}">energy_1A3_2023.xlsx</a> — Transport sector calculations</li>
    </ul>

    <h3>Results Summary</h3>
    <table>
      <tr><th>Sub-category</th><th>CO₂ (Gg)</th><th>CH₄ (Gg)</th><th>N₂O (Gg)</th></tr>
      <tr><td>1A1 Energy Industries</td><td>—</td><td>—</td><td>—</td></tr>
      <tr><td>1A2 Manufacturing &amp; Construction</td><td>—</td><td>—</td><td>—</td></tr>
      <tr><td>1A3 Transport</td><td>—</td><td>—</td><td>—</td></tr>
      <tr><td>1A4 Other Sectors</td><td>—</td><td>—</td><td>—</td></tr>
      <tr><td>1B Fugitive Emissions</td><td>—</td><td>—</td><td>—</td></tr>
    </table>
    <p class="muted">Fill in results as each sub-category is finalized. Full calculations are in the linked Excel files, or see the <a href="{{ '/sectors/energy/calculations.html' | relative_url }}">full Calculations &amp; Results page</a>.</p>
  </div>

  <!-- Methodology -->
  <div class="tab-panel" id="methodology">
    <h3>Approach by Sub-category</h3>
    <table>
      <tr><th>Sub-category</th><th>Tier</th><th>EF Source</th><th>Activity Data Source</th></tr>
      <tr><td>1A1 Energy Industries</td><td>Tier 1</td><td>IPCC 2006 default</td><td>BPDB Annual Report</td></tr>
      <tr><td>1A3 Transport</td><td>Tier 2</td><td>Country-specific (see Literature)</td><td>BRTA vehicle registration data</td></tr>
    </table>

    <h3>Key Methodological Decisions</h3>
    <ul>
      <li>Note any decision, e.g. why Tier 1 was used for 1A1 despite Tier 2 being available.</li>
      <li>Note how activity data gaps for any year were filled (interpolation, proxy data, etc.)</li>
    </ul>

    <h3>Deviations From Default Guidance</h3>
    <p>Note any places your approach diverges from the guidebook and why.</p>

    <p class="muted">See also the <a href="{{ '/methodology.html' | relative_url }}">overall cross-sector methodology</a>, or the full <a href="{{ '/sectors/energy/methodology.html' | relative_url }}">Energy Methodology page</a> for QA/QC and uncertainty approach.</p>
  </div>

  <!-- Map -->
  <div class="tab-panel" id="map">
    <h3>Spatial Reference (GIS)</h3>
    <p class="muted">
      A facility/source-level map for this sector will be added here, similar in spirit to the
      <a href="https://environmentalintegrity.org/state-emissions-inventory/" target="_blank" rel="noopener">Environmental Integrity Project's state emissions inventory map</a>
      — clickable/hoverable spatial data linking to underlying source information.
    </p>
    <div class="map-box">
      <!-- Replace this block with a <video> or <iframe> embed once available, e.g.:
      <video controls>
        <source src="{{ '/assets/energy_map_demo.mp4' | relative_url }}" type="video/mp4">
      </video>
      -->
      GIS map coming soon
    </div>
  </div>

  <!-- Literature -->
  <div class="tab-panel" id="literature">
    <h3>Papers &amp; Guidebooks Used for Emission Factors / Assumptions</h3>
    <table>
      <tr><th>Citation</th><th>Used For</th><th>Key Takeaway</th></tr>
      <tr><td>IPCC 2006 Guidelines, Vol. 2, Ch. 2</td><td>Default EFs</td><td>Tier 1 EFs for stationary combustion</td></tr>
      <tr><td>Author et al. (Year), Journal</td><td>Country-specific EF, natural gas</td><td>EF X% lower than IPCC default due to [reason]</td></tr>
    </table>

    <h3>Key Assumptions Derived From Literature</h3>
    <ul>
      <li>e.g. Oxidation factor assumed 0.99 for natural gas — per IPCC 2006 Vol. 2, Table 2.5.</li>
    </ul>

    <p class="muted">See also the <a href="{{ '/sectors/energy/literature.html' | relative_url }}">full Literature Review page</a> or the sector-wide <a href="{{ '/emission-factors.html' | relative_url }}">Emission Factors &amp; Guidebooks</a> page.</p>
  </div>

</div>

{% include footer.html %}

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

</body>
</html>
