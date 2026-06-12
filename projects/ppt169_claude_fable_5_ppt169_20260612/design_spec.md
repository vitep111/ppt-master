# Claude Fable 5 — Overview & Use Cases - Design Spec

> Human-readable design narrative. Machine-readable execution contract: `spec_lock.md` — Executor re-reads it before every SVG page. On divergence, `spec_lock.md` wins.

## I. Project Information

| Item | Value |
| ---- | ----- |
| **Project Name** | Claude Fable 5 — Overview & Use Cases |
| **Canvas Format** | PPT 16:9 (1280×720) |
| **Page Count** | 13 |
| **Design Style** | General Consulting + Claude design language (restrained, modern, conclusion-first) |
| **Target Audience** | Developers and technical decision-makers |
| **Use Case** | Tech talk / internal briefing on the Claude Fable 5 launch |
| **Created Date** | 2026-06-12 |

---

## II. Canvas Specification

| Property | Value |
| -------- | ----- |
| **Format** | PPT 16:9 |
| **Dimensions** | 1280×720 |
| **viewBox** | `0 0 1280 720` |
| **Margins** | left/right 60px, top/bottom 50px |
| **Content Area** | 1160×620 (60,50 → 1220,670) |

---

## III. Visual Theme

### Theme Style

- **Style**: Claude design language — Anthropic brand preset applied (`templates/design_spec.md`, kind: brand). Restrained product-UI tone, generous whitespace, conclusion-first headlines, six-petal mark as the only decorative motif.
- **Theme**: Light theme
- **Tone**: Tech-forward, professional, modern, restrained

### Color Scheme

> Brand preset locks the identity segment — these values are truth (provenance per brand spec).

| Role | HEX | Purpose |
| ---- | --- | ------- |
| **Background** | `#FFFFFF` | Page background |
| **Secondary bg** | `#F8FAFC` | Card background, section surfaces |
| **Primary** | `#D97757` | Anthropic Orange — title accents, key sections, icons, the mark |
| **Accent** | `#4A90D9` | Tech blue — flow / process, links, info highlights |
| **Secondary accent** | `#10B981` | Mint green — recommended options, success states |
| **Body text** | `#191919` | Anthropic near-black — main body text |
| **Secondary text** | `#64748B` | Slate gray — captions, annotations, chart labels |
| **Tertiary text** | `#94A3B8` | Footers, page numbers |
| **Border/divider** | `#E2E8F0` | Card borders, divider lines |
| **Success** | `#10B981` | Positive indicators |
| **Warning** | `#EF4444` | Coral red — risks, cautions |

Color discipline: 60-30-10 — white/off-white carries ≥60%, near-black text ~30%, orange `#D97757` as the ≤10% accent. Blue/green/red appear only when content type demands (process / recommended / risk). No more than 4 colors per page.

### Gradient Scheme

Used sparingly — only as a faint radial wash behind cover / closing hero zones:

```xml
<radialGradient id="bgDecor" cx="80%" cy="20%" r="60%">
  <stop offset="0%" stop-color="#D97757" stop-opacity="0.10"/>
  <stop offset="100%" stop-color="#D97757" stop-opacity="0"/>
</radialGradient>
```

### Brand assets (logo)

| File | Usage in this deck |
|---|---|
| `templates/anthropic_claude_lockup.svg` | Cover (bottom-left sign-off) and closing page — inline its `<path>` elements as native vectors, scaled via `transform` |
| `templates/anthropic_mark.svg` | Six-petal mark: small footer badge on content pages (optional, not every page); enlarged as the cover's decorative motif at low opacity |

Mark fill fixed `#D97757`; wordmark inherits `#191919`. Clearspace ≥ 0.5× mark height; never overlap text. Logos are inlined as `<path>` data (no `<image>` references) so they export as native DrawingML shapes.

---

## IV. Typography System

### Font Plan

**Typography direction**: Anthropic brand typefaces with PPT-safe fallback — "official Anthropic typefaces (Styrene A / Anthropic Sans) require install or PPTX embed"; the deck reads correctly on the Helvetica Neue → Arial fallback.

