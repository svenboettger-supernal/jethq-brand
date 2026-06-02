# JetHQ brand prompt

Standalone brand brief for an AI tool building a JetHQ-themed surface — the JetHQ marketing site, a charter quote tool, a fleet/availability dashboard, an investor or operator deck, a client PDF (trip itinerary, sourcing report, quote pack), an email template, or any artifact representing JetHQ externally. Apply these values directly — no token system or design-system install required.

---

## Brand foundation — read this before touching a color or a font

JetHQ is a private aviation brokerage and charter business. The brand is **not** about airplanes; it is about a small group of people who quietly arrange a complicated, high-trust movement of someone important from one point on the map to another. Every design decision answers to that promise.

- **Archetype:** Navigator / Steward. Calm, technical, unhurried, map-literate. Never Hero, never Disruptor, never Lifestyle-Influencer.
- **Enemy:** the chrome-and-cobalt corporate-aviation aesthetic — stock photos of suited men shaking hands on a tarmac, glossy hero shots of a tail number against a sunset, "luxury" used as an adjective on every page. JetHQ positions against that posture. Restraint is the differentiator.
- **Posture:** premium and quiet. Closer to a yacht broker's letterhead, a topographic survey, or a vintage navigation chart than to an airline brochure. Confidence reads as understatement; the brand is the **HQ**, not the jet.
- **The unifying brief:** be the most credible voice in private aviation by behaving like a quiet professional, not a salesperson.

If a design decision makes the brand louder, faster, glossier, or more obviously "luxury," it is wrong — regardless of how well-executed it is in isolation. Quiet luxury, not loud luxury.

---

## Output context — classify before you apply anything

Read the user's request and decide which output you are building:

- **Marketing surface** — public-facing pages for JetHQ.com; investor or operator decks; one-page tear sheets; client-facing trip PDFs, quote packs, sourcing reports, post-flight summaries. **Editorial mode applies in full.** Skip status colors and form/input chrome unless the page actually contains a form.
- **App or prototype (broker/ops tooling, charter quote builder, fleet dashboard)** — the working software used internally by brokers, ops, and accounts, or by repeat clients booking trips. **All sections apply, including status colors and tabular-figure rules.**
- **Internal document** — Notion-style notes, decision memos, ops docs, deal post-mortems. Apply only typography, page surfaces, and surface neutrals. No buttons, no status badges, no charts unless the content needs them.

If unsure, ask before applying status colors or form/input guidance. **Never invent UI controls — buttons, badges, alerts, status indicators, forms — just to apply the colors below.** Use only what the content actually requires.

---

## Aesthetic

Editorial and map-inspired — screens should read like the cover of a topographic survey, the inside of a flight planning binder, or the title page of a private-client trip dossier. Restraint as the organizing principle: one warm gold identity color, one deep charcoal ground, one disciplined teal accent reserved for active state. Generous negative space on the dark ground. Hierarchy comes from scale, spacing, and the small-caps gold rules at the top and bottom of the layout — not from heavy color contrast or busy chrome.

Asymmetric balance over centered stacks. Type does the heavy lifting; the topographic line motif is the only meaningful piece of ornament, and even it appears at low opacity until it has earned the foreground.

The site of a brokerage at this tier should age slowly on purpose. Avoid every signal that will look dated in five years — chrome textures, animated tail-fin gradients, autoplay aerial b-roll with cinematic music, "Book in 60 seconds" urgency banners, glassmorphism, illustrated airplane mascots.

---

## The mark

JetHQ's identity mark is the **winged-globe monogram** paired with the **JETHQ** wordmark — "JET" set in a light serif, "HQ" set in a gold serif. Treat it as an insignia, not a tech logo.

- **Two-color rule.** The lockup is always a two-color treatment: ivory/white + gold on dark grounds; deep charcoal + gold on light grounds. Never paint the entire lockup gold, never paint the entire lockup white, never apply gradients. If a true single-color treatment is required, use solid charcoal with the gold "HQ" desaturated to charcoal of equal weight — never re-tinted gold variants.
- **Wing-globe orientation.** The winged globe sits to the left of the wordmark on horizontal lockups. It is never stretched, rotated, mirrored, recolored, or sheared. The wings are horizontal hairlines flanking a circle — never thicken them, never animate them.
- **Minimum sizes.** Full lockup (winged globe + wordmark) ≥ 140px wide. Globe alone (favicon, social avatar) ≥ 32px square. Below that, use the globe glyph alone — never the wordmark detached from the globe.
- **Clear space.** Reserve at least the cap height of the "J" in JET around the entire lockup. Nothing crosses that boundary — not a topographic line, not a corner-arrow marker, not adjacent type.
- **Never alter.** The logo is never stretched, rotated, recolored, outlined, embossed, drop-shadowed, or set inside a containing shape (no "logo in a circle," no "logo in a square card").

---

## Typography

Two families only — never more than two fonts in a single design. Display serif for headings and the wordmark; clean sans for body, navigation, and all dense data.

| Role | Family | Weights | Used for |
|------|--------|---------|----------|
| Display serif | Mrs Eaves (Adobe Fonts) — fallback: **EB Garamond** (Google Fonts) | 400, 500 + small-caps | h1, h2, section headings, page titles, the "JET" half of the wordmark, hero copy, pull quotes |
| Sans (UI + body) | Gotham (paid) — fallback: **Inter** (Google Fonts) | 300 (Light), 500 (Medium) | h3–h6, body, navigation, captions, tables, all dense data |
| Mono | JetBrains Mono | 400 | tail numbers, ICAO codes, file refs, code |

If brand-licensed Mrs Eaves and Gotham are available (Adobe Fonts for Mrs Eaves; a licensed Gotham CDN for Gotham), use them. If not, the fallbacks are mandatory and produce a faithful look — they are not "good enough," they are part of the brand system. Alternatives listed on the guideline sheet (Arial, Times New Roman, Merriweather) are document-of-record substitutes only — acceptable in a Word doc or Outlook email, never on a web surface.

Load via Google Fonts or your framework's font system. Set `font-display: swap`. Never use raw `<link>` tags or `@import` in a component file when a framework font loader is available.

