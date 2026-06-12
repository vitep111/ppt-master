# Execution Lock

## canvas
- viewBox: 0 0 1280 720
- format: PPT 16:9

## colors
- bg: #FFFFFF
- surface: #F8FAFC
- primary: #D97757
- accent: #4A90D9
- secondary_accent: #10B981
- warning: #EF4444
- text: #191919
- text_secondary: #64748B
- text_tertiary: #94A3B8
- border: #E2E8F0

## typography
- font_family: "Anthropic Sans", "Helvetica Neue", Arial, sans-serif
- title_family: "Styrene A", "Helvetica Neue", Arial, sans-serif
- body_family: "Anthropic Sans", "Helvetica Neue", Arial, sans-serif
- code_family: Consolas, "Courier New", monospace
- body: 18
- title: 32
- subtitle: 22
- annotation: 13
- cover_title: 64
- section_title: 40
- hero_number: 48
- footnote: 11

## icons
- library: tabler-outline
- stroke_width: 2
- brand_library: simple-icons
- inventory: list-check, sparkles, target, stack-2, clock-play, hourglass, code, git-pull-request, terminal-2, chart-bar, file-text, eye, database, users-group, robot, search, microscope, flask, scale, brain, adjustments-horizontal, gauge, refresh, bolt, shield-check, shield-lock, lock, coin, world, calendar-event, rocket, arrow-right, check, message-chatbot
- brand_inventory: stripe, github, cursor

## page_rhythm
- P01: anchor
- P02: anchor
- P03: breathing
- P04: dense
- P05: dense
- P06: dense
- P07: dense
- P08: dense
- P09: breathing
- P10: dense
- P11: dense
- P12: dense
- P13: anchor

## page_charts
- P02: agenda_list
- P04: pyramid_chart
- P05: kpi_cards
- P06: icon_grid
- P07: labeled_card
- P08: vertical_list
- P10: module_composition
- P11: vertical_pillars
- P12: vertical_list

## brand_assets
- mark: templates/anthropic_mark.svg (inline paths, fill #D97757, 24×24 viewBox)
- lockup: templates/anthropic_claude_lockup.svg (inline paths, mark #D97757 + wordmark #191919, 112×24 viewBox)

## forbidden
- Mixing icon libraries
- rgba()
- `<style>`, `class`, `<foreignObject>`, `textPath`, `@font-face`, `<animate*>`, `<script>`, `<iframe>`, `<symbol>`+`<use>`
- `<g opacity>` (set opacity on each child element individually)
- HTML named entities in text (`&nbsp;`, `&mdash;`, `&copy;` …) — write raw Unicode; XML reserved chars escaped as `&amp; &lt; &gt; &quot; &apos;`
