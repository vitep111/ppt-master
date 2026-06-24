---
layout_id: shana-ci
kind: layout
summary: SHANA project official slide structure — cover, section divider, content, and ending templates rebuilt from the real SHANA deck (theme XML + slide layouts).
canvas_format: ppt169
page_count: 4
page_types: [cover, divider, content, ending]
---

# SHANA CI Layout Specification

> Structure preset, extracted from the official SHANA deck (`theme1.xml` + slide layouts 1/5/8). Best used alongside `templates/brands/shana-ci/`. All geometry below is in the 1280×720 canvas (slide is 13.33"×7.5", 16:9).

---

## I. Template Overview

| Property | Value |
|---|---|
| Template Name | shana-ci |
| Use Cases | Change impact analysis, workstream deliverables, milestone sign-off, PMO reviews, stakeholder briefs |
| Design Tone | Corporate, structured; navy + cyan + teal on photo-textured white canvas |
| Theme Mode | Light — full-bleed gradient/dot-wave backgrounds with white content zones |

---

## II. Canvas Specification

| Property | Value |
|---|---|
| Format | 16:9 |
| Dimensions | 1280 × 720 px (12192000 × 6858000 EMU) |
| viewBox | `0 0 1280 720` |
| Safe Area (content) | x: 60–1220, y: 112–668 |

---

## III. Typography (from theme fontScheme)

| Role | Family | Weight | Size | Color |
|---|---|---|---|---|
| cover title | Helvetica Neue | Bold | 42pt | #1B1164 |
| section title (divider) | Helvetica Neue | Bold | 48pt | #1B1164 |
| content page title | Helvetica Neue | Bold | 28pt | #1B1164 |
| sub-heading | Helvetica Neue | Bold | 14pt | #1B1164 |
| body | Helvetica | Regular | 14–16pt | #000000 |
| KPI figure | Helvetica Neue | Bold | 32pt | #1B1164 |
| footer | Helvetica Neue | Regular | 8pt | #000000 |
| page number | Helvetica Neue | Regular | 10pt | #000000 |

Font stack: `'Helvetica Neue', Helvetica, Arial, sans-serif`

---

## IV. Color Scheme (theme clrScheme)

| Role | HEX | Use |
|---|---|---|
| Navy (accent1) | #1B1164 | titles, headings, logo, strong text |
| Cyan (accent3) | #00AEEF | accent bars, table headers, links |
| Teal (accent5) | #3BBF92 | dividers, "to-be" highlights |
| Mid-blue (accent2) | #2A6FA0 | secondary data, subtitles |
| Lavender (accent4) | #D1CCF4 | soft fills, chart tints |
| Amber (accent6) | #F4A261 | alerts, high-impact emphasis |
| Muted (dk2) | #5E5E5E | captions, secondary text |
| Border (lt2) | #D5D5D5 | gridlines, separators |
| Risk red | #C00000 | removed/decommissioned systems |
| Add green | #92D050 | new/added systems |

---

## V. Page Types & Geometry

### 1. Cover (01_cover.svg) — from layout1
- Background: `images/bg_cover.jpeg`
- Logo lockup top-left, larger: PTTEP `x=0 y=2 255×66` · DigitalX `x=319 y=0 193×85` · SHANA **gradient** `x=510 y=12 254×48`
- Title: box `x=138 y=268 w=1078`, 42pt bold navy
- Subtitle (optional): mid-blue 22pt
- Date: box `x=138 y=555`, 18pt
- Footer: centered, 8pt

### 2. Section Divider (02_divider.svg) — from layout5
- Background: `images/bg_divider.jpeg` (alt: `images/bg_section.png` for full saturated + white text)
- Logo lockup top-left, navy: PTTEP `x=0 y=0 154×40` · DigitalX `x=193 y=2 108×48` · SHANA **navy** `x=312 y=5 167×32`
- Giant section number: box `x=120 y=178 w=846 h=230`, 230px bold navy at 12% opacity (watermark)
- Section title: box `x=120 y=408`, 48pt bold navy + teal underline
- Page number: bottom-right `x≈1215 y=697`

### 3. Content (03_content.svg) — from layout8
- Background: `images/bg_content.jpeg`
- Logo lockup top-left, navy (same coords as divider)
- Page title: box `x=60 y=51`, 28pt bold navy + cyan hairline underline at y=100
- Optional cyan topic tag pill (commented in SVG)
- Content area: `x=60–1220, y=112–668` — filled freely by Executor
- Footer: copyright `x=778 y=697` 8pt · page number `x=1215 y=697` right-aligned