| Role | Chinese | English | Fallback tail |
| ---- | ------- | ------- | ------------- |
| **Title** | — | `"Styrene A", "Helvetica Neue", Arial` | `sans-serif` |
| **Body** | — | `"Anthropic Sans", "Helvetica Neue", Arial` | `sans-serif` |
| **Emphasis** | — | same as Title | `sans-serif` |
| **Code** | — | `Consolas, "Courier New"` | `monospace` |

**Per-role font stacks**:

- Title: `"Styrene A", "Helvetica Neue", Arial, sans-serif`
- Body: `"Anthropic Sans", "Helvetica Neue", Arial, sans-serif`
- Emphasis: same as Title
- Code: `Consolas, "Courier New", monospace`

### Font Size Hierarchy

**Baseline**: Body font size = **18px** (dense — data-bearing consulting deck).

| Purpose | Ratio to body | This deck | Weight |
| ------- | ------------- | --------- | ------ |
| Cover title | 2.5-5x | 64px | Bold |
| Chapter / section opener | 2-2.5x | 40px | Bold |
| Page title | 1.5-2x | 32px | Bold |
| Hero number | 1.5-2x+ | 48px (extended slot `hero_number`) | Bold |
| Subtitle | 1.2-1.5x | 22px | SemiBold |
| **Body** | **1x** | **18px** | Regular |
| Annotation / caption | 0.7-0.85x | 13px | Regular |
| Page number / footnote | 0.5-0.65x | 11px | Regular |

**Formula rendering policy**: `text-only` — no formula-worthy expressions in source.

---

## V. Layout Principles

### Page Structure

- **Header area**: 50-110px — page title left-aligned, thin orange kicker rule above title (40px × 3px)
- **Content area**: 130-650px — main layout zone
- **Footer area**: 670-700px — slate page number right, optional small six-petal mark left (id under `footer`/`logo` chrome tokens)

### Layout Pattern Library (combine or break as content demands)

| Pattern | Used on |
| ------- | ------- |
| Negative-space-driven | P01 cover, P03 statement, P09 hero number |
| Single column centered | P13 closing |
| Asymmetric split (3:7 / 7:3) | P04 (pyramid + side panel) |
| Three/four column cards | P05 KPI cards, P06 icon grid, P07 customer cards, P11 pillars |
| Top-bottom split | P10 module composition |
| Z-pattern numbered list | P02 agenda, P08 use cases, P12 safety |

Proportion follows information weight; `breathing` pages (P03, P09) avoid multi-card grids entirely — naked text, one rule line, whitespace.

### Spacing Specification

**Universal**: safe margin 60px; content block gap 28px; icon-text gap 12px.

**Card-based layouts**: card gap 24px; card padding 24px; card border radius 12px; three-column card width 370px; 2×3 grid card ≈ 565×175px.

**Non-card containers**: line-height 1.5× body; whitespace carries rhythm on breathing pages; content width ≤ 900px for statement prose.

---

## VI. Icon Usage Specification

### Source

- **Library**: `tabler-outline` (stroke), deck-wide `stroke-width: 2` — matches brand "Icon Style: stroke" preference
- **Brand marks**: `simple-icons` only for real company logos on P07 (stripe, github, cursor); Cognition has no logo in the library — text-only treatment
- **Usage**: `<use data-icon="tabler-outline/icon-name" .../>` placeholders; Executor may only use the approved inventory below

### Recommended Icon List

