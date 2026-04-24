# Design System Inspired by ServiceNow

## 1. Visual Theme & Atmosphere

ServiceNow is the largest enterprise workflow platform company that most consumers have never heard of — $100B+ in market cap, selling the invisible infrastructure behind IT service desks, HR systems, and customer service operations at most Fortune 500 companies. The brand's contemporary design system reflects that confidence: a **deep navy-teal canvas** (`#032d42`) as the dominant surface, **ServiceNow Sans** (a proprietary custom typeface family in multiple weights), and a singular **"put AI to work" hero formula** that repeats across every product and industry page with the phrase literally restated — "Put AI to work for people," "Put AI Agents to work for you," "Put AI to work for banking." The word "Put AI to work" is always set in ServiceNow's **vivid brand green** (`#63df4e`) while the trailing "for [X]" is white, creating an instantly recognizable verbal-visual signature.

The color strategy is **aurora-inspired** — the CSS token system literally names colors `--northern-light-aurora-color-2` and associated variants, and on some pages a pale-green-to-cyan gradient runs across the top banner ("Three days can change everything. Join us at Knowledge 2026…") mimicking northern lights. The rest of the palette is disciplined: deep navy-teal as the primary dark surface, the vivid green as the accent, purple (`#7057c7`) reserved for visited link states, a pale green (`#e0f7dc`) for job card hover surfaces, and a small neutral scale. Content sections alternate between the dark navy canvas and white content surfaces, with **large pill buttons** (`500px` radius — fully rounded) as the only interactive shape, consistently rendered either filled green with navy text or outlined in white/navy.

The system's most distinguishing choices are the **persistent floating green CTA pills** (Contact, Demo) that follow the user down the right edge of every product page, and a **sub-navigation bar** that appears at the top of each product family ("AI Platform Capabilities" → ServiceNow AI Platform, AI Control Tower, AI Agents, AI Experience, Autonomous Workforce) with an active tab underlined in brand green. Decorative **dotted particle backgrounds** (small green and blue pinpoints scattered across dark sections) reinforce the aurora/starfield theme on platform pages. The design language reads as "enterprise confidence with just enough personality to feel contemporary" — corporate without being cold, energetic without being playful.

**Key Characteristics:**
- Deep Navy-Teal (`#032d42`) as the dominant primary dark surface — the brand's signature mood
- Vivid Brand Green (`#63df4e`) as the singular accent — used for CTA fills, keyword emphasis in hero headlines, active-state underlines, and logo mark
- Proprietary ServiceNow Sans typeface family (Bold, Light, Book, Regular, Mono Regular) across all surfaces
- "Put AI to work for [X]" repeating hero formula with green keyword / white trailing phrase treatment
- Full pill buttons (`500px` radius) as the only interactive shape — filled green or outlined white
- Persistent floating green CTA pills (Contact, Demo) anchored to right edge of product pages
- Sub-navigation bar with active-tab green underline on every product/platform family
- Aurora gradient system (`--northern-light-aurora-color-*` named tokens) + dotted particle decorative backgrounds
- 26-breakpoint responsive system (1850 → 98px) for global enterprise coverage
- Bootstrap grid foundation underneath the custom brand layer

**Color-block page rhythm:** Aurora gradient announcement banner → Dark navy-teal nav → Dark navy hero with green-accent keyword headline → Sub-nav bar (variants: 5-tab platform family, 4-tab product, 3-tab industry) → Dark navy content with card grids → White content section with 3-column benefit grid → Gray transitional surface → Dark navy CTA / footer.

## 2. Color Palette & Roles

**Source Pages:** `servicenow.com` (homepage), `servicenow.com/products/admin-center`, `servicenow.com/products/ai-agents`, `servicenow.com/platform/ai-experience`, `servicenow.com/platform/autonomous-workforce`, `servicenow.com/industries/banking`, `careers.servicenow.com/how-we-hire`.

### Primary

