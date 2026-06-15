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
  primary: "#055577"           # Restore Blue — the signature anchor
  secondary: "#042E43"         # Quiet — depth, gravitas
  accent: "#308CBF"            # Do More — energetic counterweight
  summit: "#EEF6FA"            # Summit — lightest blue, airy surfaces
  cream: "#FFF9F2"             # Cream — warm secondary surface
  text: "#042E43"              # Quiet reads as body text on white at full saturation
  on_surface_variant: "#055577"
  energy:
    cold: "#0081A1"
    hydration: "#53BDD8"
    oxygen: "#B7EBF9"
    nourishment: "#2C8F82"
    rest: "#C2EED8"
    light: "#FF6056"
    heat: "#FF8C60"
    movement: "#FFB0B0"
    connection: "#D880D8"
  tertiary:
    energy:       { primary: "#BB2EBA", mid: "#FFB3D8", light: "#FFEDF1" }
    immunity:     { primary: "#1C7468", mid: "#82D1BF", light: "#E9F5F3" }
    recovery:     { primary: "#4488C4", mid: "#6EB5DD", light: "#F0FAFF" }
    skin_health:  { primary: "#F18A7D", mid: "#FFD7C4", light: "#FFFBF4" }
    brain_health: { primary: "#A061BA", mid: "#B586C9", light: "#FBF1FF" }
    athletic_performance: { primary: "#E93C3D", mid: "#FB7575", light: "#FEF2EE" }
    weight_management:    { primary: "#4EC3C6", mid: "#77D8DA", light: "#E8FFFD" }
typography:
  display: "Poppins"           # SemiBold preferred; Bold/ExtraBold/Black sparingly
  body: "Open Sans"
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

> ⚠️ *This description is in flux. The visual direction is evolving toward something less clinical and more modern and emotion-driven. Update this section once the new direction is defined.*

## Colors

### Primary Palette

- **Restore Blue** `#055577` — *The signature.* Use for headlines on white, primary CTAs, header backgrounds in long-form materials. Conveys clinical depth and trust.
- **Quiet** `#042E43` — *Deeper, more grounded.* Use for body text on white (preferred over pure black), dark surface backgrounds, and as the darker stop on gradients.
- **Do More** `#308CBF` — *The energy counterweight.* Use for secondary CTAs, hover states, and lighter-mood treatments. The live website uses this as its primary brand color; brand book treats it as a brighter accent.
- **Summit** `#EEF6FA` — *Airy and light.* Use for backgrounds, section washes, and anywhere the palette needs to breathe without going to pure white.
- **Cream** `#FFF9F2` — *Warm and approachable.* Use for secondary surfaces, callouts, and email backgrounds where pure white feels too clinical. White (`#FFFFFF`) remains the default page background.

### 9 Elements Palette

Each element carries its own energy color for therapy-specific creative. Default to Restore Blue for cross-therapy materials.

| Element | Hex |
|---|---|
| **Cold** | `#0081A1` |
| **Hydration** | `#53BDD8` |
| **Oxygen** | `#B7EBF9` |
| **Nourishment** | `#2C8F82` |
| **Rest** | `#C2EED8` |
| **Light** | `#FF6056` |
| **Heat** | `#FF8C60` |
| **Movement** | `#FFB0B0` |
| **Connection** | `#D880D8` |

### IV Colors — Benefit Categories

*Introduced for the IV launch. Each category has three tiers: primary (bold), mid (approachable), and light (background/tint). These extend the primary palette and may be used beyond IV creative as needed.*

| Category | Primary | Mid | Light |
|---|---|---|---|
| **Energy** | `#BB2EBA` | `#FFB3D8` | `#FFEDF1` |
| **Immunity** | `#1C7468` | `#82D1BF` | `#E9F5F3` |
| **Recovery** | `#4488C4` | `#6EB5DD` | `#F0FAFF` |
| **Skin Health** | `#F18A7D` | `#FFD7C4` | `#FFFBF4` |
| **Brain Health** | `#A061BA` | `#B586C9` | `#FBF1FF` |
| **Athletic Performance** | `#E93C3D` | `#FB7575` | `#FEF2EE` |
| **Weight Management** | `#4EC3C6` | `#77D8DA` | `#E8FFFD` |

> Use the light tier for section backgrounds and cards. Use the primary tier for headlines, icons, and CTAs within that benefit context. Mid tier for supporting UI elements and hover states.

### Skin Health Menu Colors

*Palette specific to the Skin Health menu and related creative. Official names for Blush and Mocha TBD — update when confirmed.*

| Name | Hex | Usage |
|---|---|---|
| **Restore Blue** | `#055577` | Primary anchor, headlines, CTAs |
| **Cream** | `#FFF9F2` | Warm background surface |
| **Blush** | `#EFDEDB` | Soft secondary surface, cards, section washes |
| **Mocha** | `#9C766F` | Warm accent, text treatments, earthy depth |

### Gradients

