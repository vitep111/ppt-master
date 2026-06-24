---
layout_id: shana-ci
kind: layout
summary: SHANA project official slide structure — cover, section divider, content, and ending templates with POTX-sourced background images.
canvas_format: ppt169
page_count: 4
page_types: [cover, divider, content, ending]
---

# SHANA CI Layout Specification

> Structure preset. Best used alongside `templates/brands/shana-ci/` (brand wins on identity tokens; this spec wins on page structure). May also be used standalone — all background images and logos are self-contained.

---

## I. Template Overview

| Property | Value |
|---|---|
| Template Name | shana-ci |
| Use Cases | Project status updates, workstream deliverables, PMO reviews, stakeholder briefs, internal reports — any PTTEP / PTTEP DigitalX / SHANA branded deck |
| Design Tone | Corporate, polished; energetic navy-cyan-teal accent palette on a clean photo-textured white canvas |
| Theme Mode | Light (white content area + navy/cyan/teal accents) with full-bleed JPEG/PNG texture backgrounds |

---

## II. Canvas Specification

| Property | Value |
|---|---|
| Format | 16:9 standard |
| Dimensions | 1280 × 720 px |
| viewBox | `0 0 1280 720` |
| Safe Area (content) | x: 40–1240, y: 80–690 |

---

## III. Page Structure

### Content Slide Zone Map

| Zone | y-range | Height | Purpose |
|---|---|---|---|
| Top accent strip | 0–3 | 3 px | Navy #1B1164 brand anchor |
| Header | 3–72 | 69 px | Section tag + page title left · Logo lockup right |
| Header separator | 72–74 | 2 px | Cyan #00AEEF divider |
| Content area | 74–690 | 616 px | Free — Executor fills with text, tables, charts, cards |
| Footer separator | 690–691 | 1 px | Grey #D5D5D5 hairline |
| Footer | 691–720 | 29 px | Copyright notice left · Page number right |

### Decorative System

Background images carry all texture; SVG-drawn decoration is deliberately minimal:

| Element | Description | Color |
|---|---|---|
| Top accent strip | 3–4 px rect across full width | Navy or Cyan (slide-type specific) |
| Header left accent bar | 5 px wide vertical rect beside title (cover only) | Navy #1B1164 |
| Cyan tag pill | rx=3 rounded rect for section tag text | Cyan #00AEEF fill, white text |
| Header separator | 2 px horizontal line | Cyan #00AEEF |
| Left bar highlight | 4 px rect beside active agenda item (divider only) | Cyan #00AEEF |
| Teal underline | 3 px horizontal line under section title | Teal #3BBF92 |

---

## IV. Page Types

### 1. Cover (01_cover.svg)

