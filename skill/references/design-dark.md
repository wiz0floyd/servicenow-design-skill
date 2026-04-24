# Design System Inspired by ServiceNow — Dark Mode

> This is the **dark mode** version of the ServiceNow design system. It is fully self-contained — use this document alone when building dark-themed interfaces. No reference to the light-mode DESIGN.md is needed.

## 1. Visual Theme & Atmosphere

ServiceNow is the largest enterprise workflow platform company that most consumers have never heard of — $100B+ in market cap, selling the invisible infrastructure behind IT service desks, HR systems, and customer service operations at most Fortune 500 companies. The dark mode adaptation leans into what the live site already does well — servicenow.com is a **primarily dark-themed site by default**, using Deep Navy-Teal (`#032d42`) as its dominant hero, nav, and platform-page canvas. The dark mode version deepens this to **Abyssal Navy-Teal** (`#021a26`) as the canvas, with `#032d42` becoming a surface tier, `#042f45` for cards, and `#063e5a` for elevated modals — all preserving the brand's blue-green undertone without going pure black.

The **ServiceNow Green** (`#63df4e`) accent is preserved identically — it reads even more vividly against the deeper dark canvas. The signature **"Put AI to work for [X]"** hero formula continues with green keyword + white trailing phrase treatment. Aurora gradient banners, dotted particle starfield backgrounds, sub-navigation with green active underlines, and persistent floating green FAB pills (Contact, Demo) all remain unchanged in their color treatment — they were designed for dark canvases from the start.

Body text softens to **78% warm-white opacity** for reading comfort; headings remain pure white. Translucent white borders (`rgba(255,255,255,0.1)` standard, `rgba(255,255,255,0.18)` stronger) replace the light mode's Neutral Gray hairlines. **ServiceNow Sans** (Bold / Light / Book / Regular / Mono Regular) typography system is unchanged — weight ceiling stays at 700 with negative letter-spacing on display sizes.

**Key Characteristics:**
- Abyssal Navy-Teal canvas (`#021a26`) with surface ladder through `#032d42` → `#042f45` → `#063e5a` — never pure black
- ServiceNow Green (`#63df4e`) accent preserved identically
- Aurora gradient announcement banner preserved unchanged (aurora is a native-dark treatment)
- Dotted particle starfield backgrounds continue on hero and platform sections
- Three-tier text opacity: `#ffffff` headings / `rgba(255,255,255,0.78)` body / `rgba(255,255,255,0.5)` tertiary
- Translucent white borders at 10% / 18% opacity replacing neutral gray hairlines
- Full pill buttons (500px radius) with 2px border — Green Filled, White Outlined, Green Outlined variants
- Floating green FAB pills (Contact, Demo) continue as persistent right-edge CTAs
- Sub-navigation with green active underline unchanged
- ServiceNow Sans proprietary typography family preserved

**Color-block page rhythm (dark mode):** Aurora gradient banner → Navy-Teal nav → Deep abyssal canvas hero with dotted particles → Navy-Teal surface sections → Cards on slightly lighter elevated tier → Deep abyssal footer.

## 2. Color Palette & Roles

### Primary

- **Deep Navy-Teal** (`#032d42`): The brand's primary color — in dark mode functions as a surface tier rather than the dominant canvas. Used for nav, section surfaces, and card backgrounds
- **ServiceNow Green** (`#63df4e`): The signature accent — preserved identically. Used for CTA fills, hero keyword emphasis, active-tab underlines, logo dot, and floating FAB pills

### Secondary & Accent

- **Aurora Bright Blue** (`#52b8ff`): `--northern-light-aurora-color-2` — aurora gradient stop, decorative particle dots on dark surfaces
- **Aurora Link Teal** (`#00718f`): Inline link color — works on both light and dark context
- **Aurora Hover Teal** (`#024f69`): Darker link-hover variant
- **Visited Purple** (`#7057c7`): Visited link state
- **Pale Job Green** (`#e0f7dc`): Careers job-card hover surface — preserved as an accent for light-island moments

### Surface & Background

- **Abyssal Navy-Teal Canvas** (`#021a26`): Primary dark canvas — deepened from brand primary, carries the blue-green undertone
- **Surface** (`#032d42`): Alternating section surface — the brand primary doubles as a surface tier
- **Card** (`#042f45`): Card containers — subtle lift from Surface
- **Elevated** (`#063e5a`): Modals, elevated panels, brightest surface tier

### Neutrals & Text