- **Deep Navy-Teal** (`#032d42`): The primary brand color — hero backgrounds, nav bar, footer, dominant dark surface across the entire site. Deep enough to read as "enterprise trust" while carrying a faint blue-green undertone that distinguishes it from generic corporate navy
- **ServiceNow Green** (`#63df4e`): The signature brand accent — used for primary filled CTAs, the green word in every "Put AI to work" headline, active-tab underlines, logo dot, and link keyword emphasis. A vivid but not neon saturated green
- **Deep Green Shadow** (`#2d8f40` derived from observation; the button text color on green CTAs is the navy `#032d42`, not the green itself — so green is always a background or text-color accent never a text body)

### Secondary & Accent

- **Aurora Bright Blue** (`#52b8ff`): Named as `--northern-light-aurora-color-2` in the CSS — used in the aurora announcement banner gradient (visible at the top of every page as a pale green-to-blue-to-purple wash) and as occasional decorative accent
- **Aurora Link Teal** (`#00718f`): Named as `--surface-link-color` — used for inline links on white surfaces on content pages
- **Aurora Hover Teal** (`#024f69`): The darker hover variant of the link color, available as `--surface-link-hover-color`
- **Visited Purple** (`#7057c7`): Named as `--surface-link-visited-color` — used for visited links, a muted mid-purple
- **Pale Job Green** (`#e0f7dc`): Named as `--surface-job-card-hover-bg` — used as a very pale green card surface on careers job-listing pages

### Surface & Background

- **Deep Navy-Teal Canvas** (`#032d42`): Primary dark canvas — hero, nav, footer, platform page backgrounds
- **White** (`#ffffff`): Primary light canvas for content-dense body sections and form surfaces
- **Neutral Surface**: a slightly off-white background appears in some content areas (observed but not extracted as a named token — treat as `#ffffff` unless a specific alternate is needed)

### Neutrals & Text

- **Heading Near-Black** (`#1d1d1d`): Primary heading text on light surfaces
- **Neutral Gray** (`#848484`): Border color on dividers and utility elements; secondary supporting text
- **White Text on Dark** (`#ffffff`): All text rendered on the Deep Navy-Teal canvas
- **Navy Text on Green** (`#032d42`): Button text color when the button fill is ServiceNow Green — a deliberate high-contrast choice that keeps the green from competing as a text color

### Semantic

No dedicated error/warning/success palette was extractable from these pages — ServiceNow's commerce/app surfaces (trial sign-up, deep product UI) where status states appear were not among the extracted pages. The existing Aurora Green and Aurora Teal can serve informational status roles.

### Gradient System

- **Aurora Announcement Banner** — a pale linear gradient running roughly pale-green → cyan → soft-purple across the page-top banner (`Three days can change everything. Join us at Knowledge 2026…`). Exact gradient stops not fully extractable — treat as `linear-gradient(90deg, #b4ea9f 0%, #7fd8ce 40%, #52b8ff 70%, #9c87df 100%)` approximate reconstruction
- **Dotted Particle Background** — scattered small dots (~2–4px) in green (`#63df4e`) and aurora blue (`#52b8ff`) on dark surfaces, giving the navy canvas a starfield/aurora-texture quality. Applied via background-image pattern on platform and product hero areas

## 3. Typography Rules

### Font Family