- Background: `images/bg_cover.jpeg` full-bleed (light left, vivid cyan-blue right)
- Top accent: 4 px **cyan** (#00AEEF) strip
- **Logo lockup — top-left** (larger): PTTEP | DigitalX | SHANA, navy variants, H=48 px, x=40 y=16
- **Title block — left-center** (x=60–720, y=240–510):
  - Navy left accent bar: x=60, y=248, 5×130 px
  - Title: x=82, baseline y=318, 42 pt bold navy
  - Subtitle: x=82, baseline y=366, 24 pt light navy
  - Cyan accent line: x=82, y=382, w=380, h=2
  - Phase / workstream: x=82, baseline y=410, 15 pt cyan
  - Date: x=82, baseline y=438, 15 pt dark
- Footer: copyright only (no page number), grey italic 8 pt, x=40 y=708

### 2. Section Divider (02_divider.svg)

- Background: `images/bg_divider.png` full-bleed (left: green-cyan gradient + wave dots; right: solid navy-blue)
- Top accent: 4 px **teal** (#3BBF92) strip
- **Logo lockup — top-right** (white variants), x=860–1240, y=8–60
- **Decorative section number — right zone**: font-size=320, white 6% opacity, centered ~x=1050 y=480
- **Left content block** (x=80–700):
  - Section label: x=80, y=268, 12 pt bold teal, letter-spacing=4 (e.g. "AGENDA")
  - Section title: x=80, baseline y=338, 44 pt bold white
  - Teal underline: x=80, y=356, w=300, h=3
  - Agenda items y=394+: active item has 4 px cyan left bar + bold white 16 pt; inactive items at fill-opacity=0.65
- Footer: copyright + page num, white 8 pt at 50% opacity

### 3. Content (03_content.svg)

- Background: `images/bg_content_tl.jpeg` (default; Executor rotates TR/BL/BR/standard/alt across a long deck — see §VI)
- Top accent: 3 px **navy** (#1B1164) strip
- **Header** (y=3–72):
  - Section tag pill: x=40 y=8, h=22, rx=3, cyan fill, white 11 pt bold
  - Page title: x=40, baseline y=58, 28 pt bold navy
  - Logo lockup: x=840–1240, y=6–62, H=44 px, navy variants
- Header separator: y=72–74, cyan
- **Content area**: y=80–690, x=40–1240 — Executor fills freely
- Footer: copyright left + page number right, grey 8–9 pt

### 4. Ending / Thank You (04_ending.svg)

- Background: `images/bg_thankyou.jpeg` full-bleed (teal wave top+bottom, white center)
- Top accent: 4 px **teal** (#3BBF92) strip
- **Logo lockup — top-right** (navy), x=860–1240, y=8–60
- **Centered content block** (x=200–1080, y=260–500):
  - Closing title: centered x=640, baseline y=360, 56 pt bold navy
  - Teal underline: centered x=540, y=376, w=200, h=3
  - Tagline: centered x=640, baseline y=422, 20 pt dark
  - Contact / URL: centered x=640, baseline y=458, 15 pt cyan
- Footer: copyright only, grey italic 8 pt, centered x=640 y=708

---

## V. SVG Page Roster

| File | Role | Description |
|---|---|---|
| `01_cover.svg` | cover | Title slide — project name, phase, presenter, date |
| `02_divider.svg` | divider | Section break / agenda overview |
| `03_content.svg` | content | Main content page |
| `04_ending.svg` | ending | Thank-you / closing page |

---

## VI. Background Variants (Content Slides)

Executor rotates these for visual variety across a long deck. All variants have white centers; only the wave-dot corner changes.

| File | Key | Suggested usage |
|---|---|---|
| `images/bg_content_tl.jpeg` | TL | Default — most pages |
| `images/bg_content_tr.jpeg` | TR | Clean alternative (subtle edges all around) |
| `images/bg_content_bl.jpeg` | BL | Variety around slide 8–12 |
| `images/bg_content_br.jpeg` | BR | Variety in final content section |
| `images/bg_content.jpeg` | STD | Standard fallback |
| `images/bg_content_alt.jpeg` | ALT | High-density data pages |

---

## VII. Logo Lockup Rules

Order is always fixed: **PTTEP | DigitalX | SHANA** — never reorder.

| Slide | Position | H | Variant |
|---|---|---|---|
| Cover | Top-left, x=40–400, y=12–68 | 48 px | navy (PTTEP, DigitalX, SHANA navy) |
| Content | Top-right, x=840–1240, y=6–62 | 44 px | navy |
| Divider | Top-right, x=860–1240, y=8–60 | 44 px | white (logo_shana_white.png; PTTEP/DigitalX color) |
| Ending | Top-right, x=860–1240, y=8–60 | 44 px | navy |

Separator between logos: `<line>` 1 px, 40% opacity, color matches logo variant (dark or white).

Logo files in this template directory: `logo_pttep.png` · `logo_digitalx.png` · `logo_shana_navy.png` · `logo_shana_white.png`

---

## VIII. Table Component

Tables use SHANA CI styling throughout:

| Row type | Fill | Text |
|---|---|---|
| Header | `#00AEEF` cyan | White, Calibri Bold 12–13 pt |
| Body even | `#FFFFFF` white | Dark #1A1A2E, Calibri 10–13 pt |
| Body odd | `#F5F5F5` light grey | Dark #1A1A2E, Calibri 10–13 pt |
| All borders | `#D5D5D5` 1 px | — |

rx=0 (straight edges — per corporate style).

---

## IX. Spacing Guidelines

| Element | Value |
|---|---|
| Side padding | 40 px |
| Card gap | 16 px |
| Card inner padding | 16 px |
| Card border radius | 4 px |
| Icon–text gap | 10 px |
| Footer text baseline | y=710 |

---

## X. SVG Technical Constraints

1. viewBox: `0 0 1280 720`
2. Background: `<image href="images/bg_*.jpeg" x="0" y="0" width="1280" height="720" preserveAspectRatio="xMidYMid slice"/>`
3. Logo images: `<image href="logo_*.png" preserveAspectRatio="xMinYMid meet"/>`
4. Use `fill-opacity` / `stroke-opacity` — never `rgba()`
5. Prohibited: `mask`, `<style>`, `class`, `foreignObject`; `clipPath` only as `<image>` wrapper
6. No group opacity — set on each child element individually
7. Text wrap via `<tspan>` only
8. All styles inline

Font stack: `font-family="Calibri, 'Segoe UI', Arial, sans-serif"`

---

## XI. Placeholder Reference

| Placeholder | Slide | Description |
|---|---|---|
| `{{TITLE}}` | cover | Main presentation title |
| `{{SUBTITLE}}` | cover | Subtitle or workstream name |
| `{{PHASE}}` | cover | Phase / project label (cyan) |
| `{{DATE}}` | cover | Presentation date |
| `{{YEAR}}` | all | Copyright year |
| `{{SECTION_LABEL}}` | divider | Small uppercase category ("AGENDA", "OVERVIEW") |
| `{{SECTION_TITLE}}` | divider | Section main heading |
| `{{SECTION_NUM}}` | divider | Decorative section number ("01", "02" …) |
| `{{AGENDA_ITEM_N}}` | divider | Agenda list item N (N=1…5) |
| `{{SECTION_TAG}}` | content | Small cyan pill label above page title |
| `{{PAGE_TITLE}}` | content | Content slide page title |
| `{{PAGE_NUM}}` | content, divider, ending | Slide number |
| `{{CLOSING_TITLE}}` | ending | Main closing message (default: "Thank You") |
| `{{TAGLINE}}` | ending | Tagline or sub-message |
| `{{CONTACT}}` | ending | Contact / website line |

---

## XII. Reusable Component Snippets

### Section Tag Pill
```xml
<rect x="40" y="8" width="80" height="22" rx="3" fill="#00AEEF"/>
<text x="48" y="23" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="11" font-weight="bold" fill="#FFFFFF">OVERVIEW</text>
```

### CI Table (header + 2 data rows)
```xml
<!-- Header row -->
<rect x="40" y="100" width="1200" height="32" fill="#00AEEF"/>
<text x="48" y="121" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="12" font-weight="bold" fill="#FFFFFF">Column A</text>
<!-- Even row -->
<rect x="40" y="132" width="1200" height="28" fill="#FFFFFF" stroke="#D5D5D5" stroke-width="1"/>
<text x="48" y="151" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="12" fill="#1A1A2E">Cell value</text>
<!-- Odd row -->
<rect x="40" y="160" width="1200" height="28" fill="#F5F5F5" stroke="#D5D5D5" stroke-width="1"/>
<text x="48" y="179" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="12" fill="#1A1A2E">Cell value</text>
```

### KPI Card
```xml
<rect x="40" y="100" width="280" height="120" rx="4" fill="#FFFFFF" stroke="#D5D5D5" stroke-width="1"/>
<rect x="40" y="100" width="4" height="120" fill="#00AEEF"/>
<text x="56" y="128" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="11" font-weight="bold" fill="#00AEEF">KPI LABEL</text>
<text x="56" y="172" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="44" font-weight="bold" fill="#1B1164">42%</text>
<text x="56" y="198" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="12" fill="#888888">Supporting context</text>
```

### Active Agenda Item (Divider Slide)
```xml
<!-- Active: left bar + bold white -->
<rect x="80" y="394" width="4" height="30" fill="#00AEEF"/>
<text x="96" y="415" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="16" font-weight="bold" fill="#FFFFFF">01   Active Item</text>
<!-- Inactive: dimmed white -->
<text x="96" y="455" font-family="Calibri, 'Segoe UI', Arial, sans-serif" font-size="16" fill="#FFFFFF" fill-opacity="0.65">02   Inactive Item</text>
```

---

## XIII. Usage

To apply this layout alongside the SHANA brand in a project:

```
Create a Q4 status deck using:
  skills/ppt-master/templates/brands/shana-ci/
  skills/ppt-master/templates/layouts/shana-ci/
```

Step 3 fuses them: brand wins on color / typography / logo / voice; this spec wins on canvas / page structure / SVG roster.
