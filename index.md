/* =========================================================
   BD Emission Inventory — stylesheet
   Minimal academic look: cover-style header, single column,
   quiet palette, restrained cards/tables.
   ========================================================= */

@import url('https://fonts.googleapis.com/css2?family=Lora:wght@500;600;700&family=Inter:wght@400;500;600&display=swap');

:root {
  --ink:      #24292a;
  --navy:     #1f2d3a;
  --muted:    #6b6f72;
  --paper:    #ffffff;
  --paper-2:  #f6f5f2;
  --line:     #e4e2dc;
  --accent:   #7a5c3e;
  --good-bg:  #eaf1e6; --good-fg: #2f6d33;
  --warn-bg:  #f7f0df; --warn-fg: #8a6a1e;
  --bad-bg:   #f5e7e4;  --bad-fg: #99402f;
  --radius: 6px;
}

/* ===== Base ===== */
* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Inter', Arial, Helvetica, sans-serif;
  color: var(--ink);
  line-height: 1.7;
  background: var(--paper);
}

a { color: var(--navy); text-decoration: underline; text-decoration-color: var(--line); text-underline-offset: 2px; }
a:hover { color: var(--accent); text-decoration-color: var(--accent); }

.page {
  max-width: 720px;
  margin: 0 auto;
  padding: 48px 24px 80px;
}

h1, h2, h3 {
  font-family: 'Lora', Georgia, serif;
  color: var(--navy);
}

h1 { font-size: 28px; font-weight: 600; margin-bottom: 8px; }
h2 {
  font-size: 19px;
  font-weight: 600;
  margin: 40px 0 12px;
  padding-bottom: 8px;
  border-bottom: 1px solid var(--line);
}
h3 { font-size: 15px; font-weight: 600; margin: 18px 0 8px; color: var(--ink); }

p { margin-bottom: 12px; color: #3c3c3a; }
ul, ol { margin: 0 0 12px 22px; }
strong { color: var(--navy); }

/* ===== Header — two-tier gov-style bar ===== */
header.site-header {
  background: var(--navy);
  padding: 0;
}

.header-inner {
  max-width: 960px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  padding: 20px 24px;
}

.header-inner h1 {
  color: #fdfcf9;
  font-size: 22px;
  font-weight: 700;
  margin: 0;
  letter-spacing: 0;
  font-family: 'Inter', Arial, sans-serif;
}

/* second, darker nav strip — full width */
.header-links {
  flex: 1 0 100%;
  display: flex;
  gap: 28px;
  flex-wrap: wrap;
  background: #16283a;
  margin: 0 -24px;
  padding: 12px 24px;
}

.header-links a {
  color: #fdfcf9;
  text-decoration: none;
  font-size: 14px;
  font-weight: 700;
  font-family: 'Lora', Georgia, serif;
  border: none;
  padding: 0;
  border-radius: 0;
}

.header-links a:hover {
  color: var(--accent);
  text-decoration: underline;
}

/* ===== Sector grid (index page) ===== */
.sector-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
  gap: 10px;
  margin: 14px 0 20px;
}

.sector-card {
  display: block;
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 14px 16px;
  text-decoration: none;
  color: var(--ink);
  background: var(--paper);
  transition: border-color 0.15s, background 0.15s;
}

.sector-card:hover {
  border-color: var(--accent);
  background: var(--paper-2);
}

.sector-card .sector-name {
  font-family: 'Lora', Georgia, serif;
  font-weight: 600;
  color: var(--navy);
  margin-bottom: 2px;
}

.sector-card .sector-code {
  font-size: 12px;
  color: var(--muted);
}

/* ===== Table ===== */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 12px 0 20px;
  font-size: 14px;
}

th, td {
  border-bottom: 1px solid var(--line);
  padding: 9px 10px;
  text-align: left;
}

th {
  color: var(--navy);
  font-weight: 600;
  font-size: 12.5px;
  text-transform: uppercase;
  letter-spacing: 0.03em;
  border-bottom: 2px solid var(--navy);
}

/* ===== Stats row ===== */
.stats-row {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 10px;
  margin: 14px 0 24px;
}

.stat-box {
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 12px 14px;
  background: var(--paper-2);
}

.stat-box .stat-label {
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  color: var(--muted);
}

.stat-box .stat-value {
  font-family: 'Lora', Georgia, serif;
  font-size: 20px;
  font-weight: 600;
  color: var(--navy);
}

/* ===== Status badges ===== */
.status {
  display: inline-block;
  padding: 2px 9px;
  border-radius: 3px;
  font-size: 12px;
  font-weight: 600;
}
.status.complete  { background: var(--good-bg); color: var(--good-fg); }
.status.progress  { background: var(--warn-bg); color: var(--warn-fg); }
.status.notstarted{ background: var(--bad-bg);  color: var(--bad-fg); }

/* ===== Tabs ===== */
.tabs {
  display: flex;
  flex-wrap: wrap;
  border-bottom: 1px solid var(--line);
  margin-top: 10px;
}

.tab-btn {
  background: none;
  border: none;
  border-bottom: 2px solid transparent;
  padding: 9px 14px;
  font-size: 14px;
  font-family: inherit;
  cursor: pointer;
  color: var(--muted);
}

.tab-btn:hover { color: var(--navy); }

.tab-btn.active {
  color: var(--navy);
  border-bottom-color: var(--accent);
  font-weight: 600;
}

.tab-panel { display: none; padding: 18px 0; }
.tab-panel.active { display: block; }

/* ===== Map box ===== */
.map-box {
  border: 1px dashed #c7c3b8;
  border-radius: var(--radius);
  background: var(--paper-2);
  min-height: 300px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: var(--muted);
  padding: 20px;
  overflow: hidden;
}

.map-box video, .map-box img {
  width: 100%;
  height: 100%;
  border-radius: 4px;
}

/* ===== Footer ===== */
footer.site-footer {
  border-top: 1px solid var(--line);
  text-align: center;
  font-size: 12px;
  color: var(--muted);
  padding: 26px 20px;
}

/* ===== Misc ===== */
.back-link {
  display: inline-block;
  margin-bottom: 14px;
  font-size: 13px;
}
.muted { color: var(--muted); font-size: 13px; }
.download-list { list-style: none; margin-left: 0; }
.download-list li {
  padding: 7px 0;
  border-bottom: 1px solid var(--line);
}
