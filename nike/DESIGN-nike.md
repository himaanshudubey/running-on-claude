# Design System Inspired by Nike

## 1. Visual Theme & Atmosphere

Nike.com is a kinetic retail cathedral — a site that channels the explosive energy of sport into a digital shopping experience. The design operates on a principle of radical simplicity: strip everything back to black, white, and grey so that athletic photography and product color can dominate without competition. The result feels less like a website and more like a sports editorial laid out with the precision of a luxury magazine.

The "Podium CDS" (Nike's internal Core Design System) establishes an aggressively monochromatic foundation. The UI disappears into black (`#111111`) text and white surfaces, allowing hero photography — sweating athletes, mid-air shoes, stadium energy — to carry the emotional weight. The product itself is the color story.

The typography system is Nike's other half. Massive uppercase headlines in Nike Futura ND — a custom condensed Futura variant with impossibly tight line-height (0.90) — punch through hero imagery like a typographic shockwave. Below the headlines, Helvetica Now handles everything from navigation to product descriptions with Swiss-precision clarity.

**Key Characteristics:**
- Monochromatic UI (black/white/grey) — product photography is the only color source
- Massive uppercase display typography (96px, line-height 0.90) punching through hero images
- Full-bleed photography with no border radius — imagery fills every available edge
- Pill-shaped buttons (30px radius) as the primary interactive element
- 8px spacing grid with athletic discipline
- Shadow-free, border-minimal elevation model — surface differentiation through grey shifts only

## 2. Color Palette & Roles

### Primary
- **Nike Black** (`#111111`): Foundation — primary text, button backgrounds, nav text. Not pure black.
- **Nike White** (`#FFFFFF`): Primary page canvas, button text on dark, card surfaces.

### Surface & Background
- **Snow** (`#FAFAFA`): Lightest surface, near-white differentiation
- **Light Gray** (`#F5F5F5`): Secondary background, search input fill, loading skeleton
- **Hover Gray** (`#E5E5E5`): Hover state background, disabled button fill
- **Dark Surface** (`#28282A`): Primary background on dark/inverted sections
- **Deep Charcoal** (`#1F1F21`): Inverse primary background

### Neutrals & Text
- **Primary Text** (`#111111`): Main body text, headings, nav links
- **Secondary Text** (`#707072`): Descriptive copy, metadata, price labels
- **Disabled Text** (`#9E9EA0`): Inactive elements, unavailable options
- **Border Secondary** (`#CACACB`): Subtle borders, input borders, divider lines

### Semantic & Accent
- **Nike Red** (`#D30005`): Critical errors, sale badges
- **Nike Orange Badge** (`#D33918`): Badge text, promotional callouts
- **Success Green** (`#007D48`): Confirmation, availability, positive states
- **Link Blue** (`#1151FF`): Text links, informational highlights
- **Focus Ring** (`rgba(39, 93, 197, 1)`): Keyboard focus indicator

## 3. Typography Rules

### Font Family
- **Display:** Nike Futura ND (custom condensed Futura) — fallbacks: Helvetica Now Text Medium, Helvetica, Arial
- **Heading:** Helvetica Now Display Medium — fallbacks: Helvetica, Arial
- **Body Medium:** Helvetica Now Text Medium (weight 500)
- **Body:** Helvetica Now Text (weight 400)

### Hierarchy

| Role | Size | Weight | Line Height | Notes |
|------|------|--------|-------------|-------|
| Display | 96px | 500 | 0.90 | Nike Futura ND, uppercase, hero headlines |
| Heading 1 | 32px | 500 | 1.20 | Helvetica Now Display, section titles |
| Heading 2 | 24px | 500 | 1.20 | Subsections |
| Body | 16px | 400 | 1.75 | Product descriptions |
| Body Medium | 16px | 500 | 1.75 | Emphasized text |
| Button | 16px | 500 | 1.50 | CTA text |
| Caption | 14px | 500 | 1.50 | Price labels |
| Small | 12px | 500 | 1.50 | Timestamps |

### Principles
Nike's typography is a study in tension. The display layer (Nike Futura ND at 96px, 0.90 line-height) is engineered to feel like a stadium scoreboard. Below it, Helvetica Now provides clinical counterpoint with generous 1.75 line-height. Weight 500 (Medium) dominates throughout — every sentence reads like a confident recommendation.

## 4. Component Stylings

### Buttons

**Primary**
- Background: Nike Black (`#111111`)
- Text: White (`#FFFFFF`), 16px/500
- Border radius: 30px (full pill)
- Padding: ~12px 24px
- Hover: background shifts to Grey-500 (`#707072`)
- Focus: 2px box-shadow in `rgba(39, 93, 197, 1)`

**Primary on Dark**
- Background: White (`#FFFFFF`)
- Text: Black (`#111111`)
- Hover: background shifts to Grey-300 (`#CACACB`)

**Secondary (Outlined)**
- Background: transparent
- Border: 1.5px solid `#CACACB`
- Border radius: 30px
- Hover: border darkens to `#707072`

**Disabled**
- Background: Grey-200 (`#E5E5E5`)
- Text: Grey-400 (`#9E9EA0`)

### Cards & Containers
- Background: White (`#FFFFFF`)
- Border radius: 0px for product image cards; 20px for interactive containers
- Shadow: none — Nike uses no card shadows
- Product cards: image on top (no radius), text metadata below

### Inputs & Forms
- Background: Grey-100 (`#F5F5F5`)
- Border radius: 24px (search), 8px (form inputs)
- Focus: border shifts to `#111111`, 2px focus ring in `rgba(39, 93, 197, 1)`

### Navigation
- Background: White (`#FFFFFF`), sticky, ~60px height
- Left: Nike Swoosh logo
- Center: Category links in 16px/500 Helvetica Now
- Right: Search (24px radius), Favorites, Cart icons
- Top banner: `#111111` bg with white text for promotions

### Image Treatment
- Hero images: full-bleed, no border radius, edge-to-edge
- Product grid: square (1:1) or 4:3, no border radius
- Product hover: secondary image swap (front → side view)

## 5. Layout Principles

### Spacing System
| Token | Value | Use |
|-------|-------|-----|
| space-2 | 8px | Base unit |
| space-3 | 12px | Card padding |
| space-4 | 16px | Standard padding |
| space-6 | 24px | Section padding |
| space-8 | 48px | Major section padding |
| space-9 | 64px | Hero padding |

### Grid & Container
- Max container width: 1920px
- Product grid: 3-column desktop, 2-column tablet, 1-column mobile
- Grid gap: 4-12px between product cards (intentionally tight)
- Horizontal padding: 48px desktop, 24px tablet, 16px mobile

### Border Radius Scale
| Value | Context |
|-------|---------|
| 0px | Product images, hero photography |
| 8px | Form inputs |
| 20px | Containers, UI cards |
| 24px | Search inputs |
| 30px | Buttons, tags, filters |
| 50% | Circular icon buttons |

## 6. Depth & Elevation

Nike's elevation philosophy is radically flat. No card shadows, no hover lifts, no floating elements. Depth communicated exclusively through color shifts.

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No shadow, no border | Default for everything |
| Divider | `0px -1px 0px 0px #E5E5E5 inset` | Between sections |
| Focus | `0 0 0 2px rgba(39, 93, 197, 1)` | Keyboard focus ring |

## 7. Do's and Don'ts

### Do
- Use Nike Black (`#111111`) for all primary text — never pure `#000000`
- Keep buttons pill-shaped (30px radius)
- Use full-bleed, edge-to-edge photography for hero sections
- Let product photography provide all color vibrancy
- Use uppercase Nike Futura ND ONLY for display headlines (96px+)
- Reserve color exclusively for semantic meaning (red=error, green=success)

### Don't
- Don't add shadows to cards — entirely flat
- Don't use border radius on product imagery
- Don't introduce brand colors for UI elements
- Don't use Nike Futura ND below 24px
- Don't add hover lift effects
- Don't use regular weight (400) for buttons or links

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <640px | Single column, hamburger nav, 16px padding |
| Tablet | 768-960px | 2-column grids, 24px padding |
| Desktop | 1024-1440px | Full layout, 3-column grids, 48px padding |

### Collapsing Strategy
- Display text: 96px → 64px → 48px; hero images remain full-bleed
- Navigation: Full category links → hamburger below 960px
- Product grids: 3-col → 2-col at 960px → 1-col at 640px

## 9. Agent Prompt Guide

### Quick Color Reference
- Primary CTA: Nike Black (`#111111`)
- Background: White (`#FFFFFF`)
- Secondary surface: Light Gray (`#F5F5F5`)
- Heading text: Nike Black (`#111111`)
- Body/hover: Secondary Text (`#707072`)
- Border: Border Secondary (`#CACACB`)
- Error: Nike Red (`#D30005`)

### Example Component Prompts
- "Create a product hero with full-bleed edge-to-edge photography, no border radius, dark gradient overlay, massive uppercase 96px/500 headline with 0.90 line-height, and a Nike Black pill button (30px radius)."
- "Design a 3-column product card grid: square images (no border radius), 4px gap, product name 16px/500 Nike Black, price 14px/500, secondary text in Grey-500 (#707072)."
- "Build a sticky white nav: left-aligned Swoosh logo, centered category links 16px/500 (#111111) hover #707072, right-aligned search (24px radius, #F5F5F5 bg), favorites, cart."