- **Display / Headings**: `ServiceNowSansBold` — proprietary, used for hero headlines at 64px, 48px, 28px, 18px with tight 1.10 line-height and negative letter-spacing (`-0.64px` at 64px)
- **Body / UI**: `ServiceNowSansLight` — the body-weight workhorse with an unusual 1.79 relaxed line-height specifically on button labels
- **Secondary Body**: `ServiceNowSansBook` — slightly heavier book weight for paragraphs
- **Body Regular**: `ServiceNowSansRegular` — standard body weight
- **Monospace**: `ServiceNowSansMonoRegular` — used for code-style captions in uppercase
- **Fallback chain**: `-apple-system, system-ui, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"` — the full system-stack fallback

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | ServiceNowSansBold | 64px (4rem) | 700 | 1.10 | -0.64px | Primary hero headline ("Put AI to work...") |
| Display Large | ServiceNowSansBold | 48px (3rem) | 700 | 1.10 | -0.48px | Secondary hero / section leads |
| Heading Medium | ServiceNowSansBold | 28px (1.75rem) | 700 | 1.10 | -0.28px | Subsection headings |
| Heading Small | ServiceNowSansBold | 18px (1.13rem) | 700 | 1.10 | normal | Card titles |
| Body Large Link | ServiceNowSansLight | 20px (1.25rem) | 400 | 1.50 | normal | Lead links, nav items |
| Body | ServiceNowSansLight | 16px (1rem) | 400 | 1.50 | normal | Primary body text |
| Body Small | ServiceNowSansLight | 14px (0.88rem) | 500 | 1.43 | normal | Secondary body, captions |
| Button Large | ServiceNowSansBold | 28px (1.75rem) | 700 | 1.10 | -0.28px | Oversized hero button text |
| Button Medium | ServiceNowSansBook | 18px (1.13rem) | 400 | 1.50 | normal | Standard button label |
| Button Default | ServiceNowSansBook | 16px (1rem) | 400 | 1.50 | normal | Default pill button label |
| Button Small | ServiceNowSansLight | 14px (0.88rem) | 450 | 1.79 | normal | Compact button — unusually relaxed line-height |
| Caption | ServiceNowSansLight | 14px (0.88rem) | 500 | 1.43 | normal | Small labels, metadata |
| Caption Uppercase | ServiceNowSansMonoRegular | 14px (0.88rem) | 400 | 1.50 | normal (uppercase) | Code-style uppercase micro-labels ("INTRODUCING") |
| Tight Caption | ServiceNowSansBook | 14px (0.88rem) | 400 | 1.00–1.07 (tight) | normal (uppercase) | Super-tight uppercase labels |

### Principles

The typographic system leans heavily on **ServiceNowSansBold for all display sizes** — there is no elegant serif companion, no italic accents, no contrast pair. Everything declarative is sans-bold. Weight separation comes from the explicit multi-weight family (Bold / Book / Light / Regular) rather than from a single variable font. Line-height on display sizes is aggressively tight (1.10) while body text relaxes to 1.50 and **buttons sit at an unusual 1.79** — that relaxed button line-height is a distinctive ServiceNow quirk that keeps pill buttons feeling airy even when labels wrap. Negative letter-spacing (-0.64 to -0.28px) applies to Bold display sizes and tightens them into confident block headlines.

### Note on Font Substitutes

ServiceNowSans is proprietary. For open-source substitution, pair `Inter` (Bold + Regular + Light) as the closest match — both are geometric-humanist sans-serifs with comparable x-height. Inter's `400` weight works as a stand-in for ServiceNowSansLight, `500` for Book, `700` for Bold. Expect slightly different metrics — Inter is marginally wider, so test display headlines for line-break changes. The full fallback chain already specified in the extracted CSS is the correct system fallback to use.

## 4. Component Stylings

### Buttons

**Primary — ServiceNow Green Pill**
- Background: `#63df4e` (ServiceNow Green)
- Text: `#032d42` (Deep Navy-Teal)
- Border: none (or 2px solid `#63df4e` for size parity)
- Radius: `500px` (full pill)
- Padding: `10px 20px`
- Font: ServiceNowSansBook 16px or 18px
- Used for primary conversion CTAs ("Get Started", "Explore Platform", "Bank Solutions")

**Secondary — White Outlined Pill (on dark)**
- Background: transparent
- Text: `#ffffff`
- Border: `2px solid #ffffff`
- Radius: `500px`
- Padding: `10px 20px`
- Used for secondary actions on the dark navy canvas ("Watch Video", "Register Now", "Get Gartner Report")

**Tertiary — Navy Outlined Pill (on light)**
- Background: transparent
- Text: `#1d1d1d` (Heading Near-Black)
- Border: `2px solid #1d1d1d`
- Radius: `500px`
- Padding: `10px 20px`
- Active state: background `#4f4f4f`, text `#ffffff`, border `2px solid #4f4f4f`
- Used for secondary outlined actions on white surfaces

**Contact Sales Pill (on light)**
- Same as Navy Outlined Pill but rendered with ServiceNow Green border
- `#63df4e` border on white background with navy text

**Floating FAB Pills (persistent right-edge callouts)**
- Background: `#63df4e` (ServiceNow Green)
- Text: `#032d42` (Deep Navy-Teal)
- Radius: `500px`
- Icon + label (chat icon + "Contact", monitor icon + "Demo")
- Positioned fixed to right edge, stacked vertically on product/platform pages