- **Heading White** (`#ffffff`): All headings, button labels on dark
- **Body Text** (`rgba(255, 255, 255, 0.78)`): Primary body copy — 78% opacity for reading comfort
- **Tertiary Text** (`rgba(255, 255, 255, 0.5)`): Captions, metadata, eyebrows
- **Muted Text** (`rgba(255, 255, 255, 0.3)`): Disabled text, placeholders
- **Border Standard** (`rgba(255, 255, 255, 0.1)`): Card borders, divider hairlines
- **Border Strong** (`rgba(255, 255, 255, 0.18)`): Interactive element borders

### Semantic

No dedicated error/warning/success palette was extractable from the pages. Status states would extend the existing Green / Aurora-Teal vocabulary.

### Gradient System

- **Aurora Announcement Banner**: `linear-gradient(90deg, #b4ea9f 0%, #7fd8ce 40%, #52b8ff 70%, #9c87df 100%)` — preserved unchanged; the gradient reads even more vividly over the dark canvas
- **Aurora Gradient Border** (for featured cards): `linear-gradient(135deg, rgba(82, 184, 255, 0.7), rgba(99, 223, 78, 0.6), rgba(112, 87, 199, 0.6))` — used as a 2px border treatment around dark-surface featured cards

## 3. Typography Rules

### Font Family

- **Display / Headings**: `ServiceNowSansBold` — proprietary, 64/48/28/18px display sizes with tight 1.10 line-height
- **Body / UI**: `ServiceNowSansLight` — body workhorse; note the unusual 1.79 relaxed line-height on compact buttons
- **Secondary Body**: `ServiceNowSansBook` — mid-weight for paragraphs and button labels
- **Body Regular**: `ServiceNowSansRegular` — standard weight
- **Monospace**: `ServiceNowSansMonoRegular` — code-style uppercase captions
- **Full fallback chain**: `-apple-system, system-ui, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"`

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Color | Notes |
|------|------|------|--------|-------------|----------------|-------|-------|
| Display Hero | ServiceNowSansBold | 64px (4rem) | 700 | 1.10 | -0.64px | `#ffffff` | Primary hero ("Put AI to work...") |
| Display Large | ServiceNowSansBold | 48px (3rem) | 700 | 1.10 | -0.48px | `#ffffff` | Section leads |
| Heading Medium | ServiceNowSansBold | 28px (1.75rem) | 700 | 1.10 | -0.28px | `#ffffff` | Subsection headings |
| Heading Small | ServiceNowSansBold | 18px (1.13rem) | 700 | 1.10 | normal | `#ffffff` | Card titles |
| Body Large Link | ServiceNowSansLight | 20px (1.25rem) | 400 | 1.50 | normal | `rgba(255,255,255,0.78)` | Lead links, nav items |
| Body | ServiceNowSansLight | 16px (1rem) | 400 | 1.50 | normal | `rgba(255,255,255,0.78)` | Primary body text |
| Body Small | ServiceNowSansLight | 14px (0.88rem) | 500 | 1.43 | normal | `rgba(255,255,255,0.78)` | Secondary body |
| Button Large | ServiceNowSansBold | 28px (1.75rem) | 700 | 1.10 | -0.28px | varies | Oversized hero button |
| Button Medium | ServiceNowSansBook | 18px (1.13rem) | 400 | 1.50 | normal | varies | Standard button |
| Button Default | ServiceNowSansBook | 16px (1rem) | 400 | 1.50 | normal | varies | Default pill button |
| Button Small | ServiceNowSansLight | 14px (0.88rem) | 450 | 1.79 | normal | varies | Compact button (unusual relaxed line-height) |
| Caption | ServiceNowSansLight | 14px (0.88rem) | 500 | 1.43 | normal | `rgba(255,255,255,0.5)` | Labels, metadata |
| Caption Uppercase | ServiceNowSansMonoRegular | 14px (0.88rem) | 400 | 1.50 | normal (uppercase) | `rgba(255,255,255,0.5)` | Code-style labels ("INTRODUCING") |

### Principles

Same binary as light mode — ServiceNowSansBold for display, Light/Book/Regular for body. In dark mode, body opacity shifts to 78% for eye comfort. Weight ceiling stays at 700 with aggressive negative letter-spacing on display. The 1.79 relaxed button line-height quirk is preserved.

### Note on Font Substitutes

ServiceNowSans is proprietary. Use `Inter` (Bold/Regular/Light) as the closest open-source substitute — both geometric-humanist with comparable x-height.

## 4. Component Stylings

### Buttons

