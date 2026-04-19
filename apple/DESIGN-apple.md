# Design System Inspired by Apple

## 1. Visual Theme & Atmosphere

Apple's website is a masterclass in controlled drama — vast expanses of pure black and near-white serve as cinematic backdrops for products that are photographed as if they were sculptures in a gallery. The design philosophy is reductive to its core: every pixel exists in service of the product, and the interface itself retreats until it becomes invisible. This is not minimalism as aesthetic preference; it is minimalism as reverence for the object.

The typography anchors everything. San Francisco (SF Pro Display for large sizes, SF Pro Text for body) is Apple's proprietary typeface, engineered with optical sizing that automatically adjusts letterforms depending on point size. At display sizes (56px), weight 600 with a tight line-height of 1.07 and subtle negative letter-spacing (-0.28px) creates headlines that feel machined rather than typeset — precise, confident, and unapologetically direct. At body sizes (17px), the tracking loosens slightly (-0.374px) and line-height opens to 1.47, creating a reading rhythm that is comfortable without ever feeling slack.

The color story is starkly binary. Product sections alternate between pure black (`#000000`) backgrounds with white text and light gray (`#f5f5f7`) backgrounds with near-black text (`#1d1d1f`). This creates a cinematic pacing — dark sections feel immersive and premium, light sections feel open and informational. The only chromatic accent is Apple Blue (`#0071e3`), reserved exclusively for interactive elements: links, buttons, and focus states. This singular accent color in a sea of neutrals gives every clickable element unmistakable visibility.

**Key Characteristics:**
- SF Pro Display/Text with optical sizing — letterforms adapt automatically to size context
- Binary light/dark section rhythm: black (`#000000`) alternating with light gray (`#f5f5f7`)
- Single accent color: Apple Blue (`#0071e3`) reserved exclusively for interactive elements
- Product-as-hero photography on solid color fields — no gradients, no textures, no distractions
- Extremely tight headline line-heights (1.07-1.14) creating compressed, billboard-like impact
- Full-width section layout with centered content — the viewport IS the canvas
- Pill-shaped CTAs (980px radius) creating soft, approachable action buttons
- Generous whitespace between sections allowing each product moment to breathe

## 2. Color Palette & Roles

### Primary
- **Pure Black** (`#000000`): Hero section backgrounds, immersive product showcases. The darkest canvas for the brightest products.
- **Light Gray** (`#f5f5f7`): Alternate section backgrounds, informational areas. Not white — the slight blue-gray tint prevents sterility.
- **Near Black** (`#1d1d1f`): Primary text on light backgrounds, dark button fills. Slightly warmer than pure black for comfortable reading.

### Interactive
- **Apple Blue** (`#0071e3`): `--sk-focus-color`, primary CTA backgrounds, focus rings. The ONLY chromatic color in the interface.
- **Link Blue** (`#0066cc`): `--sk-body-link-color`, inline text links. Slightly darker than Apple Blue for text-level readability.
- **Bright Blue** (`#2997ff`): Links on dark backgrounds. Higher luminance for contrast on black sections.

### Text
- **White** (`#ffffff`): Text on dark backgrounds, button text on blue/dark CTAs.
- **Near Black** (`#1d1d1f`): Primary body text on light backgrounds.
- **Black 80%** (`rgba(0, 0, 0, 0.8)`): Secondary text, nav items on light backgrounds. Slightly softened.
- **Black 48%** (`rgba(0, 0, 0, 0.48)`): Tertiary text, disabled states, carousel controls.

### Surface & Dark Variants
- **Dark Surface 1** (`#272729`): Card backgrounds in dark sections.
- **Dark Surface 2** (`#262628`): Subtle surface variation in dark contexts.
- **Dark Surface 3** (`#28282a`): Elevated cards on dark backgrounds.
- **Dark Surface 4** (`#2a2a2d`): Highest dark surface elevation.
- **Dark Surface 5** (`#242426`): Deepest dark surface tone.

### Button States
- **Button Active** (`#ededf2`): Active/pressed state for light buttons.
- **Button Default Light** (`#fafafc`): Search/filter button backgrounds.
- **Overlay** (`rgba(210, 210, 215, 0.64)`): Media control scrims, overlays.
- **White 32%** (`rgba(255, 255, 255, 0.32)`): Hover state on dark modal close buttons.

### Shadows
- **Card Shadow** (`rgba(0, 0, 0, 0.22) 3px 5px 30px 0px`): Soft, diffused elevation for product cards.

## 3. Typography Rules