**Give Feedback Vertical Pill**
- Background: medium blue (approximately `#4A90C2`-ish teal from screenshot — not extracted as a named token)
- Text: `#ffffff`
- Vertical orientation — rendered 90° rotated along right edge
- Pill shape
- Observed on industry pages (Banking)

### Cards & Containers

**Hero Carousel Card**
- Background: full-bleed portrait or lifestyle photography
- Radius: `16px` (per extracted token for image containers)
- No shadow
- Overlay captions on top-left corner on some cards

**Product Feature Card**
- Background: `#ffffff`
- Border: `1px solid #848484` (Neutral Gray) — hairline
- Radius: `24px` (per extracted token for div/card containers)
- No shadow extracted — cards rely on border and background contrast

**Gradient-Border Feature Card** (observed on AI Agents page, "2025 Gartner Magic Quadrant")
- Background: deep navy with subtle blue-purple gradient sheen
- Radius: `24px`
- Contains illustration/chart on left half, headline + body + outlined pill button on right half
- No visible shadow

**Job Card (Careers)**
- Background: white default
- Hover surface tint: `#e0f7dc` (Pale Job Green) — named as `--surface-job-card-hover-bg` in CSS
- Radius: presumably `24px` matching other card tokens
- Contains role title, department, location, apply link

**Dark Floating Card** ("It's not too late for Knowledge 2026")
- Background: `#000000` or near-black overlay on photography
- Radius: `16px` for media, `24px` for the card container
- Contains lifestyle photograph on top, heading + body + close icon
- Positioned fixed to bottom-left on some pages as a floating promo

### Inputs & Forms

No form fields were captured on the pages extracted — ServiceNow uses tabbed/dropdown content patterns in hero sections rather than inline forms on these surfaces. Sign-up forms exist on gated content pages not crawled.

### Badges / Tags / Pills

**Dark Pill Badge** (observed in careers)
- Background: `#1d1d1d` (Heading Near-Black)
- Text: `#63df4e` (ServiceNow Green)
- Border: `1px solid #63df4e`
- Radius: `50%` (circular/pill depending on width)
- Padding: `1px 4px`
- Font: 14px
- Used as a count badge or status pill in careers UI

### Navigation

**Primary Nav**
- Background: `#032d42` (Deep Navy-Teal) — dark, persistent across pages
- Logo: "servicenow." wordmark in white with a single green accent dot after the period
- Links: "Products", "Industries", "Learning", "Support", "Partners", "Company" — all with dropdown carets
- Right cluster: search icon, globe/language switcher, "Sign In" text link, green pill "Get Started" CTA
- Scroll arrow (`>`) appears to reveal more nav items in narrower viewports

**Announcement Banner (above primary nav)**
- Background: aurora gradient (pale green → cyan → soft purple)
- Text: `#032d42` (Deep Navy-Teal) for readability on pale gradient
- Contains announcement copy + "Register Now" outlined pill
- Height: ~48px, full width

**Sub-Navigation Bar (product/platform families)** — appears in two distinct variants:

*Platform Family variant* (on `/platform/*` pages like `ai-experience`, `autonomous-workforce`, and product capability pages like `ai-agents`):
- Background: `#032d42` (Deep Navy-Teal) — matches primary nav
- Family label on left: "AI Platform Capabilities"
- 5 tab links: ServiceNow AI Platform / AI Control Tower / AI Agents / AI Experience / Autonomous Workforce
- Active tab: white text + green underline (2–3px, `#63df4e`)
- Inactive tabs: muted white text (~70% opacity)

*Product Page variant* (on standalone product pages like `admin-center`):
- Background: same `#032d42` or extends onto white content area
- 4 tab links: Benefits / Features / How To Buy / Related Apps
- Active tab has green underline; the `#benefits` URL hash auto-scrolls to that section and marks the tab active
- On white content areas, a green-outlined **"Contact Sales"** pill sits on the right edge of the sub-nav row

*Industry Page variant* (on `/industries/*` pages like `banking`):
- Tabs: Customer Stories / Featured Resources / FAQ
- Contact Sales pill on right

**Mobile**: standard responsive collapse to hamburger menu at lower breakpoints (26-breakpoint system)

