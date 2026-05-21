---
name: Restore Hyper Wellness Design System
version: "1.0"
brand: Restore Hyper Wellness
generated: 2026-05-20
lean: intent
sources:
  - { type: pdf, lane: intent, ref: "Restore Brand Guidelines (97-slide deck, owned by kristamaloney@restore.com)" }
  - { type: web, lane: reality, ref: "https://www.restore.com/" }
colors:
  primary: "#055577"          # Restore Blue — the signature anchor
  secondary: "#042E43"         # Quiet Blue — depth, gravitas
  accent: "#308CBF"            # Sky — live-site primary, energetic counterweight
  surface: "#FFFFFF"
  surface_variant: "#FFFDF8"   # Cream — new addition per latest brand book
  text: "#042E43"              # Quiet Blue reads as body text on white at full saturation
  on_surface_variant: "#055577"
typography:
  display: "Poppins"           # SemiBold preferred; Bold/ExtraBold/Black sparingly
  body: "Open Sans"
  mono: "JetBrains Mono"
spacing:
  base_unit: 4                 # 4px scale from web reality
  border_radius: "20px"        # Pills 30px (buttons), tiles 20px
components:
  button_primary:
    background: "#055577"
    text: "#FFFFFF"
    border_radius: "30px"
    shadow: "none"
  button_secondary:
    background: "#308CBF"
    text: "#FFFFFF"
    border_radius: "30px"
    shadow: "none"
---

# Restore Hyper Wellness — Design System

The single source of visual truth for every downstream coding agent in the Restore stack. Read this file, treat the tokens as authoritative.

## The look in one sentence

Restore's visual identity is **clinical-modern wellness**: a deep, considered blue palette anchors science-backed credibility while Poppins headlines bring approachable warmth. White space is structural — the brand breathes, never crowds.

## Colors

### Primary palette — Restore Blue (the signature)

- **Restore Blue** `#055577` — *The signature.* Use for headlines on white, primary CTAs, header backgrounds in long-form materials. Conveys the brand's clinical depth and trust.
- **Quiet Blue** `#042E43` — *Deeper, more grounded.* Use for body text on white (preferred over pure black), dark surface backgrounds, and as the darker stop on gradients.
- **Sky** `#308CBF` — *The energy counterweight.* Use for secondary CTAs, hover states, and lighter-mood treatments. The live website leans on this as its primary brand color; brand book treats it as a brighter accent.

### Surface

- **White** `#FFFFFF` — Default page background. Most marketing surfaces are white.
- **Cream** `#FFFDF8` — *New, 2026.* Use for warmer secondary surfaces, callouts, and email backgrounds where pure white feels too clinical.

### Energy colors

Each Restore Hyper Wellness element (Cryotherapy, Red Light, Infrared, Compression, IV Drip, Skin Health) carries its own energy color per the brand book. The full Energy palette lives in slide 14 of the source brand book and should be loaded from there when designing therapy-specific creative. Default to Restore Blue for cross-therapy materials.

## Typography

### Three-family system

| Role | Family | Weight | Spec |
|---|---|---|---|
| Headline (display) | Poppins | SemiBold (600) — preferred; Bold/ExtraBold/Black sparingly | Used for hero headlines, section titles, ad copy. |
| Body | Open Sans | Regular (400) / SemiBold (600) | Body copy, paragraph text, supporting copy. |
| Mono / code | JetBrains Mono | Regular | Inline code and hex values. |

### Scale (from live website)

- `h1` — 56px / Poppins SemiBold / -0.01em
- `h2` — 36px / Poppins SemiBold
- `h3` — 24px / Poppins SemiBold
- `body` — 16px / Open Sans 400 / 1.6 line-height
- `small` — 14px / Open Sans 400

### Rationale

Poppins SemiBold is "bold enough to feel impactful, restrained enough to stay human-approachable." Open Sans gives the science-backed body content room to breathe — never competes with the headline. The brand book is explicit: Bold/ExtraBold/Black weights "should be used sparingly for dramatic emphasis or hierarchy."

