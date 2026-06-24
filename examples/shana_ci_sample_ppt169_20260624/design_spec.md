# SHANA CI Sample — Change Impact Analysis · Finance & T&E Workstream

> Fused from:
> - brand: `templates/brands/shana-ci/` (identity: color / typography / logo / voice)
> - layout: `templates/layouts/shana-ci/` (structure: canvas / page roster / geometry)

## I. Project Information

| Item | Value |
|---|---|
| **Project Name** | shana_ci_sample |
| **Canvas Format** | PPT 16:9 (1280×720) |
| **Page Count** | 9 |
| **Design Style** | B) General Consulting + SHANA Corporate CI |
| **Target Audience** | SHANA PMO leads, workstream owners, change management team |
| **Use Case** | Internal milestone review / change impact sign-off |
| **Created Date** | 2026-06-24 |

---

## II. Canvas Specification

| Property | Value |
|---|---|
| **Format** | PPT 16:9 |
| **Dimensions** | 1280 × 720 px |
| **viewBox** | `0 0 1280 720` |
| **Margins** | Left/right 60px; top 112px (below logo + title zone); bottom 30px above footer |
| **Content Area** | x: 60–1220, y: 112–668 (from layout spec) |

---

## III. Visual Theme

### Theme Style

- **Style**: Corporate consulting, structured — navy + cyan + teal on photo-textured white canvas
- **Theme**: Light
- **Tone**: Authoritative, structured, PTTEP/Accenture corporate

### Color Scheme

| Role | HEX | Purpose |
|---|---|---|
| **Primary (Navy)** | `#1B1164` | Titles, headings, logo, strong text |
| **Accent (Cyan)** | `#00AEEF` | Accent bars, table headers, links, underlines |
| **Accent2 (Teal)** | `#3BBF92` | Dividers, "to-be" highlights, rules |
| **Secondary (Mid-blue)** | `#2A6FA0` | Subtitles, secondary data labels |
| **Alert (Amber)** | `#F4A261` | High-impact emphasis, severity badges |
| **Risk red** | `#C00000` | Decommissioned / removed systems |
| **New green** | `#92D050` | New / added systems |
| **Muted** | `#5E5E5E` | Captions, secondary text |
| **Border** | `#D5D5D5` | Gridlines, separators, table borders |
| **Background** | `#FFFFFF` | Content zone background |

---

## IV. Typography System

### Font Plan

**Typography direction**: SHANA corporate — Helvetica Neue (locked from theme fontScheme)

| Role | Latin | Fallback |
|---|---|---|
| **Title** | Helvetica Neue | Helvetica, Arial, sans-serif |
| **Body** | Helvetica | Arial, sans-serif |
| **Emphasis** | Helvetica Neue Bold | — |
| **Code** | Consolas | Courier New, monospace |

**Per-role font stacks**:
- Title: `'Helvetica Neue', Helvetica, Arial, sans-serif`
- Body: `Helvetica, Arial, sans-serif`
- Emphasis: `'Helvetica Neue', Helvetica, Arial, sans-serif`
- Code: `Consolas, 'Courier New', monospace`

### Font Size Hierarchy

**Baseline**: Body font size = 16px (dense corporate)

| Purpose | px | Weight |
|---|---|---|
| Cover title | 42px | Bold |
| Section divider title | 48px | Bold |
| Page title | 28px | Bold |
| KPI figure | 32px | Bold |
| Subtitle | 22px | Regular |
| **Body** | **16px** | Regular |
| Annotation / caption | 13px | Regular |
| Footer / page number | 8–10px | Regular |

**Formula policy**: text-only (no formulas in this deck)

---

## V. Layout Principles

### Page Structure

- **Header/logo zone**: y=0–100 (logo lockup top-left + page title at y=51)
- **Title underline**: y=100, cyan hairline
- **Content area**: x=60–1220, y=112–668
- **Footer zone**: y=697 (copyright + page number)

### Layout Pattern Library

| Pattern | Used on |
|---|---|
| Full-bleed + logo lockup (template) | P01 Cover, P02/P06 Dividers, P09 Ending |
| Asymmetric split (3:7 for label+content) | P03 As-Is table |
| Three-column stats | P04 KPI summary |
| 5-cell icon grid (horizontal) | P05 Impact area |
| Two-column comparison | P07 To-Be landscape |
| Timeline horizontal | P08 Actions |

### Spacing Specification

| Element | Value |
|---|---|
| Safe margin | 60px (left/right) |
| Column gap | 30–40px |
| Card padding | 20–24px |
| Icon-text gap | 12px |

---

## VI. Icon Usage Specification

- **Library**: `tabler-filled`
- **Usage**: Impact area grid (P05), section callouts

| Purpose | Icon | Page |
|---|---|---|
| People | `tabler-filled/user` | P05 |
| Process | `tabler-filled/settings` | P05 |
| Technology | `tabler-filled/device-desktop` | P05 |
| Data | `tabler-filled/database` | P05 |
| Document | `tabler-filled/file-description` | P05 |
| Checkmark | `tabler-filled/check` | P08 |
| Right arrow | `tabler-filled/arrow-big-right` | P03, P07 |