| Purpose | Icon Path | Page |
| ------- | --------- | ---- |
| Agenda items | `tabler-outline/list-check` | P02 |
| Positioning / frontier | `tabler-outline/sparkles`, `tabler-outline/target`, `tabler-outline/stack-2` | P02-P04 |
| Long-horizon autonomy | `tabler-outline/clock-play`, `tabler-outline/hourglass` | P06, P09 |
| Software engineering | `tabler-outline/code`, `tabler-outline/git-pull-request`, `tabler-outline/terminal-2` | P06, P08, P09 |
| Knowledge work | `tabler-outline/chart-bar`, `tabler-outline/file-text` | P06, P08, P10 |
| Vision | `tabler-outline/eye` | P06, P08 |
| Context + memory | `tabler-outline/database` | P05, P06 |
| Multi-agent | `tabler-outline/users-group`, `tabler-outline/robot` | P06, P08 |
| Research / analysis | `tabler-outline/search`, `tabler-outline/microscope`, `tabler-outline/flask`, `tabler-outline/scale` | P08, P10, P12 |
| Developer experience | `tabler-outline/brain`, `tabler-outline/adjustments-horizontal`, `tabler-outline/gauge`, `tabler-outline/refresh`, `tabler-outline/bolt` | P11 |
| Safety | `tabler-outline/shield-check`, `tabler-outline/shield-lock`, `tabler-outline/lock` | P11, P12 |
| Specs / availability | `tabler-outline/coin`, `tabler-outline/world`, `tabler-outline/calendar-event` | P05, P11 |
| CTA / closing | `tabler-outline/rocket`, `tabler-outline/arrow-right`, `tabler-outline/check`, `tabler-outline/message-chatbot` | P08, P13 |
| Customer logos | `simple-icons/stripe`, `simple-icons/github`, `simple-icons/cursor` | P07 |

---

## VII. Visualization Reference List

Catalog read: 71 templates

| Page | Template | Path | Summary-quote (verbatim from `charts_index.json`) | Usage |
| ---- | -------- | ---- | ------------------------------------------------- | ----- |
| P02 | agenda_list | `templates/charts/agenda_list.svg` | "Pick for table of contents, meeting agendas, or presentation roadmap — numbered items + brief description + duration / owner per row. Skip for substantive content lists (use vertical_list) or single-page section dividers (use a cover layout)." | Eight-item presentation roadmap |
| P04 | pyramid_chart | `templates/charts/pyramid_chart.svg` | "Pick for 3-6 stratified hierarchy layers in flat 2D side-view — Maslow's hierarchy, maturity models, value hierarchy, capability tiers, market segments, audience pyramid. Skip for dramatic tone (use pyramid_isometric), flat priority list (use vertical_list), or org reporting (use top_down_tree)." | Four capability tiers: Mythos class → Opus → Sonnet → Haiku |
| P05 | kpi_cards | `templates/charts/kpi_cards.svg` | "Pick for 4-8 standalone numeric metrics shown as overview cards (2x2 or 1x4) — exec summary opener, dashboard headline, quarterly recap, results-at-a-glance. Skip if metrics have target baselines (use bullet_chart) or single hero number (use gauge_chart)." | Six spec metrics at a glance |
| P06 | icon_grid | `templates/charts/icon_grid.svg` | "Pick for 4-9 parallel features/capabilities/services as icon cards — feature grid, service lineup, benefits matrix, brand values, product highlights. Skip for sequential ordering (use numbered_steps) or hierarchical layers (use pyramid_chart)." | Six headline capabilities |
| P07 | labeled_card | `templates/charts/labeled_card.svg` | "Pick for 3-4 parallel aspects of one subject with per-aspect titles + short body (self-introduction, four-pillar overview, capability quadrant). Skip for plain feature lists (use icon_grid), sequential steps (use numbered_steps), or strategic quadrants (use quadrant_text_bullets / matrix_2x2)." | Four early-access customer testimonials |
| P08 | vertical_list | `templates/charts/vertical_list.svg` | "Pick for 3-6 numbered key points each with a short description — design principles, core tenets, action items, key takeaways, recommendations, executive summary points. Skip for icon-style cards (use icon_grid) or sequential steps (use numbered_steps)." | Six numbered use cases |
| P10 | module_composition | `templates/charts/module_composition.svg` | "Pick for one parent container wrapping 3-N child module cards, each = title + 2-3 bullets — fits 'Feature X contains 3 parts, each with its own description'. Skip if source has only labels without descriptions (use numbered_steps or icon_grid)." | "Enterprise knowledge work" parent wrapping four work modules |
| P11 | vertical_pillars | `templates/charts/vertical_pillars.svg` | "Pick for 1×3 / 1×4 / 1×5 vertical column layout where each pillar = one independent category with title + bullets — PEST (Political/Economic/Social/Technological), four-pillar strategy overview, side-by-side independent categories. Skip for 2×2 quadrant (use quadrant_text_bullets), pricing tiers (use comparison_columns), or 2×2 parallel aspects (use labeled_card)." | Four developer-experience pillars |
| P12 | vertical_list | `templates/charts/vertical_list.svg` | "Pick for 3-6 numbered key points each with a short description — design principles, core tenets, action items, key takeaways, recommendations, executive summary points. Skip for icon-style cards (use icon_grid) or sequential steps (use numbered_steps)." | Three safeguards, numbered |