### Image Treatment

- **Portrait / lifestyle photography** is the primary hero visual content — real people in real workspaces, warm natural lighting, often diverse groups
- **Full-bleed hero carousel** with dot pagination + pause/play control in lower-left
- **Photography cards** use `16px` rounding
- **Partner logos row**: monochrome-white logos on dark navy, displayed in a simple horizontal lineup ("BHN Blackhawk, Griffith University, Raleigh, Cancom...")

### 3-Column Benefit Grid (White-Canvas Content Component)

A repeating component observed on product pages (e.g., "Benefits of Admin Center"):
- Background: `#ffffff` (White canvas)
- Layout: 3 columns on desktop, stacking to 1 column on mobile
- Each column contains:
  - Short heading in ServiceNowSansBold at ~20–22px, color `#1d1d1d` (Heading Near-Black) or `#032d42` (Deep Navy-Teal)
  - Body paragraph in ServiceNowSansLight at 15–16px, 1.5 line-height, color `#1d1d1d` or slightly muted
- Section heading centered above the grid ("Benefits of [Product]") in ServiceNowSansBold at 38–48px in Deep Navy-Teal
- No borders, no shadows, no cards — columns float freely on white canvas separated only by whitespace
- Below this grid, the next section typically transitions to a gray surface (~`#f5f5f5`) or back to dark navy

### Page Sub-Nav Signature Component

A distinctive reusable component across product/platform/industry pages:
- Horizontal bar below the announcement banner and primary nav
- Dark navy background matching primary nav
- Family name on far left in ServiceNowSansBold
- Sibling page links as horizontal tabs
- Active tab with green underline
- Acts as a persistent way-finder for browsing within a product family

## 5. Layout Principles

### Spacing System

- **Base unit**: 8px
- **Scale**: 1px, 4px, 5.5px, 8px, 10px, 12.5px, 15px, 16px, 18px, 20px, 24px, 24.5px, 32px, 40px, 42px
- Fine-grained pixel-nudge values (5.5, 12.5, 24.5) indicate precise optical alignment adjustments
- Section vertical padding: 40–96px on desktop, scaling down at mobile breakpoints
- Card internal padding: 16–24px
- Pill button padding: `10px 20px`

### Grid & Container

- Bootstrap grid foundation (container + row + col framework detected in extraction)
- Max content widths span 1200–1680px depending on viewport
- Homepage hero carousel: 3-up horizontal portrait card layout on desktop
- Product grids: typically 3-column on desktop, 2-column tablet, 1-column mobile
- Announcement banner: full-width edge-to-edge

### Whitespace Philosophy

ServiceNow uses whitespace as **executive breathing room** — headlines float with generous space around them, and content density stays moderate even in product pages. The dark navy canvas reads as architectural negative space between content blocks.

### Border Radius Scale

| Context | Radius | Usage |
|---------|--------|-------|
| Image / Media Container | 16px | Hero carousel cards, photography containers, toggle nav |
| Card / Panel | 24px | Feature cards, content containers |
| Button / Pill | 500px | All buttons — full pill shape |

The radius system is deliberately **three-tier** with a significant jump between media (16px) and cards (24px), and an aggressive commitment to **full pill** (500px) for all interactive elements. No intermediate 4/6/8/12px values — the system reads as bold and contemporary.

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No shadow, no border | Most content sections |
| Hairline | `1px solid #848484` | Divider lines, utility borders |
| Gradient-Border | Subtle blue-purple gradient background on dark cards | Featured content (e.g., "2025 Gartner Magic Quadrant" card) |
| Decorative Particles | Scattered dots in green/blue on dark surfaces | Platform page backgrounds |

No box-shadow values were extracted. Depth in the system comes from:
1. **Surface alternation** (dark navy ↔ white content sections)
2. **Photography** (lifestyle hero imagery carries inherent depth)
3. **Particle background** on dark platform pages — aurora-inspired atmospheric depth
4. **Gradient-border treatments** on special featured cards

### Decorative Depth

- **Aurora announcement banner gradient** (pale green → cyan → soft purple)
- **Dotted particle starfield** on platform page dark backgrounds — aurora/northern-lights theme
- **Green accent underline** on active sub-nav tabs — single-pixel depth cue
- **Floating green FAB pills** create a z-index layer of persistent call-to-action