---

## VII. Visualization Reference List

Catalog read: 71 templates

| Page | Template | Path | Summary-quote (verbatim) | Usage |
|---|---|---|---|---|
| P04 | kpi_cards | `templates/charts/kpi_cards.svg` | "Pick for 4-8 standalone numeric metrics shown as overview cards (2x2 or 1x4) — each card shows a big number, label, and optional trend indicator." | 3-up KPI columns: impacted processes, decommissioned systems, new tools |
| P05 | icon_grid | `templates/charts/icon_grid.svg` | "Pick for 4-9 parallel features/capabilities/services as icon cards — feature grid" | 5-cell impact area grid: People / Process / Tech / Data / Document |
| P08 | timeline | `templates/charts/timeline.svg` | "Pick for 3-8 milestone events on a horizontal time axis (no duration). Skip for tasks with duration (use gantt_chart)." | 4-phase implementation timeline Q3–Q4 2026 |

**Runners-up considered**:
- `bullet_chart` | rejected for P04: requires explicit targets per metric; our KPI stats are standalone counts without target lines
- `horizontal_bar_chart` | rejected for P05: impact area is qualitative/categorical, not a ranked metric list
- `gantt_chart` | rejected for P08: no task-duration bars needed; milestone-only timeline is cleaner at this stage

---

## VIII. Image Resource List

| Filename | Dimensions | Purpose | Type | Layout pattern | Acquire Via | Status |
|---|---|---|---|---|---|---|
| images/bg_cover.jpeg | 4000×2250 | Cover full-bleed background | Background | #1 full-bleed + title overlay | user | Existing |
| images/bg_divider.jpeg | 4000×2250 | Section divider background | Background | #1 full-bleed + title overlay | user | Existing |
| images/bg_content.jpeg | 4000×2250 | Content page background | Background | #1 full-bleed + text overlay | user | Existing |
| images/bg_thankyou.jpeg | 4000×2250 | Ending page background | Background | #1 full-bleed + title overlay | user | Existing |
| logo_pttep.png | 400×104 | PTTEP logo lockup | Logo | n/a | user | Existing |
| logo_digitalx.png | 1584×701 | DigitalX logo lockup | Logo | n/a | user | Existing |
| logo_shana_gradient.png | 12500×4966 | SHANA gradient logo (cover only) | Logo | n/a | user | Existing |
| logo_shana_navy.png | 12500×4966 | SHANA navy logo (all other slides) | Logo | n/a | user | Existing |

---

## IX. Content Outline

### Part 1: Cover & Navigation

#### Slide 01 — Cover (anchor)

- **Layout**: Full-bleed bg_cover.jpeg + logo lockup (larger) + centered title block
- **Template**: `01_cover.svg`
- **Title**: Change Impact Analysis
- **Subtitle**: Finance & Travel & Expense Workstream
- **Date**: June 2026 | v0.1
- **Core message**: This deck presents the change impact assessment for the Finance / T&E workstream as SHANA moves from legacy systems to SAP S/4HANA and Concur.

---

### Part 2: Current State Overview

#### Slide 02 — Section Divider (anchor)

- **Layout**: Full-bleed bg_divider.jpeg + logo + giant watermark number + section title
- **Template**: `02_divider.svg`
- **Section number**: 01
- **Section title**: Current State Overview
- **Core message**: Establishes the as-is baseline before assessing change impact.

#### Slide 03 — As-Is System Landscape (dense)

- **Layout**: Full-width table (3 columns: System / Owner / Status) below page title; arrow callout linking to P07
- **Template**: `03_content.svg` (base)
- **Page title**: As-Is System Landscape
- **Core message**: The current Finance stack runs on 3 legacy platforms that will be partially or fully replaced.
- **Content**:

  | System | Module / Scope | Status |
  |---|---|---|
  | SAP ECC 6.0 | Core Finance GL, AP, AR | Being replaced by S/4HANA |
  | E-Payment Portal | Travel claims, expense reimbursement | Decommissioned |
  | Concur Legacy | T&E booking (limited rollout) | Upgraded to full Concur suite |
  | Manual Excel | Budget tracking, cost allocation | Replaced by S/4HANA CO |

  Status colours: decommissioned → red `#C00000`; being replaced → amber `#F4A261`; upgraded → teal `#3BBF92`

#### Slide 04 — Change Impact Summary (dense)

- **Layout**: 3-column KPI stats separated by vertical `#D5D5D5` hairlines, each column = large number (32pt navy) + label + supporting bullet
- **Template**: `03_content.svg` (base); adapt kpi_cards pattern
- **Page title**: Change Impact Summary
- **Core message**: The workstream faces significant breadth of change — 15 impacted processes, 3 system retirements, 480 end users to train.
- **Content**:
  - Col 1: **15** Impacted Business Processes · T&E claims · Expense approval · Cost centre coding · Month-end close · AP reconciliation (top 5 shown)
  - Col 2: **3** Systems Decommissioned · E-Payment Portal · SAP ECC Finance module · Manual Excel CO tracker
  - Col 3: **480** End Users to Train · Finance team: 120 · T&E requestors: 340 · AP clerks: 20