**Primary — Green Filled Pill**
- Background: `#63df4e` (ServiceNow Green)
- Text: `#032d42` (Deep Navy-Teal)
- Border: none or `2px solid #63df4e`
- Radius: `500px`
- Padding: `10px 20px`
- Used for primary conversion CTAs

**Secondary — White Outlined Pill**
- Background: transparent
- Text: `#ffffff`
- Border: `2px solid #ffffff`
- Radius: `500px`
- Padding: `10px 20px`
- Used for secondary actions on dark canvas

**Tertiary — Green Outlined Pill**
- Background: transparent
- Text: `#63df4e`
- Border: `2px solid #63df4e`
- Radius: `500px`
- Padding: `10px 20px`
- Used for accent-colored tertiary actions on dark

**Floating FAB Pills (persistent right-edge)**
- Background: `#63df4e` (ServiceNow Green)
- Text: `#032d42` (Deep Navy-Teal)
- Radius: `500px`
- Icon + label horizontal layout
- Fixed-position right edge, stacked vertically
- Shadow: `0 2px 12px rgba(0, 0, 0, 0.3)` (deeper for dark mode)

### Cards & Containers

**Hero Carousel Card**
- Background: `#063e5a` (Elevated) or gradient from Surface to Card
- Border: `1px solid rgba(255, 255, 255, 0.1)`
- Radius: `16px`
- Full-bleed photography fill

**Content Feature Card**
- Background: `#042f45` (Card)
- Border: `1px solid rgba(255, 255, 255, 0.1)`
- Radius: `24px`
- Padding: 28px
- No shadow

**Gradient-Border Featured Card**
- Background: `#042f45` (Card)
- Border: `2px solid` aurora-gradient (`linear-gradient(135deg, rgba(82,184,255,0.7), rgba(99,223,78,0.6), rgba(112,87,199,0.6))`)
- Radius: `24px`
- Used for special featured content ("Gartner Magic Quadrant" type cards)

**Dark Pill Badge**
- Background: `#0a0a0a` (near-black on dark — even darker than canvas for contrast)
- Text: `#63df4e` (ServiceNow Green)
- Border: `1px solid #63df4e`
- Radius: `500px`
- Font: 12–14px Mono

### Inputs & Forms

**Text Input (extrapolated)**
- Background: `#032d42` (Surface)
- Text: `#ffffff`
- Border: `1px solid rgba(255, 255, 255, 0.1)`
- Radius: `24px` (matching card-radius)
- Padding: `12px 20px`
- Focus: `border-color: #63df4e` + `box-shadow: 0 0 0 3px rgba(99, 223, 78, 0.25)`

### Navigation

**Primary Nav**
- Background: `#032d42` (Surface — brand primary as nav)
- Border bottom: `1px solid rgba(255, 255, 255, 0.1)`
- Logo: "servicenow." wordmark in white with green accent dot
- Nav links in white
- Right cluster: search, globe, "Sign In", Green Filled "Get Started" pill

**Announcement Banner**
- Aurora gradient preserved (unchanged from light mode)
- Text: `#032d42` (Navy-Teal) for contrast on pale gradient
- Outlined pill in navy

**Sub-Navigation Bar** — appears in 3 variants across the site:

*Platform Family variant* (on `/platform/*` and product capability pages):
- Background: `#032d42` matching primary nav
- Family label in white ServiceNowSansBold 28–32px (e.g., "AI Platform Capabilities")
- 5 tab links: ServiceNow AI Platform / AI Control Tower / AI Agents / AI Experience / Autonomous Workforce
- Active: solid white + 3px green underline (`#63df4e`); inactive: 70% white opacity

*Product Page variant* (on standalone product pages):
- 4 tabs: Benefits / Features / How To Buy / Related Apps
- Green-outlined "Contact Sales" pill on right edge
- `#benefits` URL hash auto-scrolls and marks tab active

*Industry Page variant*:
- Tabs: Customer Stories / Featured Resources / FAQ + Contact Sales pill

### 3-Column Benefit Grid (Light-Island Content Component)

A repeating component on product pages (e.g., "Benefits of Admin Center"):
- Background: `#ffffff` — preserved as a **light island** within the dark-mode canvas, since this grid exists to break the dark rhythm and present dense textual content
- 3 columns on desktop, stacking to 1 column on mobile
- Each column: ServiceNowSansBold 20–22px heading in `#032d42`, ServiceNowSansLight 15–16px body in `#1d1d1d`
- Section heading centered above grid: ServiceNowSansBold 38–48px in `#032d42`
- No borders, no shadows — columns float freely on white canvas with whitespace separation
- Flanked above and below by dark Surface tier sections to mark it as an intentional light island

