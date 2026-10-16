---
version: 1
name: Mint Dental Clinic — Dental Hygiene London
description: A calm, modern clinical system. Warm-paper canvas, slate ink, one decisive mint-green action colour, a soft editorial serif for statements and a friendly sans for reading. Structure borrowed from the Oura DESIGN.md (awesome-design-md), recoloured to Mint's own brand.

colors:
  primary: "#4D834E"        # the ONLY button/CTA colour
  primary-hover: "#3F6E40"
  on-primary: "#FFFFFF"
  accent: "#437547"         # eyebrows, links, ticks
  mint-glow: "#8FD9C2"      # highlights on dark surfaces only
  ink: "#2F363C"            # headings
  slate: "#4B535B"          # body text, outlines, dark bands
  muted: "#6B747C"
  canvas: "#F7F5EF"         # warm paper — default background
  surface: "#FFFFFF"        # cards, nav pill, inputs
  mint-wash: "#E4F1EA"      # soft green panels
  cool-wash: "#EFF2F5"      # neutral panels
  hairline: "#E3E6E0"
  ink-band: "#262C31"       # footer / featured price card

typography:
  display:  { fontFamily: Lora, fontSize: "clamp(40px, 6vw, 72px)", fontWeight: 400, lineHeight: 1.04, letterSpacing: "-0.02em" }
  heading-2:{ fontFamily: Lora, fontSize: "clamp(32px, 4vw, 48px)", fontWeight: 400, lineHeight: 1.1, letterSpacing: "-0.015em" }
  heading-3:{ fontFamily: Figtree,  fontSize: 22px, fontWeight: 600, lineHeight: 1.3 }
  body:     { fontFamily: Figtree,  fontSize: 18px, fontWeight: 400, lineHeight: 1.6 }
  body-sm:  { fontFamily: Figtree,  fontSize: 16px, fontWeight: 400, lineHeight: 1.55 }
  eyebrow:  { fontFamily: Figtree,  fontSize: 13px, fontWeight: 700, letterSpacing: "0.14em", textTransform: uppercase }
  button:   { fontFamily: Figtree,  fontSize: 17px, fontWeight: 600 }
  price:    { fontFamily: Lora, fontWeight: 400, letterSpacing: "-0.02em" }

rounded: { sm: 10px, md: 16px, lg: 24px, xl: 32px, full: 9999px }
spacing: { base: 8px, section: "clamp(72px, 10vw, 128px)", gutter: "clamp(16px, 4vw, 40px)" }
---

## Overview
Reads like a calm, well-lit clinic: warm paper (`canvas`) instead of white, generous air between sections, and one green button doing all the selling. Serif (Lora, light weight, tight tracking) for big statements; Figtree for everything people actually read. No stock smiles: real photography only.

## Colors
- `primary` green is reserved for **conversion actions only** (Book online, Book a clean). One green moment per view where possible.
- `slate` does the quiet work: outline buttons, text, the dark featured price card, footer.
- `mint-wash` and `cool-wash` are panel colours, never buttons.
- `mint-glow` only appears on dark surfaces (eyebrows on the price card / footer).

## Typography
- Display and section headings: Lora 500, slight negative tracking, `ink`.
- Eyebrows: small uppercase Figtree with wide tracking, in `accent`, preceded by a short green rule.
- Never set body text in Lora.

## Layout
- 8px base unit. Max content width 1200px (FAQs 860px). Section padding = `spacing.section`.
- Rhythm alternates canvas → white → canvas so sections separate by colour, not borders.
- Grids: steps 5-up → 2-up → 1-up; prices 1 featured + 2; reviews 3-up → 1-up.

## Elevation
| Level | Use | Treatment |
|---|---|---|
| 0 | Most sections | flat, colour shift only |
| 1 | Cards | 1px `hairline` border, no shadow |
| 2 | Floating nav, hover cards | `0 10px 30px -12px rgba(38,44,49,.18)` |

## Shapes
- Buttons, chips, the nav: `rounded.full` (pills).
- Cards `rounded.lg`; photos and big panels `rounded.xl`.

## Components
- **floating-nav** — a white pill (`surface` at 85% + backdrop blur) detached from the page edge: sticky, 14px from the top, narrow (max 880px, shrinks to 820px once scrolled), `rounded.full`, deeper shadow once scrolled. Holds a large logo (54px tall, whitespace trimmed), section links (current section highlighted), and the green "Book a clean" pill.
- **proof-strip** — dark `ink-band` band under the hero with a slow scrolling row of trust points (Google rating, GDC, CQC, direct access, fixed price, location). Pauses on hover; only confirmed facts or [placeholders]. On mobile: logo + Call + menu button; links open in a dropdown card under the pill.
- **button-primary** — green pill, white text, 52px tall; hover darkens + lifts 1px.
- **button-outline** — transparent, 1.5px `slate` border, pill.
- **eyebrow** — 24px green rule + uppercase label.
- **step-card** — white card, big serif numeral in `primary`.
- **price-featured** — `ink-band` card, `mint-glow` eyebrow, large serif price.
- **faq** — white rows, hairline borders, rotating "+" icon.

## Do's
- Keep all placeholders ([XX], [Name], review slots) visible until the practice confirms real content — never invent prices, reviews or names.
- Keep the "Not a dental check-up" message close to every booking button.
- Respect `prefers-reduced-motion`.

## Don'ts
- No green on non-action elements bigger than an icon or eyebrow.
- No heavy or hard shadows; no gradients on buttons.
- No stock photography or fake reviews.