**Runners-up considered**:

- `timeline` | rejected for P02: agenda is a content roadmap with no time axis or milestone dates
- `comparison_table` | rejected for P04: the message is tier *hierarchy*, not row-by-row feature comparison across models
- `bullet_chart` | rejected for P05: spec metrics are standalone facts with no target-vs-actual baseline
- `team_roster` | rejected for P07: cards are company testimonials, not people profiles with photos
- `numbered_steps` | rejected for P08: the six use cases are parallel, not a sequence
- `layered_architecture` | rejected for P10: knowledge-work components are siblings inside one offering, not stacked architecture layers
- `comparison_columns` | rejected for P11: developer-experience pillars are not pricing/service tiers being sold against each other

---

## VIII. Image Resource List

No raster images (confirmation h = A "no images"). Brand logo SVGs (`anthropic_claude_lockup.svg`, `anthropic_mark.svg`) are inlined as native `<path>` vectors — they are not `<image>` assets and need no acquisition rows. Image-as-canvas coverage note: not applicable, deck has zero image-bearing pages.

---

## IX. Content Outline

### Part 1: Opening

#### Slide 01 - Cover

- **Layout**: Negative-space-driven; title block left, oversized six-petal mark (inlined path, `#D97757` at low opacity) bleeding off the right edge; faint radial wash top-right
- **Title**: Claude Fable 5
- **Subtitle**: Overview & Use Cases
- **Kicker**: ANTHROPIC · MYTHOS CLASS
- **Info**: June 2026 · model ID `claude-fable-5` · Claude lockup bottom-left

#### Slide 02 - Agenda

- **Layout**: Z-pattern numbered list (agenda_list adaptation, two columns of four)
- **Title**: What we'll cover
- **Core message**: Eight stops from "what it is" to "how it ships safely."
- **Visualization**: agenda_list (see VII)
- **Content**:
  - 01 What is Claude Fable 5 · 02 The model family · 03 Specs at a glance · 04 Headline capabilities
  - 05 Early customer signals · 06 Use cases · 07 Developer experience · 08 Safety architecture

### Part 2: Overview

#### Slide 03 - What is Claude Fable 5

- **Layout**: Breathing statement page — one oversized assertion, short prose underneath, single orange rule; no cards
- **Title**: A new class above Opus
- **Core message**: Claude Fable 5 is the first Mythos-class model — a new tier above Claude Opus, built for the most demanding reasoning and long-horizon agentic work.
- **Content**:
  - Launched June 9, 2026, Fable 5 and its sibling Claude Mythos 5 share the same underlying model: one frontier intelligence, two release postures.
  - Fable 5 is the generally available release and carries additional safety measures for dual-use capabilities. Mythos 5 ships without those measures, to approved organizations only, through Project Glasswing.
  - Anthropic's most capable widely released model — for work above what prior models could do at all.

#### Slide 04 - The model family

- **Layout**: Asymmetric 7:3 — capability pyramid left, "Fable vs Mythos" side panel right
- **Title**: Where Fable 5 sits
- **Core message**: The Mythos class sits above Opus — and Fable 5 is its generally available face.
- **Visualization**: pyramid_chart (see VII)
- **Content**:
  - Pyramid tiers (top→bottom): **Mythos class** — Fable 5 · Mythos 5 ($10/$50 per MTok) / **Opus 4.8** — most capable Opus ($5/$25) / **Sonnet 4.6** — speed × intelligence balance ($3/$15) / **Haiku 4.5** — fastest, most cost-effective ($1/$5)
  - Side panel — same model, two postures: Fable 5 = GA + dual-use safety classifiers; Mythos 5 = no classifiers, Project Glasswing only
  - Opus 4.8 remains the default for general work; reach for Fable 5 when the task demands the highest available intelligence.