### Image Treatment

- Portrait / lifestyle photography — warm natural lighting against dark canvas
- Full-bleed hero carousel with dot pagination
- 16px rounded corners on photography
- Partner logos in monochrome white on dark navy

## 5. Layout Principles

### Spacing System

- **Base unit**: 8px
- **Scale**: 1, 4, 5.5, 8, 10, 12.5, 15, 16, 18, 20, 24, 24.5, 32, 40, 42px
- Section vertical padding: 40–96px
- Card internal padding: 16–24px

### Grid & Container

- Bootstrap grid foundation
- Max widths: 1200–1680px depending on viewport
- Hero carousel: 3-up portrait layout on desktop
- Product grids: 3-column desktop, 2-column tablet, 1-column mobile

### Whitespace Philosophy

Executive breathing room — headlines float with generous space. Dark canvas reads as architectural negative space.

### Border Radius Scale

| Context | Radius | Usage |
|---------|--------|-------|
| Image / Media | 16px | Hero carousel, photography, toggle |
| Card / Panel | 24px | Feature cards, content containers, form inputs |
| Button / Pill | 500px | All buttons, FABs, badges, chips |

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No border, no shadow | Most content sections |
| Hairline | `1px solid rgba(255,255,255,0.1)` | Cards, inputs, utility borders |
| Strong Border | `1px solid rgba(255,255,255,0.18)` | Interactive/emphasized borders |
| Gradient-Border | `2px solid` aurora gradient | Featured content cards |
| Brightness Step | `#021a26` < `#032d42` < `#042f45` < `#063e5a` | Surface elevation through color |

Shadow-free system except for floating FABs (`0 2px 12px rgba(0, 0, 0, 0.3)`). Elevation comes from:
1. **Brightness-step surface ladder**
2. **Aurora particle starfield** on platform pages
3. **Gradient-border treatments** on featured cards
4. **Photography** (portraits, lifestyle imagery)

### Decorative Depth

- **Dotted particle starfield** on dark platform pages — aurora-inspired atmospheric depth, preserved unchanged
- **Aurora gradient announcement banner** unchanged
- **Gradient-border featured cards** — 2px aurora gradient around dark card borders

## 7. Do's and Don'ts

### Do
- Use Abyssal Navy-Teal (`#021a26`) as canvas — deeper than brand primary, preserving the blue-green undertone
- Use brand primary `#032d42` as a surface tier, not as the canvas
- Keep ServiceNow Green (`#63df4e`) unchanged — it's the brand signature
- Preserve the aurora gradient banner unchanged
- Use ServiceNowSansBold (or Inter 700) for all display sizes with negative letter-spacing
- Keep all buttons as full pills (`500px` radius)
- Use the radius system: 16px media, 24px cards, 500px pills — no intermediate values
- Apply translucent white borders (`rgba(255,255,255,0.1)` and `0.18`) — they adapt to any surface shade
- Body text at 78% warm-white opacity — never full white on dark
- Preserve floating green FAB pills and sub-nav green-underline patterns
- Keep the dotted particle starfield on platform pages

### Don't
- Don't use pure black (`#000000`) as canvas — the Abyssal Navy-Teal tint is specific
- Don't change ServiceNow Green for dark mode — preserved exactly
- Don't use rounded-rectangle buttons (8/12/16/24px radius) — pill-only
- Don't use box-shadows except on floating FABs — elevation through surface contrast
- Don't use heavy font weights (800+) — ceiling is 700
- Don't use ServiceNow Green as body text — always navy text on green pills
- Don't introduce alternate accent colors beyond the extracted aurora vocabulary
- Don't dim the aurora gradient banner for dark mode — it's designed to work on dark

## 8. Responsive Behavior

### Breakpoints

| Name | Width | Key Changes |
|------|-------|-------------|
| Micro | < 350px | Minimal layout, hamburger only |
| Mobile | 350–600px | Single column, hero scales down |
| Mobile Large | 600–767px | Single column, announcement wraps |
| Tablet | 768–991px | 2-column grids, sub-nav condenses |
| Desktop Small | 992–1199px | 3-column grids, full nav |
| Desktop | 1200–1499px | Default layout |
| Desktop Large | 1500–1849px | Wider container |
| Ultra-wide | > 1850px | Max container capped |

26-breakpoint system preserved from light mode.

### Touch Targets

