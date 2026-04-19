# Design System Inspired by Claude (Anthropic)

## 1. Visual Theme & Atmosphere

Claude's interface is a literary salon reimagined as a product page — warm, unhurried, and quietly intellectual. The entire experience is built on a parchment-toned canvas (`#f5f4ed`) that deliberately evokes the feeling of high-quality paper rather than a digital surface. Where most AI product pages lean into cold, futuristic aesthetics, Claude's design radiates human warmth, as if the AI itself has good taste in interior design.

The signature move is the custom Anthropic Serif typeface — a medium-weight serif with generous proportions that gives every headline the gravitas of a book title. Combined with organic, hand-drawn-feeling illustrations in terracotta (`#c96442`), black, and muted green, the visual language says "thoughtful companion" rather than "powerful tool." The serif headlines breathe at tight-but-comfortable line-heights (1.10–1.30), creating a cadence that feels more like reading an essay than scanning a product page.

What makes Claude's design truly distinctive is its warm neutral palette. Every gray has a yellow-brown undertone (`#5e5d59`, `#87867f`, `#4d4c48`) — there are no cool blue-grays anywhere. Borders are cream-tinted (`#f0eee6`, `#e8e6dc`), shadows use warm transparent blacks, and even the darkest surfaces (`#141413`, `#30302e`) carry a barely perceptible olive warmth.

**Key Characteristics:**
- Warm parchment canvas (`#f5f4ed`) evoking premium paper, not screens
- Custom Anthropic type family: Serif for headlines, Sans for UI, Mono for code
- Terracotta brand accent (`#c96442`) — warm, earthy, deliberately un-tech
- Exclusively warm-toned neutrals — every gray has a yellow-brown undertone
- Organic, editorial illustrations replacing typical tech iconography
- Ring-based shadow system (`0px 0px 0px 1px`) creating border-like depth
- Magazine-like pacing with generous section spacing and serif-driven hierarchy

## 2. Color Palette & Roles

### Primary
- **Anthropic Near Black** (`#141413`): Primary text color — warm, almost olive-tinted dark.
- **Terracotta Brand** (`#c96442`): Core brand color — burnt orange-brown for primary CTAs.
- **Coral Accent** (`#d97757`): Lighter warm variant for text accents and links on dark surfaces.

### Secondary & Accent
- **Error Crimson** (`#b53333`): Deep warm red for error states.
- **Focus Blue** (`#3898ec`): Standard blue for input focus rings — the only cool color in the system.

### Surface & Background
- **Parchment** (`#f5f4ed`): Primary page background — warm cream with yellow-green tint.
- **Ivory** (`#faf9f5`): Lightest surface for cards on Parchment background.
- **Pure White** (`#ffffff`): Reserved for specific button surfaces.
- **Warm Sand** (`#e8e6dc`): Button backgrounds and prominent interactive surfaces.
- **Dark Surface** (`#30302e`): Dark-theme containers and elevated dark elements.
- **Deep Dark** (`#141413`): Dark-theme page background and primary dark surface.

### Neutrals & Text
- **Charcoal Warm** (`#4d4c48`): Button text on light warm surfaces.
- **Olive Gray** (`#5e5d59`): Secondary body text.
- **Stone Gray** (`#87867f`): Tertiary text, footnotes, de-emphasized metadata.
- **Warm Silver** (`#b0aea5`): Text on dark surfaces.

### Semantic
- **Border Cream** (`#f0eee6`): Standard light-theme border — barely visible warm cream.
- **Border Warm** (`#e8e6dc`): Prominent borders and section dividers.

## 3. Typography Rules

### Font Family
- **Headline**: `Anthropic Serif`, fallback: `Georgia`
- **Body / UI**: `Anthropic Sans`, fallback: `Arial`
- **Code**: `Anthropic Mono`, fallback: `Arial`

### Hierarchy

| Role | Font | Size | Weight | Line Height | Notes |
|------|------|------|--------|-------------|-------|
| Display / Hero | Anthropic Serif | 64px (4rem) | 500 | 1.10 | Maximum impact |
| Section Heading | Anthropic Serif | 52px (3.25rem) | 500 | 1.20 | Feature section anchors |
| Sub-heading Large | Anthropic Serif | 36px (~2.3rem) | 500 | 1.30 | Secondary section markers |
| Sub-heading | Anthropic Serif | 32px (2rem) | 500 | 1.10 | Card titles |
| Body Serif | Anthropic Serif | 17px (1.06rem) | 400 | 1.60 | Editorial passages |
| Body Large | Anthropic Sans | 20px (1.25rem) | 400 | 1.60 | Intro paragraphs |
| Body / Nav | Anthropic Sans | 17px (1.06rem) | 400–500 | 1.00–1.60 | Navigation links, UI text |
| Caption | Anthropic Sans | 14px (0.88rem) | 400 | 1.43 | Metadata |
| Label | Anthropic Sans | 12px (0.75rem) | 400–500 | 1.25–1.60 | Badges, small labels |
| Code | Anthropic Mono | 15px (0.94rem) | 400 | 1.60 | Inline code |

### Principles
- **Serif for authority, sans for utility**: Anthropic Serif carries all headlines at weight 500.
- **Single weight for serifs**: All headlines use weight 500 — no bold, no light.
- **Relaxed body line-height**: 1.60 — closer to a book than a dashboard.
- **Tight-but-not-compressed headings**: 1.10–1.30 line-heights.