#### Slide 05 - Specs at a glance

- **Layout**: 2×3 KPI card grid
- **Title**: Frontier scale, predictable economics
- **Core message**: Fable 5 pairs a 1M-token context with flat, published pricing — less than half the price of Mythos Preview.
- **Visualization**: kpi_cards (see VII)
- **Content**:
  - **1M** token context window (default and maximum) · **128K** max output tokens per request
  - **$10** per MTok input · **$50** per MTok output
  - **5** platforms at GA (Claude API, Claude Platform on AWS, Bedrock, Vertex AI, Microsoft Foundry) · **30-day** data retention (Covered Model; no ZDR)

#### Slide 06 - Headline capabilities

- **Layout**: 2×3 icon card grid
- **Title**: What it's exceptional at
- **Core message**: The gains land above what prior models could do at all — don't evaluate it only on yesterday's workloads.
- **Visualization**: icon_grid (see VII)
- **Content**:
  - Long-horizon autonomy (clock-play) — multi-hour runs without correction; 15-minute single requests are normal
  - Software engineering (code) — months of work compressed into days; first-shot builds of well-specified systems
  - Knowledge work (chart-bar) — top finance-benchmark performance; end-to-end enterprise deliverables
  - Vision (eye) — state of the art on dense or degraded images; trained to crop, rotate, and inspect
  - Long context + memory (database) — effective across millions of tokens; notably better with a memory surface
  - Multi-agent orchestration (users-group) — dependable parallel sub-agents and sustained peer-agent communication

#### Slide 07 - Early customer signals

- **Layout**: 2×2 labeled cards, brand logo + quote per card
- **Title**: Breakthroughs, not increments
- **Core message**: Early-access teams report a new class of problems opening up, not incremental gains.
- **Visualization**: labeled_card (see VII)
- **Content**:
  - **Stripe** (simple-icons/stripe) — 50-million-line Ruby migration completed in one day; "months of work into days"
  - **Cursor** (simple-icons/cursor) — "opened up a class of long-horizon problems that were out of reach"
  - **GitHub** (simple-icons/github) — "exceeded previous benchmarks" on complex coding tasks
  - **Cognition** (text wordmark) — highest-scoring model on FrontierBench

### Part 3: Use cases

#### Slide 08 - Use cases

- **Layout**: Six numbered rows, two-column Z flow
- **Title**: Point it at the work you couldn't automate before
- **Core message**: Fable 5's use cases share one shape: long, ambiguous, high-stakes work that runs end to end.
- **Visualization**: vertical_list (see VII)
- **Content**:
  - 1 Autonomous coding agents — overnight refactors, large migrations, multi-repo changes (git-pull-request)
  - 2 Deep research & analysis — multi-source synthesis, financial modeling, legal review across 1M tokens (search)
  - 3 Enterprise deliverables — spreadsheets, decks, and documents produced as finished artifacts (file-text)
  - 4 Agent orchestration — coordinators managing fleets of parallel sub-agents (users-group)
  - 5 Vision-heavy workflows — degraded scans, screenshot-driven computer use, chart transcription (eye)
  - 6 Code review & debugging — higher recall and precision on real bugs; catches intermittent flakes (check)

#### Slide 09 - Spotlight: autonomous engineering

- **Layout**: Breathing hero-number page — "50M lines · 1 day" dominates, three short practice notes beneath a thin rule
- **Title**: Long-horizon coding is the breakout use case
- **Core message**: Stripe's 50-million-line Ruby migration finished in one day — the pattern: full task spec up front, high effort, self-verification.
- **Content**:
  - **50M lines · 1 day** — Stripe's Ruby migration, compressed from months
  - Give the full task specification in one well-specified first turn / Run at high or xhigh effort for long-horizon work / Have it establish its own verification harness as it builds

#### Slide 10 - Spotlight: enterprise knowledge work

