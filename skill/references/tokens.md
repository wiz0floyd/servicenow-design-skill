# ServiceNow Design Tokens

## Light Mode Colors

| Token | Hex | Role |
|-------|-----|------|
| Canvas | `#032d42` | Hero, nav, footer, all dark surfaces |
| Green | `#63df4e` | CTA fills, hero keyword, active tab underline |
| CTA Text | `#032d42` | Text on green buttons (navy on green) |
| Heading (light surface) | `#1d1d1d` | Headings on white sections |
| Body (dark surface) | `#ffffff` | All text on navy canvas |
| Inline Link | `#00718f` | Links on white surfaces |
| Link Hover | `#024f69` | Darker link hover |
| Visited | `#7057c7` | Visited link state |
| Divider | `#848484` | Hairline borders |
| White surface | `#ffffff` | Content-dense sections, benefit grids |
| Job Card Hover | `#e0f7dc` | Careers page card hover |

## Dark Mode Colors (Green is identical)

| Token | Hex | Role |
|-------|-----|------|
| Canvas | `#021a26` | Primary dark canvas (deeper than light-mode navy) |
| Surface | `#032d42` | Section surfaces (brand primary becomes a tier) |
| Card | `#042f45` | Card containers |
| Elevated | `#063e5a` | Modals, elevated panels |
| Heading | `#ffffff` | All headings |
| Body text | `rgba(255,255,255,0.78)` | Body copy — never full white |
| Tertiary text | `rgba(255,255,255,0.5)` | Captions, metadata, eyebrows |
| Muted text | `rgba(255,255,255,0.3)` | Disabled, placeholders |
| Border standard | `rgba(255,255,255,0.10)` | Card hairlines |
| Border strong | `rgba(255,255,255,0.18)` | Interactive borders |

**Aurora Gradient** (announcement banner only):
`linear-gradient(90deg, #b4ea9f 0%, #7fd8ce 40%, #52b8ff 70%, #9c87df 100%)`

**Gradient-border** (featured cards, dark mode):
`linear-gradient(135deg, rgba(82,184,255,0.7), rgba(99,223,78,0.6), rgba(112,87,199,0.6))`

**Particle dots**: ~2–4px, colors `#63df4e` + `#52b8ff` scattered on dark canvas.

---

## Typography

| Role | Size | Weight | Line Height | Letter Spacing |
|------|------|--------|-------------|----------------|
| Display Hero | 64px | 700 | 1.10 | -0.64px |
| Display Large | 48px | 700 | 1.10 | -0.48px |
| Heading Medium | 28px | 700 | 1.10 | -0.28px |
| Heading Small | 18px | 700 | 1.10 | normal |
| Body | 16px | 400 | 1.50 | normal |
| Body Small | 14px | 500 | 1.43 | normal |
| Button Default | 16px | 400 | 1.50 | normal |
| Button Small | 14px | 450 | **1.79** | normal |
| Caption Uppercase | 14px | 400 | 1.50 | uppercase |

**Font**: ServiceNowSans (proprietary). Open-source substitute: **Inter** — 700 = Bold, 400 = Light, 500 = Book.

Key quirk: compact button `line-height: 1.79` — intentionally relaxed for airy pill feel.

---

## Hero Formula

```
"Put [keyword] to work for [audience]"
```
- `[keyword]` (e.g., "AI") → ServiceNow Green `#63df4e`
- `"to work for [audience]"` → white

This formula repeats on every product and industry page. Apply it when building hero sections.