## 4. Component Stylings

### Buttons

**Warm Sand (Secondary)**
- Background: Warm Sand (`#e8e6dc`)
- Text: Charcoal Warm (`#4d4c48`)
- Padding: 0px 12px 0px 8px
- Radius: 8px
- Shadow: ring-based (`#d1cfc5 0px 0px 0px 1px`)

**Brand Terracotta**
- Background: Terracotta Brand (`#c96442`)
- Text: Ivory (`#faf9f5`)
- Radius: 8–12px
- The primary CTA — the only button with chromatic color

**Dark Primary**
- Background: Anthropic Near Black (`#141413`)
- Text: Warm Silver (`#b0aea5`)
- Padding: 9.6px 16.8px
- Radius: 12px

### Cards & Containers
- Background: Ivory (`#faf9f5`) on light; Dark Surface (`#30302e`) on dark
- Border: `1px solid #f0eee6` on light; `1px solid #30302e` on dark
- Radius: 8px standard; 16px featured; 32px hero containers
- Shadow: `rgba(0,0,0,0.05) 0px 4px 24px`

### Navigation
- Sticky top nav with warm background
- Logo: Claude wordmark in Anthropic Near Black
- Links: Near Black (`#141413`), Olive Gray (`#5e5d59`)
- CTA: Terracotta Brand button

### Distinctive Components

**Organic Illustrations**
- Hand-drawn-feeling vector illustrations in terracotta, black, and muted green
- Abstract, conceptual — the primary visual personality

**Dark/Light Section Alternation**
- Alternates between Parchment light and Near Black dark sections
- Creates a reading rhythm like chapters in a book

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 3px, 4px, 6px, 8px, 10px, 12px, 16px, 20px, 24px, 30px
- Section vertical spacing: 80–120px between major sections

### Grid & Container
- Max container width: approximately 1200px, centered
- Feature sections: single-column or 2–3 column card grids
- Full-width dark sections breaking the container for emphasis

### Border Radius Scale
- Comfortably rounded (8–8.5px): Standard buttons, cards
- Generously rounded (12px): Primary buttons, input fields
- Very rounded (16px): Featured containers, video players
- Maximum rounded (32px): Hero containers, large cards

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No shadow | Parchment background |
| Contained | `1px solid #f0eee6` | Standard cards |
| Ring | `0px 0px 0px 1px` warm ring shadows | Interactive cards, buttons |
| Whisper | `rgba(0,0,0,0.05) 0px 4px 24px` | Elevated feature cards |

**Shadow Philosophy**: Depth through warm-toned ring shadows (`0px 0px 0px 1px`). Drop shadows are extremely soft (0.05 opacity, 24px blur). Light/Dark alternation provides the most dramatic depth effect.

## 7. Do's and Don'ts

### Do
- Use Parchment (`#f5f4ed`) as the primary light background
- Use Anthropic Serif at weight 500 for all headlines
- Use Terracotta Brand (`#c96442`) only for primary CTAs
- Keep all neutrals warm-toned — every gray should have a yellow-brown undertone
- Use ring shadows (`0px 0px 0px 1px`) for interactive states
- Use generous body line-height (1.60)
- Apply generous border-radius (12–32px)

### Don't
- Don't use cool blue-grays anywhere
- Don't use bold (700+) weight on Anthropic Serif
- Don't introduce saturated colors beyond Terracotta
- Don't use sharp corners (< 6px) on buttons or cards
- Don't use pure white (`#ffffff`) as a page background
- Don't use geometric/tech-style illustrations
- Don't mix in sans-serif for headlines

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <479px | Single column, hamburger nav |
| Tablet | 768–991px | 2-column grids begin |
| Desktop | 992px+ | Full multi-column layout, 64px hero typography |

### Collapsing Strategy
- Hero text: 64px → 36px → ~25px
- Navigation: Full horizontal → hamburger
- Feature sections: Multi-column → stacked
- Model cards: 3-column → stacked vertical

## 9. Agent Prompt Guide

### Quick Color Reference
- Brand CTA: Terracotta Brand (`#c96442`)
- Page Background: Parchment (`#f5f4ed`)
- Card Surface: Ivory (`#faf9f5`)
- Primary Text: Anthropic Near Black (`#141413`)
- Secondary Text: Olive Gray (`#5e5d59`)
- Tertiary Text: Stone Gray (`#87867f`)
- Borders (light): Border Cream (`#f0eee6`)
- Dark Surface: Dark Surface (`#30302e`)

### Example Component Prompts
- "Create a hero section on Parchment (#f5f4ed) with a headline at 64px Anthropic Serif weight 500, line-height 1.10. Use Anthropic Near Black (#141413) text. Add a subtitle in Olive Gray (#5e5d59) at 20px Anthropic Sans. Place a Terracotta Brand (#c96442) CTA button with Ivory text, 12px radius."
- "Design a feature card on Ivory (#faf9f5) with a 1px solid Border Cream (#f0eee6) border, 8px radius. Title in Anthropic Serif at 25px weight 500, description in Olive Gray at 16px Anthropic Sans. Add whisper shadow (rgba(0,0,0,0.05) 0px 4px 24px)."
- "Build a dark section on Anthropic Near Black (#141413) with Ivory (#faf9f5) headline in Anthropic Serif at 52px weight 500. Use Warm Silver (#b0aea5) for body text."
