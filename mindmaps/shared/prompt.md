Act as an expert visual content designer specializing in animated HTML infographics and mind maps for memorization & quick revision.

---

## INPUT
[PASTE YOUR YOUTUBE VIDEO SUMMARY / TRANSCRIPT / NOTES HERE]

---

## YOUR TASK — 3 STEPS (run in parallel)

### STEP 1 — Extract Keywords & Concepts
From the input, extract:
- Major ideas & core thesis
- Subtopics & frameworks
- Step-by-step processes or workflows
- Tools, technologies, commands mentioned
- Pitfalls / common mistakes
- Metrics / KPIs / key numbers
- Actionable recommendations
- Any other significant data points

Keep extractions concise — 1 to 5 words each.

---

### STEP 2 — Build the Animated HTML Mind Map

Generate a single self-contained HTML file with the following specifications:

#### 🎨 DESIGN SYSTEM
- **Theme:** Light warm only — base color `#F7F6F2`, cards `#FFFFFF`, surface2 `#F0EEE8`
- **Fonts:** Outfit (400–900 weight) for display text + JetBrains Mono for code/labels/KPIs — import from Google Fonts
- **Color coding:** Each card/section gets its own distinct accent color (teal, violet, orange, blue, rose, amber, green, sky). Use light bg, medium border, strong text for each accent.
- **No dark theme** anywhere

#### 🏗️ LAYOUT RULES
- `max-width: 960px`, centered, `padding: 28px 18px`
- Main content in a `display: grid; grid-template-columns: 1fr 1fr` layout
- Full-width cards use `grid-column: 1 / -1`
- **Zero horizontal scroll** — flow diagrams must use `flex: 1 1 0` (not fixed widths) so all steps fit in one row without overflow
- **Mobile responsive:** at ≤640px collapse to single column; flow diagrams collapse to `grid-template-columns: 1fr 1fr` at ≤700px, `1fr` at ≤360px; KPIs go `repeat(2, 1fr)` on mobile
- No page headers, footers, or "Mind Map · Quick Revision" style badges anywhere in the page body

#### ✨ MANDATORY ANIMATION TECHNIQUES (apply all)

**Background layer:**
- Aurora Background: 3 absolutely-positioned color blobs, `filter: blur(90px)`, `opacity: 0.14`, CSS `@keyframes` floating animation (no JS mouse tracking)
- Noise Texture Overlay: SVG `feTurbulence` fractal noise as `body::after` fixed overlay, `opacity: 0.025`
- Floating Token Particles: HTML5 canvas fixed to viewport, 20 domain-specific text tokens (e.g. `skill.md`, `/cmd`, `→`, `[]`, `ctx`) drifting upward with `requestAnimationFrame`
- Parallax Aurora: on `scroll` event (`passive: true`), shift blobs at different rates (`translateY` only — no mouse X/Y)
- Scroll Color Shift: on `scroll`, apply `hue-rotate(0–16deg)` to `documentElement.style.filter`

**Header:**
- Chip Float: badge `@keyframes` bobs up/down 5px, 3s loop
- Pulsing Dot + Blinking Status Dot: 8px dot with expanding ring via `::after` pseudo-element
- Gradient Text + Shift: H1 uses `background: linear-gradient(...)`, `background-size: 300%`, `@keyframes` animates `background-position` over 6s
- Hero Stagger: badge → H1 → subtitle each have staggered `animation-delay`

**KPI cards:**
- Card Bar: 3px gradient `::before` top stripe per accent color
- Scan Line Continuous: `::after` light sheen sweeps up each KPI card every 4s, staggered by 1s offsets
- Lift on KPI: `translateY(-6px) rotate(1.2deg) scale(1.03)` on `:hover` with colored `box-shadow`
- Counter: JS `requestAnimationFrame` counts numeric KPI values up from 0 on page load
- Click Ripple: on `click`, inject a `div` that scales from 0 to 12× then removes itself

**Cards:**
- Card Tint: diagonal `linear-gradient(145deg, white 55%, accent-bg)` per accent
- Card Entrance Cascade: `opacity: 0` by default, IntersectionObserver adds `.visible` class — odd cards slide from left, even from right
- Lift + Glow on Hover: `translateY(-4px)` + colored `box-shadow` per accent
- Icon Rotate: `.card-icon` does `rotate(-8deg) scale(1.12)` on card `:hover`

**List items:**
- Item Slide: each `.item` starts `opacity:0; transform: translateX(-14px)`, animates in with staggered delays
- Dot Pop: each indicator dot springs in with `scale(0.3) rotate(-30deg)` → `scale(1)` via `cubic-bezier(.34,1.56,.64,1)`
- Check Rotate Hover: dot rotates `10deg` and scales on item hover

**Tags:**
- Tag Bounce: spring entrance via `cubic-bezier(.34,1.56,.64,1)` from scale 0.4
- Fill Sweep: `::before` pseudo scaleX fills tag on hover
- Colored glow `box-shadow` on hover per tag accent

**Flow diagrams:**
- Flowing Dashed Arrows: SVG arrows between steps using `stroke-dasharray` + `@keyframes` animating `stroke-dashoffset` so the dashes appear to flow
- Moving Dot on Arrow: inside each SVG arrow, add `<circle>` with `<animateMotion>` following an `<mpath>` along the arrow path — dot travels in arrow direction with staggered `begin` delays per arrow
- Step Highlight: `::before` underline at step bottom, `scaleX(0)` → `scaleX(1)` on hover
- Numbered Badge: small rounded square (ByteByteGo-style) with step number in monospace font
- Step hover: `translateY(-6px)` + colored shadow

**Rule/highlight boxes:**
- Border Flow: animated `box-shadow` cycles through 4 accent colors every 4s
- Bounce Icon: icon inside rule box animates `translateY + rotate` loop

**Code references:**
- Code Pill: inline `<span class="pill">` with monospace font, accent color text, subtle border

#### 🚫 NEVER INCLUDE THESE (cause UI sluggishness):
- Custom Cursor (orange dot + lagging ring following mouse)
- Spotlight effect tracking mouse X/Y inside cards  
- Magnetic Cursor (element scaling near mouse)
- Shockwave Hover expanding from cursor position
- 3D Card Tilt based on mouse X/Y coordinates
All five require continuous `mousemove` event polling — this causes the "stuck" laggy feel especially on mobile.

#### 📐 STRUCTURE (in this order):
1. Fixed aurora blobs + noise overlay
2. Fixed canvas (token particles)
3. `.page` wrapper (z-index above canvas)
4. Header: badge (chip float + pulsing dot) → animated gradient H1 → mono subtitle
5. KPI row (4 cards, scan line, counter, card bar)
6. Optional: 3-column concept/pillar chips
7. 2-column main grid of content cards (with full-width cards as needed)
8. Flow diagram card (full-width, no horizontal scroll)
9. No footer

---

### STEP 3 — Output Requirements
- Single self-contained `.html` file — no external JS libraries, no separate CSS files
- All Google Fonts loaded via `<link>` in `<head>`
- All animations CSS-only where possible, JS only for: canvas particles, scroll listeners (passive), IntersectionObserver, counter, click ripple
- Valid, clean HTML5
- Works offline except for Google Fonts
- File must render correctly on Chrome, Safari, Firefox
- Mobile-first responsive (test mentally at 360px, 640px, 960px widths)
