# Design System Inspired by Notion

## 1. Visual Theme & Atmosphere

Notion's website embodies the philosophy of the tool itself: a blank canvas that gets out of your way. The design system is built on warm neutrals rather than cold grays, creating a distinctly approachable minimalism that feels like quality paper rather than sterile glass. The page canvas is pure white (`#ffffff`) but the text isn't pure black — it's a warm near-black (`rgba(0,0,0,0.95)`) that softens the reading experience imperceptibly. The warm gray scale (`#f6f5f4`, `#31302e`, `#615d59`, `#a39e98`) carries subtle yellow-brown undertones, giving the interface a tactile, almost analog warmth.

The custom NotionInter font (a modified Inter) is the backbone of the system. At display sizes (64px), it uses aggressive negative letter-spacing (-2.125px), creating headlines that feel compressed and precise. What makes Notion's visual language distinctive is its border philosophy — ultra-thin `1px solid rgba(0,0,0,0.1)` borders that exist as whispers, barely perceptible division lines that create structure without weight.

**Key Characteristics:**
- NotionInter (modified Inter) with negative letter-spacing at display sizes (-2.125px at 64px)
- Warm neutral palette: grays carry yellow-brown undertones (`#f6f5f4` warm white, `#31302e` warm dark)
- Near-black text via `rgba(0,0,0,0.95)` — not pure black, creating micro-warmth
- Ultra-thin borders: `1px solid rgba(0,0,0,0.1)` — whisper-weight division
- Multi-layer shadow stacks with sub-0.05 opacity for barely-there depth
- Notion Blue (`#0075de`) as the singular accent color for CTAs and interactive elements
- Pill badges (9999px radius) with tinted blue backgrounds for status indicators

## 2. Color Palette & Roles

### Primary
- **Notion Black** (`rgba(0,0,0,0.95)`): Primary text — 95% opacity softens pure black.
- **Pure White** (`#ffffff`): Page background, card surfaces, button text on blue.
- **Notion Blue** (`#0075de`): Primary CTA, link color — the only saturated color in core UI.

### Brand Secondary
- **Deep Navy** (`#213183`): Secondary brand color, used sparingly.
- **Active Blue** (`#005bab`): Button active/pressed state.

### Warm Neutral Scale
- **Warm White** (`#f6f5f4`): Background surface tint, section alternation. Yellow undertone is key.
- **Warm Dark** (`#31302e`): Dark surface background. Warmer than standard grays.
- **Warm Gray 500** (`#615d59`): Secondary text, descriptions, muted labels.
- **Warm Gray 300** (`#a39e98`): Placeholder text, disabled states.

### Interactive
- **Link Blue** (`#0075de`): Primary link color with underline-on-hover.
- **Focus Blue** (`#097fe8`): Focus ring on interactive elements.
- **Badge Blue Bg** (`#f2f9ff`): Pill badge background.
- **Badge Blue Text** (`#097fe8`): Pill badge text.

### Shadows & Depth
- **Card Shadow**: `rgba(0,0,0,0.04) 0px 4px 18px, rgba(0,0,0,0.027) 0px 2.025px 7.85px, rgba(0,0,0,0.02) 0px 0.8px 2.925px, rgba(0,0,0,0.01) 0px 0.175px 1.04px`
- **Deep Shadow**: `rgba(0,0,0,0.01) 0px 1px 3px, rgba(0,0,0,0.02) 0px 3px 7px, rgba(0,0,0,0.02) 0px 7px 15px, rgba(0,0,0,0.04) 0px 14px 28px, rgba(0,0,0,0.05) 0px 23px 52px`
- **Whisper Border**: `1px solid rgba(0,0,0,0.1)`

## 3. Typography Rules

### Font Family
- **Primary**: `NotionInter`, fallbacks: `Inter, -apple-system, system-ui, Segoe UI, Helvetica, Arial`
- OpenType features: `"lnum"` and `"locl"` enabled on display and heading text.

### Hierarchy

| Role | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|--------|-------------|----------------|-------|
| Display Hero | 64px (4rem) | 700 | 1.00 | -2.125px | Maximum compression |
| Display Secondary | 54px (3.38rem) | 700 | 1.04 | -1.875px | Secondary hero |
| Section Heading | 48px (3rem) | 700 | 1.00 | -1.5px | Feature sections |
| Sub-heading Large | 40px (2.5rem) | 700 | 1.50 | normal | Card headings |
| Sub-heading | 26px (1.63rem) | 700 | 1.23 | -0.625px | Section subtitles |
| Card Title | 22px (1.38rem) | 700 | 1.27 | -0.25px | Feature cards |
| Body Large | 20px (1.25rem) | 600 | 1.40 | -0.125px | Intro paragraphs |
| Body | 16px (1rem) | 400 | 1.50 | normal | Standard reading |
| Body Medium | 16px (1rem) | 500 | 1.50 | normal | Navigation, UI |
| Nav / Button | 15px (0.94rem) | 600 | 1.33 | normal | Navigation links |
| Caption | 14px (0.88rem) | 500 | 1.43 | normal | Metadata |
| Badge | 12px (0.75rem) | 600 | 1.33 | 0.125px | Pill badges |

### Principles
- **Compression at scale**: -2.125px at 64px, relaxing to -0.625px at 26px, normal at 16px.
- **Four-weight system**: 400 (read), 500 (interact), 600 (emphasize), 700 (announce).
- **Badge micro-tracking**: 12px badge text uses positive spacing (0.125px) — the only positive tracking.

## 4. Component Stylings