### Font Family
- **Display**: `SF Pro Display`, with fallbacks: `SF Pro Icons, Helvetica Neue, Helvetica, Arial, sans-serif`
- **Body**: `SF Pro Text`, with fallbacks: `SF Pro Icons, Helvetica Neue, Helvetica, Arial, sans-serif`
- SF Pro Display is used at 20px and above; SF Pro Text is optimized for 19px and below.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | SF Pro Display | 56px (3.50rem) | 600 | 1.07 (tight) | -0.28px | Product launch headlines |
| Section Heading | SF Pro Display | 40px (2.50rem) | 600 | 1.10 (tight) | normal | Feature section titles |
| Tile Heading | SF Pro Display | 28px (1.75rem) | 400 | 1.14 (tight) | 0.196px | Product tile headlines |
| Card Title | SF Pro Display | 21px (1.31rem) | 700 | 1.19 (tight) | 0.231px | Bold card headings |
| Body | SF Pro Text | 17px (1.06rem) | 400 | 1.47 | -0.374px | Standard reading text |
| Button | SF Pro Text | 17px (1.06rem) | 400 | 2.41 (relaxed) | normal | Standard button text |
| Link | SF Pro Text | 14px (0.88rem) | 400 | 1.43 | -0.224px | Body links |
| Caption | SF Pro Text | 14px (0.88rem) | 400 | 1.29 (tight) | -0.224px | Secondary text |
| Micro | SF Pro Text | 12px (0.75rem) | 400 | 1.33 | -0.12px | Fine print |

## 4. Component Stylings

### Buttons

**Primary Blue (CTA)**
- Background: `#0071e3` (Apple Blue)
- Text: `#ffffff`
- Padding: 8px 15px
- Radius: 8px
- Font: SF Pro Text, 17px, weight 400
- Use: Primary call-to-action ("Buy", "Shop iPhone")

**Pill Link (Learn More / Shop)**
- Background: transparent
- Text: `#0066cc` (light bg) or `#2997ff` (dark bg)
- Radius: 980px (full pill)
- Border: 1px solid `#0066cc`
- Font: SF Pro Text, 14px-17px
- Use: "Learn more" and "Shop" links

### Cards & Containers
- Background: `#f5f5f7` (light) or `#272729`-`#2a2a2d` (dark)
- Radius: 5px-8px
- Shadow: `rgba(0, 0, 0, 0.22) 3px 5px 30px 0px` for elevated product cards

### Navigation
- Background: `rgba(0, 0, 0, 0.8)` with `backdrop-filter: saturate(180%) blur(20px)`
- Height: 48px
- Text: `#ffffff` at 12px, weight 400

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 2px, 4px, 5px, 6px, 7px, 8px, 9px, 10px, 11px, 14px, 15px, 17px, 20px, 24px

### Grid & Container
- Max content width: approximately 980px
- Hero: full-viewport-width sections with centered content block
- Single-column for hero moments — one product, one message, full attention

### Border Radius Scale
- Micro (5px): Small containers
- Standard (8px): Buttons, product cards
- Comfortable (11px): Search inputs
- Large (12px): Feature panels
- Full Pill (980px): CTA links
- Circle (50%): Media controls

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (Level 0) | No shadow | Standard content sections |
| Navigation Glass | `backdrop-filter: saturate(180%) blur(20px)` on `rgba(0,0,0,0.8)` | Sticky nav |
| Subtle Lift (Level 1) | `rgba(0, 0, 0, 0.22) 3px 5px 30px 0px` | Product cards |
| Focus | `2px solid #0071e3` | Keyboard focus |

## 7. Do's and Don'ts

### Do
- Use SF Pro Display at 20px+ and SF Pro Text below 20px
- Apply negative letter-spacing at all text sizes
- Use Apple Blue (`#0071e3`) ONLY for interactive elements
- Alternate between black and light gray (`#f5f5f7`) section backgrounds
- Use 980px pill radius for CTA links
- Compress headline line-heights to 1.07-1.14

### Don't
- Don't introduce additional accent colors
- Don't use heavy shadows or multiple shadow layers
- Don't use borders on cards or containers
- Don't apply wide letter-spacing to SF Pro
- Don't add textures, patterns, or gradients to backgrounds
- Don't make the navigation opaque

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | 360-480px | Standard mobile layout |
| Tablet | 834-1024px | Full tablet layout |
| Desktop | 1070-1440px | Full layout, max content width |

### Collapsing Strategy
- Hero headlines: 56px → 40px → 28px on mobile
- Product grids: 3-column → 2-column → single column
- Navigation: full horizontal nav → compact mobile menu

## 9. Agent Prompt Guide

### Quick Color Reference
- Primary CTA: Apple Blue (`#0071e3`)
- Page background (light): `#f5f5f7`
- Page background (dark): `#000000`
- Heading text (light): `#1d1d1f`
- Heading text (dark): `#ffffff`
- Link (light bg): `#0066cc`
- Link (dark bg): `#2997ff`

### Example Component Prompts
- "Create a hero section on black background. Headline at 56px SF Pro Display weight 600, line-height 1.07, letter-spacing -0.28px, color white. Two pill CTAs: 'Learn more' (transparent bg, white text, 1px solid white border, 980px radius) and 'Buy' (Apple Blue #0071e3 bg, white text, 8px radius)."
- "Design a product card: #f5f5f7 background, 8px border-radius, no border, no shadow. Title at 28px SF Pro Display weight 400. 'Learn more' and 'Shop' links in #0066cc at 14px."