## Spacing

- **Base unit:** 4px (scale: 4, 8, 12, 16, 24, 32, 48, 64)
- **Border radius:**
  - Tiles / cards: 20px
  - Buttons: 30px (full pill shape from live site)
  - Inputs: 8px
- **Section padding:** 64–96px vertical on desktop; 32–48px on mobile

## Components

### Buttons

**Primary**
- Background: `#055577` (Restore Blue)
- Text: `#FFFFFF`
- Padding: 14px 32px
- Border radius: 30px
- Font: Poppins SemiBold, 16px
- No shadow. The brand earns depth from saturated color, not elevation.

**Secondary**
- Background: `#308CBF` (Sky)
- Text: `#FFFFFF`
- Same proportions as primary.

**Tertiary / on-dark**
- Background: `#FFFFFF`
- Text: `#055577`
- Border: 2px solid `#055577` (optional)

### Cards / tiles

- Background: `#FFFFFF` or `#FFFDF8` (Cream for warmer contexts)
- Border radius: 20px
- Optional 1px border: `rgba(5, 85, 119, 0.10)` (Restore Blue at 10% opacity)
- Padding: 24–32px
- Heading: Poppins SemiBold 20–24px
- Body: Open Sans 16px

### Callouts / proof-point boxes

- Background: `#FFFDF8` (Cream)
- Left border: 4px solid `#055577` (Restore Blue)
- Padding: 20px 24px
- Inside: lead with **bold Poppins** label, body in Open Sans

## Do's and Don'ts

✅ **Do:**
- Lead headlines with a benefit, not the brand name
- Use Restore Blue for primary action and trust signals
- Pair Cream surfaces with Restore Blue text for warmth without losing brand recognition
- Reserve ExtraBold/Black Poppins weights for dramatic emphasis only

❌ **Don't:**
- Use Sky `#308CBF` as the primary anchor in print or formal materials — that's the brand book's intent (web reality differs)
- Mix more than two type weights in a single composition
- Add box-shadow to buttons — depth comes from color saturation
- Use Oxford commas anywhere (AP Style)

## Deviations

The live website (https://www.restore.com/) currently uses `#308CBF` (Sky) as the dominant button color and `#055577` (Restore Blue) as accent/text. The 2026 brand book reverses this — Restore Blue is the primary signature. We've kept the brand book intent here (`lean: intent`). For any web work that needs to ship alongside existing pages, swap the primary/secondary roles to match production.

The brand book also introduces Cream `#FFFDF8` as a new 2026 surface color. The current production site does not yet use it.

## Accessibility

- Restore Blue `#055577` on White: 7.84:1 contrast ratio — passes WCAG AAA
- Sky `#308CBF` on White: 3.12:1 — **fails AAA for body text**; OK for large text or non-essential UI only
- Quiet Blue `#042E43` on White: 12.93:1 — passes AAA comfortably
- White on Restore Blue: 7.84:1 — passes AAA

## Sub-brand palettes

Restore is planning a brand transition for August/September 2026. The current brand book is stable through mid-2026. Sub-brand palettes (if any emerge from the rebrand) should be added here under `colors.subbrands` in frontmatter with a row in the brand_showcase HTML.

## Notes for downstream agents

When asked to build any UI for Restore:
1. Read this file (`@design.md` in Claude Code, drag-and-drop in Cursor, paste as context elsewhere)
2. Use the hex values exactly — no "close enough" blues
3. Default to Restore Blue primary unless the spec explicitly calls for live-site parity
4. Lead headlines with Poppins SemiBold at the largest scale
5. Body must be Open Sans, never serif, never display-weight

For voice/copy, pair this with the `restore-hyper-wellness-voice` Claude skill in `../01_Brand_Voice/restore-hyper-wellness-voice/`.