### Buttons

**Primary Blue**
- Background: `#0075de`
- Text: `#ffffff`
- Padding: 8px 16px
- Radius: 4px
- Hover: background darkens to `#005bab`
- Active: scale(0.9) transform

**Secondary**
- Background: `rgba(0,0,0,0.05)`
- Text: `#000000`
- Radius: 4px
- Hover: scale(1.05)

**Pill Badge**
- Background: `#f2f9ff`
- Text: `#097fe8`
- Padding: 4px 8px
- Radius: 9999px
- Font: 12px weight 600

### Cards & Containers
- Background: `#ffffff`
- Border: `1px solid rgba(0,0,0,0.1)`
- Radius: 12px standard, 16px featured
- Shadow: 4-layer stack (max opacity 0.04)

### Inputs & Forms
- Background: `#ffffff`
- Border: `1px solid #dddddd`
- Radius: 4px
- Focus: blue outline ring
- Placeholder: `#a39e98`

### Navigation
- Clean horizontal nav on white
- Links: NotionInter 15px weight 500-600
- CTA: blue pill button "Get Notion free" right-aligned
- Mobile: hamburger menu collapse

### Distinctive Components

**Feature Cards with Illustrations**
- Large illustrative headers (product UI screenshots)
- 12px radius card with whisper border
- Title at 22px weight 700, description at 16px weight 400

**Metric Cards**
- Large number display (e.g., "$4,200 ROI")
- NotionInter 40px+ weight 700 for the metric
- Whisper-bordered card container

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 2px, 3px, 4px, 5px, 6px, 7px, 8px, 11px, 12px, 14px, 16px, 24px, 32px

### Grid & Container
- Max content width: approximately 1200px
- Hero: centered single-column with generous top padding (80-120px)
- Full-width warm white (`#f6f5f4`) section backgrounds for alternation

### Whitespace Philosophy
- **Generous vertical rhythm**: 64-120px between major sections.
- **Warm alternation**: White sections alternate with warm white (`#f6f5f4`).
- **Content-first density**: Body text compact (1.50) surrounded by ample margin.

### Border Radius Scale
- Micro (4px): Buttons, inputs
- Standard (8px): Small cards
- Comfortable (12px): Standard cards, image tops
- Large (16px): Hero cards, featured content
- Full Pill (9999px): Badges, pills, status indicators

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No shadow | Page background |
| Whisper | `1px solid rgba(0,0,0,0.1)` | Card outlines, dividers |
| Soft Card | 4-layer shadow (max 0.04) | Content cards |
| Deep Card | 5-layer shadow (max 0.05, 52px blur) | Modals, hero elements |

**Shadow Philosophy**: Multiple layers with 0.01–0.05 individual opacity accumulate into soft, natural elevation. Elements feel embedded in the page rather than floating above it.

## 7. Do's and Don'ts

### Do
- Use warm neutrals — Notion's grays have yellow-brown undertones
- Letter-spacing scales with size: -2.125px at 64px, normal at 16px
- Use four weights: 400 (read), 500 (interact), 600 (emphasize), 700 (announce)
- Keep borders as whispers: `1px solid rgba(0,0,0,0.1)`
- Use 4-5 shadow layers with individual opacity never exceeding 0.05
- Use warm white (`#f6f5f4`) for section alternation
- Use Notion Blue (`#0075de`) sparingly — CTAs and links only

### Don't
- Don't use cool blue-grays — all grays must have warm undertones
- Don't use heavy borders or single-layer drop shadows
- Don't use pure black (#000000) for text — use rgba(0,0,0,0.95)
- Don't use radius larger than 4px on buttons and inputs (keep them subtle)
- Don't use bold display text without the matching tight letter-spacing

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <600px | Single column, stacked layout |
| Tablet | 768-1080px | Full card grids, expanded padding |
| Desktop | 1200-1440px | Full layout, max content width |

### Collapsing Strategy
- Hero: 64px → 40px → 26px, maintains proportional letter-spacing
- Navigation: horizontal + blue CTA → hamburger menu
- Feature cards: 3-column → 2-column → single column
- Section spacing: 80px+ → 48px on mobile

## 9. Agent Prompt Guide

### Quick Color Reference
- Primary CTA: Notion Blue (`#0075de`)
- Background: Pure White (`#ffffff`)
- Alt Background: Warm White (`#f6f5f4`)
- Heading: Near-Black (`rgba(0,0,0,0.95)`)
- Secondary text: Warm Gray 500 (`#615d59`)
- Muted text: Warm Gray 300 (`#a39e98`)
- Border: `1px solid rgba(0,0,0,0.1)`

### Example Component Prompts
- "Create a hero on white. Headline 64px NotionInter weight 700, line-height 1.00, letter-spacing -2.125px, color rgba(0,0,0,0.95). Subtitle 20px weight 600, color #615d59. Blue CTA (#0075de, 4px radius, 8px 16px padding)."
- "Design a card: white bg, 1px solid rgba(0,0,0,0.1) border, 12px radius. Shadow: rgba(0,0,0,0.04) 0px 4px 18px + 3 more layers. Title 22px weight 700 letter-spacing -0.25px. Body 16px weight 400, color #615d59."
- "Build a pill badge: #f2f9ff bg, #097fe8 text, 9999px radius, 4px 8px padding, 12px weight 600, letter-spacing 0.125px."
- "Section layout: white alternating with warm white (#f6f5f4). 64-80px vertical padding, max-width 1200px. Section heading 48px weight 700, line-height 1.00, letter-spacing -1.5px."