```css
/* Fallback stack — when Mrs Eaves / Gotham licenses are unavailable */
@import url('https://fonts.googleapis.com/css2?family=EB+Garamond:wght@400;500;600&family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400&display=swap');

:root {
  --font-display: 'Mrs Eaves OT', 'mrs-eaves-roman-all-petite-caps', 'EB Garamond', Georgia, serif;
  --font-sans:    'Gotham', 'Gotham SSm', 'Inter', system-ui, -apple-system, sans-serif;
  --font-mono:    'JetBrains Mono', 'SF Mono', ui-monospace, monospace;
}
```

### Type scale

| Element | Size | Line height | Weight | Family | Notes |
|---------|------|-------------|--------|--------|-------|
| Display title (e.g. "Brand Guidelines", hero) | 56–72px | 1.05 | 400 | Display serif | Large serif, mixed weight ("Brand" in display weight, "Guidelines" in italic display weight, per the guideline cover) |
| h1 (marketing) | 44px | 1.15 | 400 | Display serif | Letter-spacing default; never bold |
| h2 (marketing) | 32px | 1.2 | 400 | Display serif | |
| Section heading (small-caps gold rule) | 13–14px | 1.3 | 500 | Display serif, **all small-caps** | `letter-spacing: 0.14em`; gold (#b9986d); always paired with a corner-arrow marker |
| Subheading (next to a heading) | 22px | 1.25 | 500 | Sans | Used directly beneath a serif HEADING — see "Heading + Subheading pattern" |
| h1 (app) | 28px | 1.25 | 500 | Sans Medium | |
| h2 (app) | 22px | 1.3 | 500 | Sans Medium | |
| h3 | 18–20px | 1.35 | 500 | Sans Medium | |
| h4 | 16px | 1.4 | 500 | Sans Medium | |
| Body | 14–15px | 1.55 | 300 (Light) | Sans | Gotham Light is the default body weight per the guideline |
| Small / metadata / nav labels | 12–13px | 1.4 | 500 | Sans Medium | Used for nav items like "Logo · Font · Color · Visual" |
| Mono / tail number | 13–14px | 1.4 | 400 | Mono | Always uppercase for tail numbers and ICAO codes |

### Heading + Subheading pattern (signature device)

JetHQ's signature type lockup is a **serif HEADING in gold** stacked directly above a **sans SUBHEADING in white**, drawn from the guideline page. Reproduce it exactly where a section needs emphasis:

```html
<div class="section-title">
  <h2 class="section-title__heading">HEADING</h2>
  <p class="section-title__subheading">SUBHEADING</p>
</div>
```

```css
.section-title__heading {
  font-family: var(--font-display);
  font-size: 32px;
  font-weight: 400;
  letter-spacing: 0.04em;
  color: var(--brand-gold);
  margin: 0 0 0.15em 0;
  text-transform: uppercase;
}
.section-title__subheading {
  font-family: var(--font-sans);
  font-size: 22px;
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--text-on-dark);
  margin: 0;
  text-transform: uppercase;
}
```

### Section labels (gold small-caps rule)

Anywhere a section opens — a card, a panel, a deck slide, a PDF section break — use the **small-caps gold label**. It is the spine of the JetHQ hierarchy.

```css
.label-gold {
  font-family: var(--font-display);
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 0.14em;
  color: var(--brand-gold);
  text-transform: uppercase;
}
```

Always paired with a **corner-arrow marker** to the right (see Decorative motifs).

### Letter-spacing

- Display serif headings: default tracking; never tighten below `-0.005em`. Mrs Eaves wants room.
- Small-caps section labels: `letter-spacing: 0.14em`.
- Body and UI: default tracking.
- Mono (tail numbers, ICAO): default tracking, uppercase.

### Numerals — tabular figures in any dense data

Anywhere numbers stack — a quote breakdown, a fleet table, a flight schedule, a sourcing comparison — use tabular figures so columns align:

```css
font-variant-numeric: tabular-nums;
font-feature-settings: "tnum" 1;
```

Apply on `table`, `.quote`, `.itinerary`, `.fleet`, `.amount`, `pre`, `code`, and any data-bearing component. Prose numbers ("over twelve years in operation") use default proportional figures and are fine.

### Type rules from the guideline (verbatim spirit)

- **Maintain a clean and professional hierarchy in text sizes.**
- **Avoid using more than two fonts per design.** Display serif + sans. That is the entire system.
- **Keep text contrast high for readability.** Especially on the charcoal ground — body text is `#cfcfcf` light gray, not white-at-low-opacity.

---

## Colors

All values are HSL components — paste inside `hsl()` to use as a CSS color. HEX values follow the guideline sheet exactly.

### The five-swatch system

| # | Role | HEX | HSL | Where |
|---|------|-----|-----|-------|
| 1 | **Brand Gold** (primary identity) | `#b9986d` | `hsl(34 36% 58%)` | The "HQ" in the wordmark; section headings; small-caps labels; gold rule under nav; gold full-width bar at the bottom of every page; topographic line accents on dark grounds |
| 2 | **Deep Ink** (deepest dark) | `#262626` | `hsl(0 0% 15%)` | Deepest panels, footers on dark surfaces, PDF cover backgrounds, text on light surfaces |
| 3 | **Charcoal Slate** (signature ground) | `#414649` | `hsl(204 5% 27%)` | **The default page background.** Every marketing surface, deck, and PDF cover sits on this. Cards on dark sit one step deeper (Deep Ink) |
| 4 | **Mist** (body text on dark) | `#cfcfcf` | `hsl(0 0% 81%)` | Body copy on dark surfaces; quiet hairline dividers; the "JET" half of the wordmark on dark |
| 5 | **Signal Teal** (accent — reserved) | `#3dabaf` | `hsl(182 47% 46%)` | **Reserved for status, active state, and selected — never decorative.** See "Action and accent rules" below |

### Page surfaces

The default JetHQ surface is **dark**. The brand was designed for charcoal grounds — light surfaces are the exception, used for documents that will be printed or for legibility-critical screens (long-form articles, dense tables, regulatory pages).

| Role | Value | Where |
|------|-------|-------|
| Editorial dark (default page background) | `hsl(204 5% 27%)` — `#414649` | Default for every JetHQ marketing surface, deck, and PDF |
| Card / panel on dark | `hsl(0 0% 15%)` — `#262626` | Cards and panels sit one step deeper than the page, not lighter |
| Card hover / elevated panel on dark | `hsl(0 0% 18%)` | A barely-perceptible lift |
| Editorial light (fallback, print, long-form) | `hsl(38 18% 96%)` | Warm ivory, never pure white. Pure white is for the inside of the lockup containment box only |
| Card on light | `hsl(0 0% 100%)` | Pure white sits on the ivory with a quiet hue gap |

The page is charcoal; cards on dark go **darker, not lighter**. This is the opposite of most SaaS conventions and is core to the JetHQ feel — the layout reads like ink-on-paper, not pixels-on-screen.

### Action and accent rules (read this twice)

JetHQ has three colors that signal interaction or state. They are strictly partitioned:

1. **Brand Gold (`#b9986d`)** — **identity**, not interaction. Use for the wordmark, section headings, small-caps labels, the top nav hairline rule, the bottom gold bar, topographic line accents, and a single underline beneath an active nav item. **Never paint a button gold.** Never paint a chart series gold. Gold is the family crest — it dilutes the moment it becomes a generic UI color.
2. **Mist white-ish (`#cfcfcf`)** — **default text and chrome** on dark grounds.
3. **Signal Teal (`#3dabaf`)** — **reserved for active state, selected, and informational status only.** A teal focus ring. A teal "selected" indicator on a tab. A teal "this option is currently chosen" pill. **Never a decorative accent. Never a hero color. Never a chart series default.** Once teal appears on a decorative element, its meaning as a state indicator is broken everywhere else.

### Action color — interactive elements

JetHQ's primary button is a **gold-outlined gold-text button on dark**, or a **filled charcoal button with gold border on light**. Filled-gold buttons exist but are rare — used only for a single primary CTA per page (e.g. "Request a Quote" in the hero).

| Role | Value |
|------|-------|
| Primary button bg (filled, rare — hero CTA only) | `hsl(34 36% 58%)` — `#b9986d` |
| Primary button text on filled gold | `hsl(0 0% 15%)` — `#262626` |
| Primary button hover (filled) | `hsl(34 36% 50%)` — slightly deeper gold |
| Default button bg on dark (outline) | transparent |
| Default button border on dark | `hsl(34 36% 58%)` — gold |
| Default button text on dark | `hsl(34 36% 58%)` — gold |
| Default button hover on dark | `hsl(34 36% 58% / 0.10)` background tint |
| Default button bg on light | transparent |
| Default button border on light | `hsl(0 0% 15%)` — charcoal |
| Default button text on light | `hsl(0 0% 15%)` |
| Ghost on dark | transparent, `hsl(0 0% 81% / 0.30)` border, mist text |
| Focus ring (everywhere) | `hsl(182 47% 46%)` — Signal Teal, 2px, 2px offset |
| Inline link (on dark) | `hsl(34 36% 58%)` with `border-bottom: 1px solid currentColor` at 40% alpha |
| Inline link (on light) | `hsl(0 0% 15%)` with gold underline |

**Buttons are rectangles with a 4px radius, not pills.** Pills read as consumer-app casual and break the premium brokerage posture. The only pill-radius elements are status indicators and avatars.

### Surface neutrals

Borders on dark grounds are mist at low alpha — this reads as a true hairline on charcoal. Use the alpha values directly; do not substitute a solid gray.

| Role | Value |
|------|-------|
| Foreground (body text on dark) | `hsl(0 0% 81%)` — `#cfcfcf` |
| Foreground (body text on light) | `hsl(0 0% 15%)` — `#262626` |
| Muted foreground (secondary text, dark) | `hsl(0 0% 65%)` |
| Muted foreground (secondary text, light) | `hsl(204 5% 38%)` |
| Placeholder text | `hsl(0 0% 55%)` |
| Border (default, dark) | `hsl(0 0% 81% / 0.14)` |
| Border (input / field, dark) | `hsl(0 0% 81% / 0.18)` |
| Border (strong / hover, dark) | `hsl(0 0% 81% / 0.28)` |
| Border (default, light) | `hsl(0 0% 15% / 0.12)` |
| Hairline (the gold rule under nav, the gold bottom bar) | `hsl(34 36% 58%)` — solid gold, 1px (nav) or 12px (bottom bar) |

### Status colors (app / prototype mode only)

**Skip this section entirely if you are building a marketing surface, deck, or PDF.** Status colors exist for success/warning/error/info feedback in the broker/ops tooling. **They are semantic-only — never use a status color as a decorative or brand accent**; a status hue must always mean its state.

JetHQ status colors are calibrated to sit on the charcoal ground without clashing with the gold identity. Backgrounds are deeper, more muted than typical web defaults.

| Status | Background (on dark) | Text / Icon | Border |
|--------|---------------------|-------------|--------|
| Success | `hsl(150 30% 18%)` | `hsl(150 50% 70%)` | `hsl(150 30% 32%)` |
| Warning | `hsl(34 40% 22%)` | `hsl(34 60% 72%)` | `hsl(34 40% 38%)` |
| Error   | `hsl(4 40% 22%)`   | `hsl(4 60% 72%)`   | `hsl(4 40% 38%)`   |
| Info (uses Signal Teal) | `hsl(182 40% 18%)` | `hsl(182 47% 70%)` | `hsl(182 47% 38%)` |

Info status and Signal Teal are the same hue family — this is intentional. Teal means "currently active / informational" everywhere it appears.

### Visualization palette

Eight calibrated identity colors for charts, fleet category tags, broker avatars, sourcing comparison grids, and entity markers on maps. Three permitted uses: (1) data visualization — chart, quote-breakdown, sourcing-comparison series fills; (2) identity markers — broker avatars, fleet categorical tags tied to a specific aircraft class or operator; (3) brand-decorative accents on long-form surfaces. This is the accent palette — reach for it instead of teal, used sparingly.

Never use viz colors on UI controls (buttons, alerts, status indicators, badges). Never use **Brand Gold** or **Signal Teal** as a chart series — they have other jobs.

**Chart series assignment.** Single-series charts use index 0 (Slate Blue). Multi-series charts cycle 0 → 7 before any reuse.

| Index | Name | Base | Background tint (on dark) | Foreground on base |
|-------|------|------|---------------------------|--------------------|
| 0 | Slate Blue   | `hsl(210 22% 56%)` | `hsl(210 18% 22%)` | light — `hsl(0 0% 96%)` |
| 1 | Warm Tan     | `hsl(34 28% 62%)`  | `hsl(34 22% 22%)`  | dark — `hsl(0 0% 15%)`  |
| 2 | Burnt Sienna | `hsl(18 42% 50%)`  | `hsl(18 28% 22%)`  | light — `hsl(0 0% 96%)` |
| 3 | Moss         | `hsl(95 18% 44%)`  | `hsl(95 14% 22%)`  | light — `hsl(0 0% 96%)` |
| 4 | Aubergine    | `hsl(295 14% 42%)` | `hsl(295 12% 22%)` | light — `hsl(0 0% 96%)` |
| 5 | Sand         | `hsl(45 28% 64%)`  | `hsl(45 22% 22%)`  | dark — `hsl(0 0% 15%)`  |
| 6 | Sky          | `hsl(200 32% 60%)` | `hsl(200 24% 22%)` | dark — `hsl(0 0% 15%)`  |
| 7 | Fog          | `hsl(210 6% 56%)`  | `hsl(210 4% 22%)`  | dark — `hsl(0 0% 15%)`  |

Index 7 (Fog) is the low-chroma "uncategorized / unknown" slot. Assign avatar colors by stable position in the list (`index = position % 8`) — never by hashing the name.

For more than 8 categories, cycle back with lightened, desaturated versions:

```css
color-mix(in srgb, hsl(var(--color-viz-N)) 60%, white)
```

---

## Decorative motifs

JetHQ has exactly **two** sanctioned decorative devices. Both come straight from the guideline sheet. Nothing else is invented or imported.

### 1. Topographic contour lines (the signature motif)

Thin gold contour lines, like elevation rings on a survey map or flight-path isobars on a wind chart. They evoke terrain, navigation, and the quiet precision of route planning — the work behind a trip, not the trip itself.

**When to use:**
- **Background texture** on hero sections, dark cover surfaces, PDF covers, and the visual-accent block of any section. Always at low opacity (12–25%) on the charcoal ground, gold lines only.
- **Feature blocks** — a dedicated rectangular panel of denser topographic lines, used once or twice per page as a stand-alone visual element (the guideline shows this in the upper-right "VISUAL ACCENTS" block).
- **Section dividers** — a single horizontal contour fragment can replace a divider line between two sections.

**When NOT to use:**
- Never on light surfaces unless rendered in deep charcoal at low opacity — gold lines on ivory disappear.
- Never inside cards or panels at high opacity — they fight body copy.
- Never over a photograph.
- Never animated. Never parallax-scrolled. Never gradient-tinted.
- **Never more than two topographic elements per visible viewport.** If the viewport already has a background texture and a feature block, do not add a third. Restraint is the point.

```css
.topo-bg {
  /* Layered SVG or PNG of gold contour lines on transparent */
  background-image: url('/topographic-lines.svg');
  background-size: cover;
  background-position: center;
  opacity: 0.18; /* never above 0.25 on dark ground */
  pointer-events: none;
}

.topo-feature-block {
  /* A bordered panel of denser contour lines */
  border: 1px solid hsl(34 36% 58% / 0.30);
  background-color: hsl(0 0% 15%);
  background-image: url('/topographic-lines-dense.svg');
  background-size: cover;
  aspect-ratio: 4 / 3;
}
```

### 2. Corner-arrow markers (↙)

Small white (or charcoal on light) arrow brackets pointing toward the bottom-left, placed at the **top-right corner of every section heading block**. They evoke a compass-rose tick or a survey marker — quiet, technical, recurring. On the guideline sheet, every section has one.

**Spec:**
- Two strokes forming a right angle pointing southwest: a 12px horizontal line and a 12px vertical line, meeting at the corner, both 1.5px stroke, no fill.
- Color: `#cfcfcf` (Mist) on dark surfaces, `#262626` (Deep Ink) on light surfaces.
- Always placed at the **top-right** of the section heading row, vertically centered against the heading.
- Always 1:1 ratio with the heading's cap height (roughly 12–16px tall).

```html
<div class="section-header">
  <h3 class="label-gold">LOGO USAGE</h3>
  <svg class="corner-arrow" width="16" height="16" viewBox="0 0 16 16" aria-hidden="true">
    <path d="M14 2 H4 V14 M14 2 L4 14" stroke="currentColor" stroke-width="1.5" fill="none" />
  </svg>
</div>
```

```css
.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.corner-arrow {
  color: var(--text-on-dark);
  flex-shrink: 0;
}
```

**Do not** invent new decorative shapes (triangles, dots, ornaments, dividers, brackets in other orientations). The corner arrow is the one motif. Two arrows are not more brand than one.

### 3. The gold rules (top and bottom of page)

Two non-negotiable structural elements on every full-page surface (marketing pages, deck slides, PDF covers):

- **Top:** a 1px gold hairline running the full width directly beneath the primary nav (or beneath the wordmark on a deck slide / PDF cover).
- **Bottom:** a 12px solid gold bar running the full width of the page, flush with the bottom edge.

These two rules frame every JetHQ surface like the top and bottom margins of a vintage navigation chart. They are the brand's chrome.

```css
.page-frame::before {
  content: "";
  position: absolute;
  top: var(--nav-height); /* directly beneath nav */
  left: 0; right: 0;
  height: 1px;
  background: var(--brand-gold);
}
.page-frame::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0; right: 0;
  height: 12px;
  background: var(--brand-gold);
}
```

---

## Layout

### Grid

12-column grid, 24px gutter at desktop, 16px at tablet, 8px at mobile. Container max-widths:

- Editorial marketing: 1240px outer, 720px text measure for long-form prose.
- App: 1440px outer, full-bleed tables and sheets inside.
- PDF / deck slide: 1140px (matches a standard 16:9 deck export at 1920×1080 with margins).

### Page shell

Every full-page surface follows the same shell:

```
┌──────────────────────────────────────────────────────────┐
│  [JETHQ wordmark]              Logo  Font  Color  Visual │  ← nav, 64px tall
├──────────────────────────────────────────────────────────┤  ← 1px gold hairline
│                                                          │
│                      [page content]                      │
│                                                          │
├──────────────────────────────────────────────────────────┤  ← 12px gold bar
└──────────────────────────────────────────────────────────┘
```

The nav, the gold hairline, and the gold bottom bar are present on **every** marketing surface and PDF cover. Internal app pages may drop the bottom bar in favor of a denser footer, but never drop the hairline.

### Spacing

Base unit: **8px**. Spacing tokens: 4, 8, 12, 16, 24, 32, 48, 64, 96, 128. Marketing layouts bias toward 48–128. App layouts use 8–24 most often.

### Border-radius

Disciplined small set: `0` (table cells, hairline dividers), `4px` (cards, inputs, buttons), `8px` (modals, large panels), `9999px` (status pills, avatars only — never primary buttons).

### Elevation

Almost flat. Default surfaces use a 1px border, no shadow. Cards on dark surfaces are darker, not lighter. Modals and dropdowns get a single soft elevation:

```css
box-shadow: 0 12px 32px -8px rgba(0, 0, 0, 0.6);
```

Never use heavy drop shadows — they read as dated and salesy.

### Motion

Fast 150ms, base 250ms, slow 400ms; ease-out for fades, ease-in-out for transforms. No bounce, no spring, no parallax, no decorative motion. Honor `prefers-reduced-motion: reduce` with a zero-duration variant.

---

## Imagery

The biggest mistake brokerages in this category make is generic aviation stock — sunset tail shots, tarmac handshakes, leather-cabin close-ups with a champagne flute. JetHQ does not use them. Imagery is either:

1. **Topographic and cartographic abstractions** — contour-line patterns, vintage navigation charts, isobar wind maps, sectional VFR chart fragments, route lines on a globe. The signature visual language.
2. **Commissioned, restrained photography** — real aircraft, real crews, real airports, shot with available light, never the cinematic-sunset cliché. Aerial shots show terrain and route, not the airplane as hero. If a cabin appears, it is empty and editorial, not "lifestyle."
3. **Document specimens** — a redacted excerpt of a quote pack, a stylized fragment of a sourcing report, a flight log entry. JetHQ's own artifacts, treated as portraits.

**The test:** could a competitor lift this image onto their own brokerage site? If yes, it is working against you. Replace it.

Stock aviation imagery is forbidden. If a photograph is required and no commissioned shot exists, default to a topographic accent block instead.

---

## Voice and page patterns

Marketing surfaces sell calm competence, not "luxury experiences." Concretely:

- **Hero copy must speak like an operator, not a marketer.** "We arrange the trip" lands harder than "Experience aviation reimagined." Speak to the specific situation — a charter to a strip without scheduled service, a multi-leg international itinerary, a recurring route with a fleet preference, an aircraft acquisition. The visitor knows what a private jet is; what they want to know is whether you are competent and discreet.
- **Proof goes high on the page.** Named brokers with real faces and tenure, years in operation, fleet scope, regulatory affiliations (ARGUS, Wyvern, IS-BAO) shown as a quiet trust bar — never as logos-soup.
- **One low-pressure call to action per page.** "Request a quote" or "Speak with a broker." Framed as a conversation, not a transaction. A single field — name, route, date, or a short message. Never a ten-field RFQ form on the marketing site, never urgency banners, never countdown timers, never chatbots.
- **No marketing motion.** No autoplay aerial b-roll. No animated counters ("$1.2B in flights brokered"). No carousels. No exit-intent overlays. Each reads as salesy and erodes the brokerage posture.
- **Body voice — direct, declarative, owner/date/next-step framed.** No em dashes. No hedging. Short sentences sit comfortably next to long ones. Never "we believe" or "we are passionate about" — show, never claim. Tail numbers and ICAO codes appear in mono and uppercase: `N1234J`, `KTEB → LFPB`.

App surfaces (broker/ops tooling) sell competence and care. Keep the same restraint, but allow density:

- Quote breakdowns, fleet comparison grids, and itineraries are dense by necessity. Respect the density — do not pad data screens with marketing whitespace, and do not import editorial display type into app chrome.
- Surface only one primary action per screen. Secondary actions ghost. Destructive actions (cancel a quote, release a hold) require a typed confirmation, never just a "Cancel" button at hover-distance.
- Audit trail and provenance are part of the brand. Show "quoted by [broker] on [date]" on every quote artifact. This is how the product earns trust the way the firm does.

---

## Trust bar

JetHQ marketing surfaces should carry a **quiet trust bar** near the hero — a single line of subdued credentials, never logos-soup. Suggested pattern:

```
Founded 2009   ·   ARGUS Platinum / Wyvern Wingman   ·   12,000+ trips arranged   ·   Operations in 6 regions
```

- Render in 12–13px sans Medium, `hsl(0 0% 65%)` on dark surfaces / `hsl(204 5% 38%)` on light.
- Dot separators with a full em of space either side.
- Never use partner / operator logos as a trust bar. JetHQ's trust is conferred by its own credentials, not by a Gulfstream or NetJets wordmark.

---

## Component patterns — copy-pasteable

### CSS tokens

```css
:root {
  /* fonts */
  --font-display: 'Mrs Eaves OT', 'EB Garamond', Georgia, serif;
  --font-sans:    'Gotham', 'Inter', system-ui, sans-serif;
  --font-mono:    'JetBrains Mono', ui-monospace, monospace;

  /* surfaces */
  --surface-page-dark:   hsl(204 5% 27%);   /* #414649 */
  --surface-card-dark:   hsl(0 0% 15%);     /* #262626 */
  --surface-card-hover:  hsl(0 0% 18%);
  --surface-page-light:  hsl(38 18% 96%);
  --surface-card-light:  hsl(0 0% 100%);

  /* brand */
  --brand-gold:          hsl(34 36% 58%);   /* #b9986d */
  --brand-gold-deep:     hsl(34 36% 50%);
  --brand-gold-tint:     hsl(34 36% 58% / 0.10);
  --signal-teal:         hsl(182 47% 46%);  /* #3dabaf — accent / active state only */

  /* text */
  --text-on-dark:        hsl(0 0% 81%);     /* #cfcfcf */
  --text-on-light:       hsl(0 0% 15%);     /* #262626 */
  --text-muted-dark:     hsl(0 0% 65%);
  --text-muted-light:    hsl(204 5% 38%);
  --text-placeholder:    hsl(0 0% 55%);

  /* borders */
  --border-on-dark:      hsl(0 0% 81% / 0.14);
  --border-on-dark-input: hsl(0 0% 81% / 0.18);
  --border-on-dark-strong: hsl(0 0% 81% / 0.28);
  --border-on-light:     hsl(0 0% 15% / 0.12);

  /* structural rules */
  --rule-hairline:       1px solid var(--brand-gold);
  --rule-bottom-bar:     12px solid var(--brand-gold);
}

body {
  background: var(--surface-page-dark);
  color: var(--text-on-dark);
  font-family: var(--font-sans);
  font-size: 15px;
  font-weight: 300;
  line-height: 1.55;
  margin: 0;
  min-height: 100vh;
}
```

### Nav bar

```jsx
<nav className="flex items-center justify-between px-12 py-6 bg-[hsl(204_5%_27%)] border-b border-[hsl(34_36%_58%)]">
  <a href="/" className="flex items-center gap-3" aria-label="JetHQ home">
    <WingedGlobeMark className="h-7 w-auto" />
    <span className="font-serif text-2xl tracking-wide">
      <span className="text-[hsl(0_0%_81%)]">JET</span>
      <span className="text-[hsl(34_36%_58%)]">HQ</span>
    </span>
  </a>
  <ul className="flex items-center gap-8 text-[13px] font-medium tracking-wide uppercase text-[hsl(0_0%_81%)]">
    <li><a href="/fleet"  className="hover:text-[hsl(34_36%_58%)] transition-colors">Fleet</a></li>
    <li><a href="/routes" className="hover:text-[hsl(34_36%_58%)] transition-colors">Routes</a></li>
    <li><a href="/about"  className="hover:text-[hsl(34_36%_58%)] transition-colors">About</a></li>
    <li><a href="/quote"  className="hover:text-[hsl(34_36%_58%)] transition-colors">Quote</a></li>
  </ul>
</nav>
```

### Primary button (filled gold — rare, hero CTA only)

```jsx
<button className="
  inline-flex items-center justify-center
  px-6 py-3
  bg-[hsl(34_36%_58%)] text-[hsl(0_0%_15%)]
  font-medium text-sm uppercase tracking-wider
  rounded
  transition-colors duration-200
  hover:bg-[hsl(34_36%_50%)]
  focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-[hsl(182_47%_46%)] focus-visible:ring-offset-2 focus-visible:ring-offset-[hsl(204_5%_27%)]
">
  Request a Quote
</button>
```

### Default button (gold outline on dark)

```jsx
<button className="
  inline-flex items-center justify-center
  px-6 py-3
  bg-transparent text-[hsl(34_36%_58%)]
  border border-[hsl(34_36%_58%)]
  font-medium text-sm uppercase tracking-wider
  rounded
  transition-colors duration-200
  hover:bg-[hsl(34_36%_58%/0.10)]
  focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-[hsl(182_47%_46%)] focus-visible:ring-offset-2 focus-visible:ring-offset-[hsl(204_5%_27%)]
">
  Speak with a Broker
</button>
```

### Card on dark

```jsx
<article className="
  bg-[hsl(0_0%_15%)]
  border border-[hsl(0_0%_81%/0.14)]
  rounded
  p-8
  text-[hsl(0_0%_81%)]
">
  <div className="flex items-start justify-between mb-6">
    <h3 className="font-serif text-[13px] font-medium tracking-[0.14em] uppercase text-[hsl(34_36%_58%)]">
      Fleet Class
    </h3>
    <svg width="14" height="14" viewBox="0 0 16 16" aria-hidden="true" className="text-[hsl(0_0%_81%)]">
      <path d="M14 2 H4 V14 M14 2 L4 14" stroke="currentColor" strokeWidth="1.5" fill="none" />
    </svg>
  </div>
  <h2 className="font-serif text-3xl mb-2 text-[hsl(34_36%_58%)] uppercase tracking-wide">Heavy Jet</h2>
  <p className="font-sans text-base text-[hsl(0_0%_81%)] leading-relaxed">
    Transcontinental and transatlantic range, 10–14 passengers, full galley and enclosed lavatory.
  </p>
</article>
```

### Section heading (signature gold/sans pair)

```jsx
<header className="mb-12">
  <div className="flex items-start justify-between mb-8">
    <span className="font-serif text-[13px] font-medium tracking-[0.14em] uppercase text-[hsl(34_36%_58%)]">
      Color Usage
    </span>
    <svg width="16" height="16" viewBox="0 0 16 16" aria-hidden="true" className="text-[hsl(0_0%_81%)]">
      <path d="M14 2 H4 V14 M14 2 L4 14" stroke="currentColor" strokeWidth="1.5" fill="none" />
    </svg>
  </div>
  <h2 className="font-serif text-[32px] uppercase tracking-wide text-[hsl(34_36%_58%)] mb-1">
    Heading
  </h2>
  <p className="font-sans text-[22px] font-medium uppercase tracking-wide text-[hsl(0_0%_81%)]">
    Subheading
  </p>
</header>
```

### Page shell (full marketing surface)

```jsx
<div className="min-h-screen bg-[hsl(204_5%_27%)] text-[hsl(0_0%_81%)] flex flex-col">
  <Nav />
  {/* 1px gold hairline directly beneath nav */}
  <div className="h-px bg-[hsl(34_36%_58%)] w-full" />

  <main className="flex-1 max-w-[1240px] w-full mx-auto px-12 py-24 relative">
    {/* optional low-opacity topographic background */}
    <div className="absolute inset-0 pointer-events-none opacity-[0.18]" aria-hidden="true">
      <TopographicLines />
    </div>
    <div className="relative">
      {/* page content */}
    </div>
  </main>

  {/* 12px solid gold bottom bar */}
  <div className="h-3 bg-[hsl(34_36%_58%)] w-full" />
</div>
```

---

## shadcn/ui integration notes

If the project uses shadcn/ui, override the default theme tokens to map JetHQ's palette. The CSS variables shadcn expects (in HSL component form, space-separated, no `hsl()` wrapper):

```css
:root {
  --background: 204 5% 27%;       /* page = charcoal */
  --foreground: 0 0% 81%;         /* text on dark */

  --card: 0 0% 15%;               /* cards go darker, not lighter */
  --card-foreground: 0 0% 81%;

  --popover: 0 0% 15%;
  --popover-foreground: 0 0% 81%;

  --primary: 34 36% 58%;          /* gold */
  --primary-foreground: 0 0% 15%;

  --secondary: 0 0% 18%;
  --secondary-foreground: 0 0% 81%;

  --muted: 0 0% 18%;
  --muted-foreground: 0 0% 65%;

  --accent: 182 47% 46%;          /* Signal Teal — used by shadcn for hover/active */
  --accent-foreground: 0 0% 96%;

  --destructive: 4 60% 50%;
  --destructive-foreground: 0 0% 96%;

  --border: 0 0% 81% / 0.14;
  --input: 0 0% 81% / 0.18;
  --ring: 182 47% 46%;            /* teal focus ring */

  --radius: 0.25rem;              /* 4px — rectangles, not pills */
}
```

After mapping, override the default Button variants so `variant="default"` is the outline-gold treatment (not filled) and a new `variant="hero"` is the filled-gold CTA. Filled-gold is for one button per page maximum.

---

## Do / Don't

### Do

- **Default to the dark ground.** Charcoal `#414649` is the page. The brand was designed for it.
- **Use exactly two fonts** — display serif and sans. Per the guideline: *Avoid using more than two fonts per design.*
- **Keep the gold rule on top and the gold bar on the bottom.** They frame the page like the margins of a navigation chart.
- **Pair every section heading with a corner-arrow marker.** It is the JetHQ tick.
- **Reserve Signal Teal for state.** Active, selected, focus, informational. Nothing else.
- **Use tabular figures in any dense data.** Quote breakdowns, fleet tables, itineraries.
- **Show the broker.** Named, with credentials. Real face, available light.
- **Treat the topographic motif as ornament with restraint** — once or twice per viewport, never three places at once.

### Don't

- **Don't stretch, rotate, recolor, or alter the logo.** Two-color treatment only. Never paint the lockup entirely gold or entirely white.
- **Don't use more than two fonts.** Three is a redesign, not a JetHQ surface.
- **Don't paint a button gold by default** — gold is identity. The filled-gold button is reserved for one hero CTA per page.
- **Don't use teal as a decorative accent.** The moment teal becomes ornament, its state meaning is broken.
- **Don't make cards lighter than the page.** On dark, cards go darker — that is the JetHQ way.
- **Don't use pure white anywhere except inside the lockup containment box.** Off-white ivory (`hsl(38 18% 96%)`) is the light surface.
- **Don't use stock aviation imagery.** Tarmac handshakes, sunset tails, champagne-flute cabins. If no commissioned shot exists, use a topographic block.
- **Don't introduce status colors on marketing surfaces.** Status is for app state.
- **Don't use vendor Tailwind colors** (`bg-amber-50`, `text-emerald-600`). They will not match the calibrated palette and will clash with the charcoal ground.
- **Don't add chrome textures, glassmorphism, animated counters, autoplay video, urgency banners, exit-intent overlays, or chatbots.** Every one reads as salesy.
- **Don't use pills for buttons.** Buttons are 4px-radius rectangles. Pills are reserved for status indicators and avatars.
- **Don't tighten serif tracking.** Mrs Eaves and its fallback want room.
- **Don't break the page frame.** Top gold hairline and bottom gold bar are present on every full-page surface.

---

## Common mistakes to avoid

1. **Painting the wordmark all-gold.** "JET" is light, "HQ" is gold. The two-color contrast is the wordmark. A solid-gold JETHQ reads as a generic luxury brand.
2. **Putting cards on a lighter background than the page.** On dark, cards descend toward black, not ascend toward white. Inverting this kills the editorial-print feel.
3. **Using teal as a brand color.** Teal is state. Painting a hero section teal or using teal as a chart series default breaks the brand's most reserved system color.
4. **Adding a third font.** A "modern" sans for nav and Inter for body is two fonts too many. Display serif + sans, full stop.
5. **Overusing the topographic motif.** A page with background topography, a topographic feature block, and topographic dividers is three places too many. Once or twice, low opacity, then stop.
6. **Forgetting the bottom gold bar.** The 12px gold bar at the bottom of the page is structural, not decorative. It is always present on marketing surfaces and PDF covers.
7. **Using stock aviation imagery.** A sunset-tail hero shot will instantly drag the brand back into the cobalt-and-chrome category it works to escape.
8. **Centering everything.** JetHQ favors asymmetric balance — the guideline page itself is asymmetric. Avoid the centered-stack landing page.
9. **Tightening Mrs Eaves.** It is designed to breathe. Default tracking, never below `-0.005em`.
10. **Treating Gotham Light as too thin to read.** It is the body weight. Pair it with high-contrast color (`#cfcfcf` on `#414649`) and generous line-height (1.55) and it reads as quietly confident — not weak.

---

## Rules summary

- **Apply only what the content needs.** Marketing pages don't need status colors. Static documents don't need form chrome. Pull only the sections this output requires.
- **Two-color logo, always.** Ivory + gold on dark, charcoal + gold on light. Never stretched, rotated, recolored, or boxed.
- **Two fonts, always.** Display serif + sans. No exceptions.
- **Gold is identity, not interaction.** Use for wordmark, headings, rules, and the bottom bar. Buttons are gold-outline by default; filled-gold is reserved for one hero CTA per page.
- **Teal is state, not decoration.** Active, selected, focus, info. Nothing else.
- **Dark ground is the default.** Charcoal `#414649` is the page; cards go darker, not lighter.
- **Topographic motif, sparingly.** Once or twice per viewport, low opacity, gold lines on dark.
- **Corner-arrow marker on every section heading.** It is the JetHQ tick.
- **Top gold hairline + bottom gold bar.** Structural frame on every full-page surface.
- **Tabular figures in any dense data.** Quotes, fleet, schedules, itineraries.
- **No vendor Tailwind colors.** Use the calibrated values from this brief.
- **Buttons are rectangles, 4px radius.** Pills are for status and avatars.
- **No salesy chrome.** No urgency banners, autoplay video, glassmorphism, animated counters, chatbots, pop-ups.
- **WCAG AA on all body text.** Verify per-color, especially `#cfcfcf` mist on the `#414649` ground.

---

## Worked example — JetHQ hero section (full-bleed dark)

```html
<div class="page-shell">
  <nav class="nav">
    <a href="/" class="lockup" aria-label="JetHQ home">
      <svg class="winged-globe" width="32" height="20" aria-hidden="true">…</svg>
      <span class="wordmark">
        <span class="jet">JET</span><span class="hq">HQ</span>
      </span>
    </a>
    <ul class="nav-links">
      <li><a href="/fleet">Fleet</a></li>
      <li><a href="/routes">Routes</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="/quote">Quote</a></li>
    </ul>
  </nav>
  <div class="hairline"></div>

  <main class="hero">
    <div class="topo-bg" aria-hidden="true"></div>

    <header class="section-label">
      <span class="label-gold">Private Aviation, Brokered</span>
      <svg class="corner-arrow" width="14" height="14" viewBox="0 0 16 16" aria-hidden="true">
        <path d="M14 2 H4 V14 M14 2 L4 14" stroke="currentColor" stroke-width="1.5" fill="none"/>
      </svg>
    </header>

    <h1 class="hero-title">
      <span class="serif">Trips arranged.</span><br/>
      <span class="serif italic">Not sold.</span>
    </h1>

    <p class="hero-body">
      JetHQ sources, quotes, and oversees private charters across six regions.
      A single broker handles the trip from request to wheels-up.
    </p>

    <div class="hero-actions">
      <a class="button-hero" href="/quote">Request a Quote</a>
      <a class="button-outline" href="/about">Speak with a Broker</a>
    </div>

    <p class="trust-bar">
      <span>Founded 2009</span><span>ARGUS Platinum / Wyvern Wingman</span><span>12,000+ trips arranged</span>
    </p>
  </main>

  <div class="bottom-bar"></div>
</div>
```

```css
.page-shell {
  background: hsl(204 5% 27%);
  color: hsl(0 0% 81%);
  font-family: 'Gotham', 'Inter', sans-serif;
  font-weight: 300;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.nav {
  display: flex; align-items: center; justify-content: space-between;
  padding: 1.5rem 3rem;
}
.lockup { display: flex; align-items: center; gap: 0.75rem; text-decoration: none; }
.wordmark { font-family: 'EB Garamond', 'Mrs Eaves OT', serif; font-size: 1.75rem; letter-spacing: 0.04em; }
.jet { color: hsl(0 0% 81%); }
.hq  { color: hsl(34 36% 58%); }

.nav-links { display: flex; gap: 2rem; list-style: none; margin: 0; padding: 0; }
.nav-links a {
  font-size: 13px; font-weight: 500; letter-spacing: 0.08em; text-transform: uppercase;
  color: hsl(0 0% 81%); text-decoration: none; transition: color 200ms ease-out;
}
.nav-links a:hover { color: hsl(34 36% 58%); }

.hairline { height: 1px; background: hsl(34 36% 58%); }

.hero {
  position: relative;
  flex: 1;
  max-width: 1240px;
  width: 100%;
  margin: 0 auto;
  padding: 6rem 3rem;
}
.topo-bg {
  position: absolute; inset: 0;
  background-image: url('/topographic-lines.svg');
  background-size: cover; background-position: center;
  opacity: 0.18; pointer-events: none;
}

.section-label {
  position: relative;
  display: flex; align-items: center; justify-content: space-between;
  max-width: 720px;
  margin-bottom: 3rem;
}
.label-gold {
  font-family: 'EB Garamond', serif;
  font-size: 13px; font-weight: 500; letter-spacing: 0.14em; text-transform: uppercase;
  color: hsl(34 36% 58%);
}

.hero-title {
  position: relative;
  font-family: 'EB Garamond', 'Mrs Eaves OT', serif;
  font-size: clamp(48px, 6vw, 72px);
  font-weight: 400;
  line-height: 1.05;
  letter-spacing: -0.005em;
  color: hsl(0 0% 96%);
  max-width: 720px;
  margin: 0 0 1.5rem 0;
}
.hero-title .italic { font-style: italic; color: hsl(34 36% 58%); }

.hero-body {
  position: relative;
  max-width: 560px;
  font-size: 17px; line-height: 1.55; font-weight: 300;
  color: hsl(0 0% 81%);
  margin: 0 0 2.5rem 0;
}

.hero-actions { position: relative; display: flex; gap: 1rem; margin-bottom: 4rem; }

.button-hero {
  display: inline-flex; align-items: center; justify-content: center;
  background: hsl(34 36% 58%); color: hsl(0 0% 15%);
  border: none; border-radius: 4px;
  padding: 0.875rem 1.5rem;
  font-family: 'Gotham', 'Inter', sans-serif;
  font-weight: 500; font-size: 13px; letter-spacing: 0.08em; text-transform: uppercase;
  text-decoration: none;
  transition: background 200ms ease-out;
}
.button-hero:hover { background: hsl(34 36% 50%); }

.button-outline {
  display: inline-flex; align-items: center; justify-content: center;
  background: transparent; color: hsl(34 36% 58%);
  border: 1px solid hsl(34 36% 58%); border-radius: 4px;
  padding: 0.875rem 1.5rem;
  font-family: 'Gotham', 'Inter', sans-serif;
  font-weight: 500; font-size: 13px; letter-spacing: 0.08em; text-transform: uppercase;
  text-decoration: none;
  transition: background 200ms ease-out;
}
.button-outline:hover { background: hsl(34 36% 58% / 0.10); }

.trust-bar {
  position: relative;
  font-size: 12px; font-weight: 500; letter-spacing: 0.06em;
  color: hsl(0 0% 65%);
  margin: 0;
}
.trust-bar span + span::before {
  content: "·"; margin: 0 0.75em; color: hsl(0 0% 65%);
}

.bottom-bar { height: 12px; background: hsl(34 36% 58%); }

*:focus-visible {
  outline: 2px solid hsl(182 47% 46%);
  outline-offset: 2px;
}
```

---

## One-line summary

JetHQ is **charcoal ground + warm gold identity + Mrs Eaves serif + Gotham sans + a single topographic motif + a teal accent reserved for state**. Restraint over volume. The brand is the HQ, not the jet.