- **Layout**: Top-bottom — parent container "Enterprise knowledge work, end to end" wrapping four module cards
- **Title**: From raw source to finished artifact
- **Core message**: One agent carries analysis from raw source material to a finished, shippable deliverable.
- **Visualization**: module_composition (see VII)
- **Content**:
  - Financial analysis (chart-bar) — benchmark-leading; models, valuations, audit support
  - Documents & decks (file-text) — spreadsheets, slides, and reports delivered as artifacts, not drafts
  - Research synthesis (search) — reads across the 1M-token window; multi-source verification
  - Legal review (scale) — contract and document review at production scale

### Part 4: Building & shipping

#### Slide 11 - Developer experience

- **Layout**: Four vertical pillars
- **Title**: Same Messages API, a few Fable-specific behaviors
- **Core message**: Integration is a model-ID swap plus three behaviors to plan for: always-on thinking, refusal fallback, and longer turns.
- **Visualization**: vertical_pillars (see VII)
- **Content**:
  - Thinking, always on (brain) — adaptive thinking is the only mode; control depth with `effort` (low → max); low effort often beats prior models' max
  - Refusals & fallback (refresh) — classifiers may return `stop_reason: "refusal"` (HTTP 200); server-side fallback retries on Opus 4.8; pre-output refusals are unbilled
  - Launch feature set (adjustments-horizontal) — effort, task budgets, memory tool, code execution, programmatic tool calling, compaction, vision
  - Where it runs (world) — Claude API, Claude Platform on AWS, Bedrock, Vertex AI, Microsoft Foundry; 30-day retention required

#### Slide 12 - Safety architecture

- **Layout**: Three numbered rows + footnote band
- **Title**: Frontier capability, shipped responsibly
- **Core message**: Fable 5 reaches general availability because three safeguards travel with it.
- **Visualization**: vertical_list (see VII)
- **Content**:
  - 1 Dual-use classifiers (shield-check) — detect and block harmful cybersecurity, bio/chem, and model-distillation requests; blocked queries fall back to Opus 4.8 instead of dead-ending
  - 2 Jailbreak resistance (shield-lock) — 1,000+ hours of external red-teaming produced no universal jailbreaks
  - 3 Data retention (lock) — 30-day policy; data used only for safety purposes, then deleted
  - Footnote: Mythos 5 is the same model with safeguards lifted for vetted defense and research partners via trusted-access programs.

#### Slide 13 - Closing

- **Layout**: Single column centered; lockup sign-off; faint radial wash
- **Title**: Start with your hardest problem
- **Core message**: The teams with the best results gave Fable 5 their hardest unsolved problems first.
- **Content**:
  - Model ID `claude-fable-5` — available today on the Claude API and all major cloud platforms
  - Give the full spec up front · sweep effort levels · let it delegate and self-verify
  - anthropic.com/news/claude-fable-5-mythos-5

---

## X. Speaker Notes Requirements

- One note file per page in `notes/`, filenames matching SVG names (`01_cover.svg` → `notes/01_cover.md`)
- Total duration ≈ 10 minutes; style: conversational-professional (brand voice: we/you, no emoji, spell out on first use); purpose: inform
- `notes/total.md` uses `#` headings; split files contain no `#` lines

---

## XI. Technical Constraints Reminder

### SVG Generation Must Follow:

1. viewBox: `0 0 1280 720`
2. Background uses `<rect>` elements
3. Text wrapping uses `<tspan>` (`<foreignObject>` FORBIDDEN)
4. Transparency uses `fill-opacity` / `stroke-opacity`; `rgba()` FORBIDDEN
5. FORBIDDEN: `mask`, `<style>`, `class`, `foreignObject`, `textPath`, `animate*`, `script`
6. Text characters: raw Unicode for typography (`—`, `·`, `→`, `×`); XML reserved chars escaped (`&amp;` etc.); HTML named entities FORBIDDEN
7. `marker-start`/`marker-end` only with `<marker>` in `<defs>`, `orient="auto"`, triangle/diamond/circle shapes
8. `clipPath` only on `<image>` elements — not applicable here (no images)

### PPT Compatibility Rules:

- `<g opacity="...">` FORBIDDEN — set opacity per child element
- Inline styles only; external CSS and `@font-face` FORBIDDEN
- Brand typefaces note: Styrene A / Anthropic Sans require install or PPTX embed; Arial fallback is the PPT-safe floor