- Minimum 44x44px on interactive elements
- Pill buttons naturally meet this through `10px 20px` padding
- Floating FABs sized for thumb tapping

### Collapsing Strategy

- Nav collapses to hamburger below ~991px
- Sub-nav becomes horizontal-scroll tabs or dropdown
- Product grid: 3 → 2 → 1 column
- Hero carousel: 3-up → 1-up with swipe
- Floating FABs reposition to bottom-right on mobile

### Image Behavior

- Portraits maintain aspect ratio
- Lifestyle photography uses responsive crops
- Partner logos horizontal scroll if needed

## 9. Agent Prompt Guide

### Quick Color Reference

- Canvas: Abyssal Navy-Teal (`#021a26`)
- Surface: Deep Navy-Teal (`#032d42`)
- Card: (`#042f45`)
- Elevated: (`#063e5a`)
- Primary CTA / Accent: ServiceNow Green (`#63df4e`)
- Heading Text: White (`#ffffff`)
- Body Text: `rgba(255,255,255,0.78)`
- Border Standard: `rgba(255,255,255,0.1)`
- Aurora Gradient Stops: `#b4ea9f → #7fd8ce → #52b8ff → #9c87df`

### Example Component Prompts

- "Create a dark hero on Abyssal Navy-Teal (#021a26) canvas with a dotted particle starfield background (small green #63df4e and aurora blue #52b8ff dots scattered across). Display headline at 64px ServiceNowSansBold (or Inter Bold) weight 700, 1.10 line-height, -0.64px letter-spacing. Apply the 'Put X to work for [Y]' formula — green keyword in #63df4e, trailing phrase in white. 18px body at 78% white opacity. Two buttons: Green Filled pill + White Outlined pill."
- "Design a primary pill button: #63df4e (ServiceNow Green) background, #032d42 (Navy-Teal) text in ServiceNowSansBook 16px, 500px border-radius, 10px 20px padding, 2px same-color border."
- "Add a sub-navigation bar below the primary nav: #032d42 background matching the nav. Family label in ServiceNowSansBold 28px white on the left, horizontal tab links on the right. Active tab: solid white + 3px green (#63df4e) underline at the bottom."
- "Place persistent floating CTA pills anchored to the right edge: two green filled pills stacked vertically (Contact with icon, Demo with icon). #63df4e fill, #032d42 navy text, 500px radius, 0 2px 12px rgba(0,0,0,0.3) shadow."
- "Build a gradient-border featured card: 24px border-radius, #042f45 (Card) background, 2px border with a linear-gradient(135deg, rgba(82,184,255,0.7), rgba(99,223,78,0.6), rgba(112,87,199,0.6)) aurora treatment. Inside: left half chart/illustration placeholder, right half headline in ServiceNowSansBold white, body at 78% white, and a white-outlined pill CTA."
- "Preserve the aurora gradient announcement banner at page top: linear-gradient(90deg, #b4ea9f 0%, #7fd8ce 40%, #52b8ff 70%, #9c87df 100%). Dark navy text on the gradient, outlined navy pill button on right."

### Iteration Guide

When refining dark-themed screens generated with this design system:
1. Verify canvas is Abyssal Navy-Teal (`#021a26`) — not pure black
2. Check the brightness-step ladder: `#021a26` < `#032d42` < `#042f45` < `#063e5a`
3. Confirm ServiceNow Green (`#63df4e`) is preserved unchanged
4. Ensure body text uses `rgba(255,255,255,0.78)`, never full white
5. Check all buttons are full pills (`500px` radius) — no rounded-rectangles
6. Verify radius system: `16px` media, `24px` cards, `500px` pills
7. Confirm typography uses ServiceNowSansBold (or Inter 700) with negative letter-spacing
8. Ensure no box-shadows except floating FABs — elevation through surface brightness
9. Preserve aurora gradient banner and dotted particle starfield backgrounds unchanged
10. Check that "Put X to work for [Y]" hero formula uses green keyword / white trailing phrase

### Known Gaps

- The aurora banner gradient exact stops are approximated — treat the sequence as a close reconstruction
- Form field styling is extrapolated from the system radius + color vocabulary — direct input tokens were not in the documented surfaces
- Semantic colors (error, warning, success) are not part of the documented palette — likely reuse Brand Green for success, error/warning defined outside the brand surface
- The "Give Feedback" vertical right-edge pill color exact hex is not captured as a named token
- ServiceNow Sans is proprietary — Inter is the recommended open-source substitute
- Animation and transition timing values are not captured (static extraction only)