## 7. Do's and Don'ts

### Do
- Use Deep Navy-Teal (`#032d42`) as the primary dark surface — never pure black
- Reserve ServiceNow Green (`#63df4e`) for the singular accent — CTA fills, hero-keyword emphasis, active-tab underlines, logo dot
- Apply the "Put X to work for [Y]" hero formula with green keyword / white trailing phrase treatment
- Use ServiceNowSansBold (or Inter substitute) for all display sizes with -0.28 to -0.64px letter-spacing
- Keep all buttons as full pills (`500px` radius) — never introduce rounded-rectangle intermediate shapes
- Use `16px` radius for image containers, `24px` for cards, `500px` for pills — no intermediate values
- Apply the aurora gradient only to the page-top announcement banner — it's the single gradient in the system
- Use dotted particle backgrounds sparingly on dark platform pages for aurora/starfield atmosphere
- Include persistent floating green FAB pills (Contact, Demo) on product/platform pages
- Use the sub-nav bar pattern on product family pages with green active-tab underline

### Don't
- Don't use pure black or pure navy without the teal undertone — the `#032d42` shade is specific to ServiceNow
- Don't use ServiceNow Green as a text body color — it's always a background or accent, with navy text on green pills
- Don't introduce additional accent colors beyond the existing aurora/green/navy/purple-visited vocabulary
- Don't use rounded-rectangle buttons (8px, 12px, 16px, 24px, 32px radius) — the system is pill-only
- Don't use box-shadows — elevation through surface contrast and photography only
- Don't use the dotted particle background on content-dense pages — reserve for hero/platform surfaces
- Don't deviate from the serif-free type system — ServiceNowSans handles everything
- Don't use weights heavier than 700 — the system's Bold is the ceiling

## 8. Responsive Behavior

### Breakpoints

ServiceNow operates on a 26-breakpoint system from 1850px → 98px, far more granular than typical Bootstrap defaults — likely driven by global enterprise-content layout needs across many languages.

| Name | Width | Key Changes |
|------|-------|-------------|
| Micro | < 350px | Minimal layout, hamburger nav only |
| Mobile | 350–600px | Single column, hero headline scales down significantly, floating FABs may shift to bottom |
| Mobile Large | 600–767px | Single column, announcement banner wraps |
| Tablet | 768–991px | 2-column grids emerge, sub-nav bar may condense to dropdown |
| Desktop Small | 992–1199px | Full 3-column grids, full nav, sub-nav bar visible |
| Desktop | 1200–1499px | Default desktop layout |
| Desktop Large | 1500–1849px | Wider content container |
| Ultra-wide | > 1850px | Max container capped, generous side whitespace |

The 26-breakpoint granularity handles fine-grained edge cases (421/420, 1199/1200, 1700/1680) specific to ServiceNow's multi-tenant localized content system.

### Touch Targets

- Minimum 44x44px on interactive elements
- Pill buttons meet this through `10px 20px` padding + content
- Floating FAB pills sized for comfortable thumb tapping at mobile breakpoints
- Announcement banner pill and sub-nav tabs sized for touch

### Collapsing Strategy

- Primary nav collapses to hamburger menu below ~991px
- Sub-nav bar may transform to horizontal-scrolling tab row or dropdown below tablet
- Product feature grid: 3 → 2 → 1 column as viewport narrows
- Hero carousel: 3-up cards → 1-up cards on mobile with swipe
- Floating FABs may reposition to bottom-right corner on mobile
- Announcement banner text may wrap to two lines or shorten

### Image Behavior

- Hero carousel portraits maintain aspect ratio at all breakpoints
- Lifestyle photography in featured cards uses responsive crops
- Partner logo row stays horizontal even on mobile (horizontal scroll if needed)
- Dotted particle background scales to viewport

## 9. Agent Prompt Guide

### Quick Color Reference

