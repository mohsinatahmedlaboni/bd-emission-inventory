# Sector Template — How to Replicate

This is the template for **one sector** (Energy). To add another sector (e.g. Agriculture):

1. Copy `sectors/energy.md` → `sectors/agriculture.md`, edit content.
2. Copy the whole `sectors/energy/` folder → `sectors/agriculture/`, rename nothing (keep `calculations.md`, `sources.md`, `literature.md`, `methodology.md`).
3. Update the "Back to [Sector]" link at the top of each sub-page (should point to `/sectors/agriculture.html`).
4. Update file paths under `data/` to match the new sector's Excel files.
5. Add the new sector to the homepage (`index.md`) sector list.

## Site-wide header/footer

The header and footer are now defined once in `_includes/header.html` and `_includes/footer.html`,
and pulled into every page with `{% include header.html %}` / `{% include footer.html %}`.
To change the site title, nav links, or badge, edit `_includes/header.html` only — it updates everywhere.

## Every page needs this front matter at minimum

```
---
layout: none
title: Page Title
---
```

`layout: none` is important — without it, your theme's default layout may wrap its own header/footer
around the page, which is likely what caused the "messy" duplicated/unstyled look before.

## Internal links

Jekyll converts `.md` files to `.html` on build. Always link to `.html`, never `.md`:

- ✅ `<a href="{{ '/sectors/energy.html' | relative_url }}">Energy</a>`
- ❌ `<a href="../energy.md">Energy</a>`

Using `{{ '...' | relative_url }}` instead of hardcoded relative paths (`../../`) avoids broken links
if a page ever moves to a different folder depth.

## Suggested full repo structure

```
/
  _config.yml
  _includes/
    header.html
    footer.html
  index.md              → homepage, links to all sectors
  methodology.md        → cross-sector methodology (QA/QC, tiers, uncertainty)
  references.md         → master bibliography across all sectors
  emission-factors.md   → consolidated EF lookup table across all sectors
  /sectors
    energy.md
    agriculture.md
    ippu.md
    lulucf.md
    waste.md
    /energy
      calculations.md
      sources.md
      literature.md
      methodology.md
    /agriculture
      ... (same 4 files)
    ...
  /data
    energy_1A1_2023.xlsx
    agriculture_*.xlsx
    ...
  /assets
    style.css
  /references            (optional — PDFs you have rights to host)
```

## Status emoji legend (used in sector status tables)
- 🟢 Complete
- 🟡 In progress
- 🔴 Not started