### 4. Ending (04_ending.svg)
- Background: `images/bg_thankyou.jpeg`
- Logo lockup top-left, navy
- Centered closing title 56pt navy + teal rule + tagline + cyan contact line
- Footer: centered 8pt

---

## VI. SVG Page Roster

| File | Role | Background |
|---|---|---|
| `01_cover.svg` | cover | bg_cover.jpeg |
| `02_divider.svg` | divider | bg_divider.jpeg |
| `03_content.svg` | content | bg_content.jpeg |
| `04_ending.svg` | ending | bg_thankyou.jpeg |

Additional background available: `images/bg_section.png` (full cyan-blue gradient + green dots, for TOC / saturated section pages with white text).

---

## VII. Logo Lockup Rules

Order is always **PTTEP | DigitalX | SHANA** (left → right), positioned **top-left** on every slide.

| Slide | Variant of SHANA |
|---|---|
| Cover | gradient (`logo_shana_gradient.png`) |
| Divider / Content / Ending | navy (`logo_shana_navy.png`) |

Logo files: `logo_pttep.png` · `logo_digitalx.png` · `logo_shana_gradient.png` · `logo_shana_navy.png` · `logo_shana_navy_flat.png`

Never recolor or reorder. Cover uses the larger lockup; all other slides use the compact lockup.

---

## VIII. Table Component

| Row | Fill | Text |
|---|---|---|
| Header | `#00AEEF` | White, Helvetica Neue Bold 12–13pt |
| Body even | `#FFFFFF` | #000000, Helvetica 10–13pt |
| Body odd | `#F5F5F5` | #000000 |
| Borders | `#D5D5D5` 1px | — |

Straight edges (rx=0), per corporate style.

---

## IX. Signature Content Patterns (observed in source deck)

| Pattern | Description |
|---|---|
| As-is / To-be split | Two columns; left = current systems, right = future. Arrows show system migration (e.g. `E-Payment → SAP Concur`). Removed systems in red #C00000, new in green #92D050. |
| 3-up stat columns | KPI figure (32pt navy) + label, separated by vertical #D5D5D5 lines, with charts. |
| Impact-area icon grid | People / Process / Tech / Data / Document — filled 512px icons; grey out areas with no impact. |
| Impact severity badges | High = amber #F4A261; Medium/Low = cyan/teal. |
| Change-action ticks | Tick icons instead of text for change actions. |

---

## X. SVG Technical Constraints

1. viewBox `0 0 1280 720`
2. Backgrounds full-bleed: `<image href="images/bg_*" preserveAspectRatio="xMidYMid slice"/>`
3. Logos: `<image href="logo_*.png" preserveAspectRatio="xMinYMid meet"/>`
4. `fill-opacity` / `stroke-opacity` only — never `rgba()`
5. Prohibited: `mask`, `<style>`, `class`, `foreignObject`; `clipPath` only as `<image>` wrapper
6. No group opacity — set per child element
7. Text wrap via `<tspan>`; inline styles only

---

## XI. Placeholder Reference

| Placeholder | Slide | Description |
|---|---|---|
| `{{TITLE}}` | cover | Main title |
| `{{SUBTITLE}}` | cover | Subtitle / workstream |
| `{{DATE}}` | cover | Date |
| `{{YEAR}}` | all | Copyright year |
| `{{SECTION_NUM}}` | divider | Big watermark number |
| `{{SECTION_TITLE}}` | divider | Section heading |
| `{{PAGE_TITLE}}` | content | Page title |
| `{{SECTION_TAG}}` | content | Optional cyan topic pill |
| `{{PAGE_NUM}}` | content, divider | Slide number |
| `{{CLOSING_TITLE}}` | ending | Closing message (default "Thank You") |
| `{{TAGLINE}}` | ending | Tagline |
| `{{CONTACT}}` | ending | Contact / URL |

---

## XII. Usage

```
Create a CIA deck using:
  skills/ppt-master/templates/brands/shana-ci/
  skills/ppt-master/templates/layouts/shana-ci/
```

Step 3 fuses them: brand wins on color / typography / logo / voice; this spec wins on canvas / page structure / SVG roster.
