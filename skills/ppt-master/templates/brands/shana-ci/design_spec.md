---
brand_id: shana-ci
kind: brand
summary: "SHANA project official corporate identity — PTTEP | DigitalX | SHANA co-branded presentations"
keywords: [shana, pttep, digitalx, corporate, energy]
primary_color: "#1B1164"
---

# SHANA Corporate Identity Brand Specification

> Identity-only preset. No SVG page roster — pages are composed freely under these constraints.
> Extracted from the official SHANA Presentation Template (`_SHANA__Presentation_Template_for_ACN_2026_V1_20260219.potx`).

## I. Brand Overview

| Property | Value |
|---|---|
| Brand Name | SHANA — PTTEP \| DigitalX \| SHANA |
| Use Cases | Project status decks, workstream deliverables, stakeholder presentations, internal reports |
| Tone | Formal, confidential, professional |

## II. Color Scheme

| Role | HEX | Provenance |
|---|---|---|
| primary | #1B1164 | fact — Navy; headings, titles, strong text |
| secondary | #00AEEF | fact — Cyan; accent elements, table headers, section tags |
| accent | #3BBF92 | fact — Teal; secondary accents, divider elements |
| text | #1A1A2E | fact — Off-Black; body text |
| bg | #F0F9FF | fact — Light Sky; default content background |
| supporting_white | #FFFFFF | fact — text on dark backgrounds |
| supporting_grey | #D5D5D5 | fact — borders, captions, separators |
| supporting_footer | #888888 | fact — footer text |
| supporting_dark_blue | #0066CC | fact — section divider gradient end |
| supporting_light_grey | #F5F5F5 | fact — alternating table rows |

### Gradient Recipes

| Name | Definition |
|---|---|
| Cover / Title background | left `#E8F6FF` → right `#00AEEF` |
| Section Divider | left `#00AEEF` → right `#0066CC` |
| Teal accent | `#3BBF92` → `#00AEEF` |

## III. Typography

| Role | Family | Weight | Size Range | Color |
|---|---|---|---|---|
| cover title | Calibri | Bold | 40pt | #1B1164 |
| title | Calibri | Bold | 30–44pt | #1B1164 |
| subtitle | Calibri | Light | 24–28pt | #1B1164 |
| section tag | Calibri | Regular | 11pt | #00AEEF |
| body | Calibri | Regular | 14–16pt | #1A1A2E |
| table header | Calibri | Bold | 12–13pt | #FFFFFF on #00AEEF fill |
| table body | Calibri | Regular | 10–13pt | #1A1A2E |
| footer | Calibri | Italic | 8–10pt | #888888 |

## IV. Logo

### Primary Logo Lockup
- Order: **PTTEP | DigitalX | SHANA** — never change this order
- File (color): `./logo.png` — SHANA color logo; use as primary
- File (navy): `./logo_navy.png` — navy variant; use on light backgrounds
- File (white): `./logo_white.png` — white variant; use on dark/color backgrounds
- File (PTTEP): `./logo_pttep.png` / `./logo_pttep_hq.png`
- File (DigitalX): `./logo_digitalx.png` / `./logo_digitalx_hq.png`

### Logo Placement Rules

| Slide type | Position | Variant |
|---|---|---|
| Title / Cover | Top-left, larger | color or navy |
| Content slides | Top-right, standard | navy |
| Section dividers | Top-right, standard | white (on dark bg) |
| Thank You | Centered or top | white |

- Usage: every-page

### Fallback (when image unavailable)
Text lockup: "PTTEP  |  DigitalX  |  SHANA" — SHANA portion in bold italic teal (#3BBF92)

## V. Voice & Tone

- Formality: formal
- Person: we
- Emoji: forbidden
- Abbreviations: common-abbrev-allowed
- Footer: `Confidential. Copyright © [YEAR], PTTEP and Accenture. All rights reserved.` — auto on every slide
- Page numbers: bottom-right on all content slides

## VI. Icon Style

- Preference: linear
- Color: navy #1B1164 or cyan #00AEEF depending on context

## VII. Visual Assets

- Images: `./images/` — official background images extracted from POTX template

### Background Image Catalog

| File | Slide Type | Description |
|---|---|---|
| `images/bg_cover.jpeg` | Title / Cover | Green top-left glow → white → bright blue right |
| `images/bg_divider.png` | Agenda / Section Divider | Green-to-cyan left + wave dots → solid blue right |
| `images/bg_content_tl.jpeg` | Content (default) | White center, teal wave dots top-left |
| `images/bg_content_tr.jpeg` | Content (alt) | White center, subtle teal dots all edges |
| `images/bg_content_bl.jpeg` | Content (alt) | White center, wave dots bottom-left |
| `images/bg_content_br.jpeg` | Content (alt) | White center, wave dots bottom-right |
| `images/bg_content.jpeg` | Content (standard) | Standard content background |
| `images/bg_content_alt.jpeg` | Content (alternate) | Alternate content background |
| `images/bg_thankyou.jpeg` | Thank You / End | Full teal wave top + bottom, white center |

### Usage Rule
Always use the real background JPEG/PNG — never approximate with flat color or shapes.