- Canvas / Dark Surface: Deep Navy-Teal (`#032d42`)
- Primary CTA / Accent: ServiceNow Green (`#63df4e`)
- CTA Text (on green): Deep Navy-Teal (`#032d42`)
- Heading on Light: Near-Black (`#1d1d1d`)
- Body on Dark: White (`#ffffff`)
- Inline Link on Light: Aurora Link Teal (`#00718f`)
- Divider: Neutral Gray (`#848484`)
- Aurora Gradient Stops (approximation): pale-green → cyan → soft-purple

### Example Component Prompts

- "Create a primary CTA pill button with ServiceNow Green (#63df4e) background, Deep Navy-Teal (#032d42) text in ServiceNowSansBook (or Inter substitute), 500px border-radius, and 10px 20px padding."
- "Design a dark navy hero section: #032d42 background. Place a display headline in ServiceNowSansBold at 64px weight 700 with -0.64px letter-spacing and 1.10 line-height. Apply the 'Put X to work for [Y]' formula — color the first phrase (e.g., 'Put AI to work') in #63df4e (ServiceNow Green) and the trailing phrase ('for banking') in white. Follow with a 16–18px body paragraph in ServiceNowSansLight at 1.50 line-height and two CTAs: one green filled pill and one white outlined pill."
- "Add a sub-navigation bar: #032d42 background matching the primary nav. On the left, a family name in ServiceNowSansBold at 28–32px. On the right, horizontal tab links with active state marked by a 2–3px green (#63df4e) underline. No background fill on active — just underline and color shift."
- "Place a persistent floating CTA pill stack anchored to the right edge of the viewport: two green-filled pills stacked vertically ('Contact' with chat icon, 'Demo' with monitor icon). Green fill #63df4e, navy #032d42 text, 500px radius, small icon + label horizontal layout."
- "Design a gradient-border feature card: 24px border-radius, dark navy background (#032d42) with a subtle blue-purple gradient sheen. Inside: left half illustration/chart image (16px rounded), right half with a white ServiceNowSansBold heading, body text, and a white outlined pill CTA button."
- "Apply a decorative dotted particle background to a dark platform page: scatter small dots (~2–4px diameter) in #63df4e green and #52b8ff aurora blue across the #032d42 canvas for an aurora/starfield atmosphere."
- "Build a 3-column benefit grid on white canvas: center a section heading in ServiceNowSansBold at 38–48px in Deep Navy-Teal (#032d42), then three columns each with a ~20–22px bold column heading and a 15–16px body paragraph in ServiceNowSansLight. No borders, no shadows — just whitespace separation between columns. Stack to 1 column on mobile."

### Iteration Guide

When refining screens generated with this design system:
1. Verify the Deep Navy-Teal canvas is `#032d42` — not pure black or generic navy
2. Check that ServiceNow Green appears only in CTA fills, hero-keyword emphasis, active-tab underlines — never as large surfaces or text body
3. Confirm every button is a full pill (`500px` radius) — no rounded-rectangle variants
4. Verify the radius system: `16px` media, `24px` cards, `500px` pills — no intermediate values
5. Check typography: ServiceNowSansBold (or Inter 700) for display, ServiceNowSansLight (Inter 400) for body, negative letter-spacing on display sizes
6. Confirm "Put X to work for [Y]" hero formula with green keyword / white trailing phrase if the page is a product/industry page
7. Ensure no box-shadows — elevation through surface contrast only
8. Check that persistent floating FAB pills (Contact, Demo) are present on product pages
9. Verify sub-nav bar pattern with green underline on active tab for product family pages
10. Include the aurora gradient banner at page top only — it's the single gradient in the system

### Known Gaps

- The aurora announcement-banner gradient exact stops are approximated — treat the `#b4ea9f → #7fd8ce → #52b8ff → #9c87df` sequence as a close reconstruction rather than exact site values
- Form field styling (sign-up, contact forms) is not documented — those surfaces are gated behind trial flows and not represented in the extracted pages
- Semantic colors (error red, warning yellow, success green) are not part of the documented palette — the Brand Green likely serves success; error/warning conventions sit outside the brand surface
- The "Give Feedback" vertical right-edge pill color exact hex is not captured as a named token
- The exact gradient inside featured cards like the "Gartner Magic Quadrant" card is approximated, not a named token
- ServiceNowSans is proprietary — Inter is the recommended open-source substitute
- Animation and transition timing values are not captured (static extraction only)