#### Slide 05 — Impact Area Assessment (dense)

- **Layout**: 5-cell horizontal icon grid (equal width cells) — People / Process / Technology / Data / Document; each cell = icon + area name + severity badge + 2-line description
- **Template**: `03_content.svg` (base); icon_grid pattern
- **Page title**: Impact Area Assessment
- **Core message**: Technology and Process carry the highest impact; People training is moderate; Data migration is critical but contained; Document updates are low impact.
- **Content**:
  - People | icon: user | **High** (amber) | 480 users across 3 roles; change management and training plan required
  - Process | icon: settings | **High** (amber) | 15 processes redesigned; 6 new approval workflows introduced
  - Technology | icon: device-desktop | **High** (amber) | 3 decommissions, 2 new platforms, 4 integration touchpoints
  - Data | icon: database | **Medium** (cyan) | Historical data migration from ECC; 3-year data retention in archive
  - Document | icon: file-description | **Low** (teal) | SOP updates and job aids; no regulatory filing impact

---

### Part 3: Target State & Actions

#### Slide 06 — Section Divider (anchor)

- **Layout**: Full-bleed bg_divider.jpeg + logo + giant watermark number + section title
- **Template**: `02_divider.svg`
- **Section number**: 02
- **Section title**: Target State & Key Actions
- **Core message**: Defines the to-be landscape and concrete change actions for the workstream.

#### Slide 07 — To-Be System Landscape (dense)

- **Layout**: Two-column comparison; Left = As-Is systems (grayed out with red strike for decommissioned); Right = To-Be systems (green for new); arrows in the center show migration direction
- **Template**: `03_content.svg` (base)
- **Page title**: To-Be System Landscape
- **Core message**: Legacy E-Payment and ECC Finance are replaced by SAP Concur and S/4HANA, creating a unified and integrated Finance platform.
- **Content**:
  - As-Is (left, x=60–580): SAP ECC 6.0 [→ S/4HANA, amber arrow], E-Payment Portal [→ DECOMMISSIONED, red], Concur Legacy [→ Concur Full Suite, teal arrow], Manual Excel [→ DECOMMISSIONED, red]
  - To-Be (right, x=640–1220): SAP S/4HANA (green #92D050 label), SAP Concur Full Suite (green), Integrated Data Archive (teal)
  - Column headers: "Current (As-Is)" left | "Future (To-Be)" right; divider line at x=610

#### Slide 08 — Key Actions & Timeline (dense)

- **Layout**: Horizontal timeline with 4 phase nodes; below each node = action bullets
- **Template**: `03_content.svg` (base); adapt timeline chart
- **Page title**: Key Actions & Timeline
- **Core message**: Implementation spans Q3–Q4 2026 in four sequential phases, culminating in go-live and hypercare.
- **Content**:
  - Phase 1 · Jul 2026: System configuration complete · Data migration blueprint signed off
  - Phase 2 · Aug 2026: UAT executed · Change impact workshops conducted for all 3 roles
  - Phase 3 · Sep 2026: Training delivered · Cut-over planning finalised · Legacy data archived
  - Phase 4 · Oct 2026: Go-live · Hypercare support 4 weeks · Lessons learned captured

---

### Part 4: Close

#### Slide 09 — Ending (anchor)

- **Layout**: Full-bleed bg_thankyou.jpeg + logo + centered closing block
- **Template**: `04_ending.svg`
- **Closing title**: Thank You
- **Tagline**: SHANA — Enabling Digital Finance for PTTEP
- **Contact**: shana-pmo@pttep.com
- **Core message**: Close and contact slide.

---

## X. Speaker Notes Requirements

- One file per slide: `notes/01_cover.md` through `notes/09_ending.md`
- Master: `notes/total.md` with `#` headings per slide
- Style: professional, concise script — presenter-paced, consulting delivery
- Duration: ~15 minutes total (~1.5 min/slide average)

---

## XI. Technical Constraints Reminder

1. viewBox: `0 0 1280 720` on every SVG
2. Background images: `<image href="images/bg_*.jpeg" preserveAspectRatio="xMidYMid slice"/>`
3. Logos: `<image href="logo_*.png" preserveAspectRatio="xMinYMid meet"/>`
4. `fill-opacity` / `stroke-opacity` only — no `rgba()`
5. Prohibited: `mask`, `<style>`, `class`, `foreignObject`, `textPath`, `animate*`, `script`
6. No group opacity — set per child element
7. Text wrap: `<tspan>` with `dy` offsets — no `<foreignObject>`
8. XML entities: raw Unicode only; escape `&` as `&amp;`, `<` as `&lt;`, `>` as `&gt;`
9. Icon placeholders: `<use data-icon="tabler-filled/icon-name" .../>`
