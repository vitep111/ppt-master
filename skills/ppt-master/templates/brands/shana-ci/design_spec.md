---
brand_id: shana-ci
kind: brand
summary: "SHANA project official corporate identity — PTTEP | DigitalX | SHANA co-branded presentations (delivered by Accenture)"
keywords: [shana, pttep, digitalx, accenture, corporate]
primary_color: "#1B1164"
---

# SHANA Corporate Identity Brand Specification

> Identity-only preset. No SVG page roster — pages are composed freely under these constraints.
> All values extracted directly from the official SHANA deck theme XML (`theme1.xml`) and slide layouts. Provenance `fact` = read from theme/layout XML; `approx` = visual estimate.

## I. Brand Overview

| Property | Value |
|---|---|
| Brand Name | SHANA — PTTEP \| DigitalX \| SHANA |
| Delivered by | Accenture |
| Use Cases | Change impact analysis, workstream deliverables, milestone sign-off decks, PMO reviews, stakeholder briefs |
| Tone | Formal, confidential, structured, conclusion-first |

## II. Color Scheme

The official theme palette (`theme1.xml` `<a:clrScheme>`):

| Role | HEX | Provenance | Notes |
|---|---|---|---|
| primary (accent1) | #1B1164 | fact | Navy — all titles, headings, strong text, logo |
| accent (accent3) | #00AEEF | fact | Cyan — table headers, section tags, accent bars, links |
| positive (accent5) | #3BBF92 | fact | Teal/green — secondary accents, dividers, "to-be" highlights |
| mid-blue (accent2) | #2A6FA0 | fact | Steel blue — secondary data series, sub-accents |
| lavender (accent4) | #D1CCF4 | fact | Pale violet — soft fills, chart tints, callout backgrounds |
| amber (accent6) | #F4A261 | fact | Warm orange — alerts, "high impact" emphasis |
| text (dk1) | #000000 | fact | Body text (often softened to #1A1A2E) |
| muted (dk2) | #5E5E5E | fact | Secondary text, captions |
| border (lt2) | #D5D5D5 | fact | Borders, separators, table gridlines |
| bg (lt1) | #FFFFFF | fact | Page background (white center of all bg images) |

### Supplementary colors seen in slide content

| HEX | Usage |
|---|---|
| #00B0F0 | Bright blue — process/system callouts |
| #C00000 | Dark red — risks, removed/decommissioned systems |
| #92D050 | Green — added/new systems, positive deltas |
| #002060 | Deep navy — high-contrast labels |
| #E7F8FF | Pale cyan — light card fills |

### Gradient Recipes (observed in backgrounds & logo)

| Name | Definition |
|---|---|
| SHANA logo (color) | left `#1B7FE0` (blue) → right `#3BBF92` (green) |
| Section / cover background | green `#3BBF92` → cyan `#00AEEF` → white |
| Divider band | left saturated `#00AEEF`/`#3BBF92` dot-wave → right white |

## III. Typography

Theme fonts (`theme1.xml` `<a:fontScheme>`):

| Role | Family | Weight | Size | Color |
|---|---|---|---|---|
| major (headings) | Helvetica Neue | Bold | cover 42pt · section 48pt · content title 28pt | #1B1164 |
| minor (body) | Helvetica | Regular | 14–16pt | #000000 / #1A1A2E |
| sub-heading | Helvetica Neue | Bold | 14pt | #1B1164 |
| KPI figure | Helvetica Neue | Bold | 32pt | #1B1164 |
| footer | Helvetica Neue | Regular | 8pt | #000000 |
| page number | Helvetica Neue | Regular | 10pt | #000000 |

> The deck declares **Helvetica Neue / Helvetica**. On Windows/Office these fall back to Arial. Recommended SVG font stack: `"Helvetica Neue", Helvetica, Arial, sans-serif`. Embed Helvetica Neue into the PPTX for exact fidelity, otherwise accept the Arial fallback.

## IV. Logo

### Lockup order — always **PTTEP | DigitalX | SHANA** (left to right), top-left of every slide. Never reorder.

| File | Form | Usage |
|---|---|---|
| `./logo_pttep.png` | PTTEP flame mark + navy wordmark | Always — leftmost |
| `./logo_digitalx.png` | "DigitalX" cyan/navy + green-blue X mark | Always — center |
| `./logo_shana_gradient.png` | SHANA wordmark, blue→green gradient | **Cover only** — rightmost |
| `./logo_shana_navy.png` | SHANA wordmark, solid navy #1B1164 | **All non-cover slides** — rightmost |
| `./logo_shana_navy_flat.png` | SHANA navy, smaller flat version | Tight/small placements |

### Placement (from layout XML, 1280×720 canvas)

| Slide | PTTEP | DigitalX | SHANA |
|---|---|---|---|
| Cover (larger) | x=0 y=2 · 255×66 | x=319 y=0 · 193×85 | gradient x=510 y=12 · 254×48 |
| Content / Divider / Section | x=0 y=0 · 154×40 | x=193 y=2 · 108×48 | navy x=312 y=5 · 167×32 |

- Logo lockup sits **top-left** on all slide types
- Clearspace: keep ≥ 0.4× mark height clear; never overlap title text
- Never recolor the logos; use the navy SHANA on light/content backgrounds and the gradient SHANA only on the white cover

## V. Voice & Tone

- Formality: formal
- Person: we / passive
- Emoji: forbidden
- Abbreviations: common-abbrev-allowed (SAP Concur, CIA, TE, R&R, etc.)
- Footer (exact, every slide): `Copyright © {{YEAR}} Accenture. All rights reserved. Accenture Confidential Information`
- Page numbers: bottom-right on all content/divider slides

## VI. Icon Style

- Preference: filled / duotone (the deck uses 512×512 filled pictographic icons for impact areas — People, Process, Tech, Data, Document — and small tick marks for change actions)
- Icon accent colors drawn from the palette (navy / cyan / teal)

## VII. Visual Assets

- Logos: this directory (`logo_*.png`)
- Backgrounds: `./images/`

### Background Catalog (real, theme-sourced)

| File | Slide type | Description |
|---|---|---|
| `images/bg_cover.jpeg` | Cover | Green glow top-left → white center → bright cyan right, wave dots bottom |
| `images/bg_content.jpeg` | Content | White center, teal/cyan wave dots top-left + bottom-right corners |
| `images/bg_section.png` | Section title / TOC | Full cyan-blue gradient + green wave dots left (for white text) |
| `images/bg_divider.jpeg` | Section divider | Green-cyan dot-wave left band → white right |
| `images/bg_thankyou.jpeg` | Thank-you / closing | Cyan wave dots top + bottom, white center band |

### Usage Rule
Always place the real background image full-bleed (`xMidYMid slice`); never approximate with flat color or shapes.
