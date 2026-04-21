# CampusX Mind Maps — Project Notes

## Project Structure

```
/
├── home.html                        ← Index of all mind maps (latest first)
├── PROJECT_NOTES.md                 ← This file
├── ai_stay_updated_mindmap.html     ← Legacy standalone (dark theme) — kept for reference
└── mindmaps/
    ├── shared/
    │   ├── base.css                 ← Shared design system (MUST remain backward compatible)
    │   └── mindmap.js               ← Shared JS runtime (particles, counters, scroll, ripple)
    ├── 01_ai_stay_updated.html
    ├── 02_claude_code_skills.html
    ├── 03_slash_commands.html
    ├── 04_plan_mode_ultraplan.html
    └── 05_rag_explained.html
```

---

## Mind Map Log (newest first)

| # | File | Topic | Date |
|---|------|--------|------|
| 05 | `mindmaps/05_rag_explained.html` | Retrieval Augmented Generation (RAG) | Apr 2026 |
| 04 | `mindmaps/04_plan_mode_ultraplan.html` | Plan Mode & Ultraplan in Claude Code | Apr 2026 |
| 03 | `mindmaps/03_slash_commands.html` | Custom Slash Commands | Apr 2026 |
| 02 | `mindmaps/02_claude_code_skills.html` | Claude Code Skills Guide | Apr 2026 |
| 01 | `mindmaps/01_ai_stay_updated.html` | Stay Updated in AI Without Burning Out | Apr 2026 |

---

## Shared Design System (`mindmaps/shared/`)

### base.css — Design Tokens
- **Palette:** Warm light (#F7F6F2 bg, #FFFFFF surface, #F0EEE8 surface2)
- **Fonts:** Outfit (display) + JetBrains Mono (code/KPIs)
- **Accents (10):** `--or` orange · `--am` amber · `--te` teal · `--bl` blue · `--vi` violet · `--ro` rose · `--gr` green · `--sk` sky · `--li` lime · `--sl` slate
- **Components:** aurora, noise, canvas, header, KPI row, chips, grid, cards, items, tags, rule box, flow diagram, compare/anatomy, code pill

### mindmap.js — Exported API
```js
MindMap.init(tokens[], hues[], maxDeg?)   // call all at once
MindMap.initParticles(tokens, hues)       // floating token canvas
MindMap.initCounters()                    // [data-count] KPI animation
MindMap.initScrollReveal()                // IntersectionObserver card entrance
MindMap.initRipple()                      // click ripple on kpi/cards
MindMap.initParallax()                    // aurora scroll parallax
MindMap.initColorShift(maxDeg)            // scroll hue-rotate
```

### Backward Compatibility Rules
- NEVER remove existing CSS variables or class names from base.css
- NEVER change the MindMap public API signatures in mindmap.js
- New additions are always additive (new classes/variables only)
- All 5 existing mindmaps must render correctly after any shared file change

---

## Per-Page Pattern (each new mindmap)

```html
<!-- 1. Link shared CSS -->
<link rel="stylesheet" href="shared/base.css">

<!-- 2. Page-specific <style> block: -->
<!-- - Aurora blob colors/positions -->
<!-- - Badge/dot/H1 gradient accent overrides -->
<!-- - KPI nth-child accent vars -->
<!-- - Chip accent vars (mc-1, mc-2, mc-3) -->
<!-- - Card accent vars (c-XX pattern) -->
<!-- - Flow color vars (mm-flow-XX) -->
<!-- - Any page-unique components -->

<!-- 3. Load shared JS at bottom -->
<script src="shared/mindmap.js"></script>
<script>
  MindMap.init(
    ['domain', 'tokens', '→', '[]', 'etc'],   // domain-specific floating tokens
    [hue1, hue2, hue3, hue4, hue5]             // HSL hues for particle colors
  );
</script>
```

---

## KPI Counter Syntax
- `data-count="42"` → counts up from 0 to 42
- `data-count="skip"` → leaves text as-is (for labels like "RAG", "/cmd", "∞")

---

## Content Structure per Mind Map
1. Header: badge → H1 → mono subtitle
2. KPI row (4 cards)
3. Concept chips (3 columns)
4. 2-column card grid:
   - Problem/limitations card (rose/red)
   - Alternative/comparison card (orange/amber)
   - Core concept card (teal/green) + rule box
   - Comparison table card (green)
   - Full-width flow diagram (4–7 steps)
   - Deep-dive / detail card (violet/full-width)
   - Use cases card (amber)
   - Benefits/metrics card (sky/blue)

---

## Notion Links
_Update these when Notion pages are created:_
- 05 RAG: `#` (placeholder)
- 04 Plan Mode: `#` (placeholder)
- 03 Slash Commands: `#` (placeholder)
- 02 Claude Code Skills: `#` (placeholder)
- 01 AI Stay Updated: `#` (placeholder)