| Name | Type | Direction | Stops |
|---|---|---|---|
| **General Restore Gradient 1** | Linear | Top-left → bottom-right (~135°) | `#042E43` 0% → `#1182B5` 99% |
| **General Restore Gradient 2** | Linear | Top-left → bottom-right (~135°) | `#008578` 0% → `#0B5676` 99% |
| **General Restore Gradient 3** | Linear | Top-left → bottom-right (~135°) | `#1182B5` 0% → `#33B2CD` 100% |
| **General Restore Gradient 4** | Linear | Top-left → bottom-right (~135°) | `#055577` 0% → `#042E43` 99% |
| **General Restore Gradient 5** | Linear | Top-left → bottom-right (~135°) | `#E7F9FF` 0% → `#33B2CD` 100% |

| **Campaign Gradient 1** | Linear | Top-left → bottom-right (~135°) | `#00C1DD` 0% → `#008EC7` 37% → `#2FBADD` 72% → `#008EC7` 100% |
| **Campaign Gradient 2** | Radial | Center outward | Light blue-green center → teal/sage edges. *Hex TBD — see Restore Colors Figma.* |

> CSS:
> - Gradient 1: `background: linear-gradient(135deg, #042E43 0%, #1182B5 99%);`
> - Gradient 2: `background: linear-gradient(135deg, #008578 0%, #0B5676 99%);`
> - Gradient 3: `background: linear-gradient(135deg, #1182B5 0%, #33B2CD 100%);`
> - Gradient 4: `background: linear-gradient(135deg, #055577 0%, #042E43 99%);`
> - Gradient 5: `background: linear-gradient(135deg, #E7F9FF 0%, #33B2CD 100%);`
> - Campaign Gradient 1: `background: linear-gradient(135deg, #00C1DD 0%, #008EC7 37%, #2FBADD 72%, #008EC7 100%);`

## Typography

### Three-family system

| Role | Family | Weight | Spec |
|---|---|---|---|
| Headline (display) | Poppins | SemiBold (600) — preferred; Bold/ExtraBold/Black sparingly | Used for hero headlines, section titles, ad copy. |
| Body | Open Sans | Regular (400) / SemiBold (600) | Body copy, paragraph text, supporting copy. |

### Scale (from live website)

- `h1` — 56px / Poppins SemiBold / -0.01em
- `h2` — 36px / Poppins SemiBold
- `h3` — 24px / Poppins SemiBold
- `body` — 16px / Open Sans 400 / 1.6 line-height
- `small` — 14px / Open Sans 400

## Spacing

> ⚠️ *Pending review with Logan — values below are working defaults and may need updating.*

- **Base unit:** 4px (scale: 4, 8, 12, 16, 24, 32, 48, 64)
- **Border radius:**
  - Tiles / cards: 20px
  - Buttons: 30px (full pill shape from live site)
  - Inputs: 8px
- **Section padding:** 64–96px vertical on desktop; 32–48px on mobile

## Components

> ⚠️ *Pending review with Logan — button styles, cards, and callouts below are working defaults and may need updating.*

### Buttons

**Primary**
- Background: `#055577` (Restore Blue)
- Text: `#FFFFFF`
- Padding: 14px 32px
- Border radius: 30px
- Font: Poppins SemiBold, 16px
- No shadow. The brand earns depth from saturated color, not elevation.

**Secondary**
- Background: `#308CBF` (Do More)
- Text: `#FFFFFF`
- Same proportions as primary.

**Tertiary / on-dark**
- Background: `#FFFFFF`
- Text: `#055577`
- Border: 2px solid `#055577` (optional)

**Gradient buttons**
- Used on select pages (e.g. service pages). Exact usage rules and gradient assignments TBD — see live site for reference.
- *Pill shape (30px border-radius) is the standard CTA shape; variations exist by page and context.*

### Cards / tiles

- Background: `#FFFFFF` or `#FFF9F2` (Cream for warmer contexts)
- Border radius: 20px
- Optional 1px border: `rgba(5, 85, 119, 0.10)` (Restore Blue at 10% opacity)
- Padding: 24–32px
- Heading: Poppins SemiBold 20–24px
- Body: Open Sans 16px

### Callouts / proof-point boxes

- Background: `#FFF9F2` (Cream)
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
- Use Do More `#308CBF` as the primary anchor in print or formal materials — that's the brand book's intent (web reality differs)
- Mix more than two type weights in a single composition
- Add box-shadow to buttons — depth comes from color saturation
- Use Oxford commas anywhere (AP Style)

## Deviations

The live website (https://www.restore.com/) currently uses `#308CBF` (Do More) as the dominant button color and `#055577` (Restore Blue) as accent/text. The 2026 brand book reverses this — Restore Blue is the primary signature. We've kept the brand book intent here (`lean: intent`). For any web work that needs to ship alongside existing pages, swap the primary/secondary roles to match production.

The brand book also introduces Cream `#FFF9F2` as a new 2026 surface color. The current production site does not yet use it.

## Accessibility

- Restore Blue `#055577` on White: 7.84:1 contrast ratio — passes WCAG AAA
- Do More `#308CBF` on White: 3.12:1 — **fails AAA for body text**; OK for large text or non-essential UI only
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
