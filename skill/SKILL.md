---
name: servicenow-design
description: Apply the ServiceNow design system when building any artifact that should look like, be inspired by, or be presented to a ServiceNow audience — HTML prototypes, mockups, components, landing pages, slide designs, dashboards, or any visual output. Use this skill whenever the user mentions ServiceNow design, brand, UI, mockup, artifact, or asks to "make it look like ServiceNow." Covers light mode (navy-teal canvas) and dark mode (abyssal navy-teal canvas). Trigger even for single components — the system is specific enough that guessing produces wrong results. Always load this skill before writing any HTML, CSS, or design spec with a ServiceNow context.
---

# ServiceNow Design System

## 1. Choose Mode

- **Light mode** (default): dark navy-teal canvas `#032d42`. Use for most marketing/product pages.
- **Dark mode**: abyssal navy-teal canvas `#021a26`. Use when the user asks for dark, or context is a deep platform/technical page.

Read `references/tokens.md` for full color palettes, typography table, and hero formula before writing any values.

## 2. Apply Non-Negotiable Rules

These eight rules govern every artifact — internalize them before writing a single line:

1. **Navy is never pure black** — `#032d42` light / `#021a26` dark. The blue-green undertone is brand-specific.
2. **Green (`#63df4e`) is accent only** — CTAs, hero keyword, active-tab underline. Never body text. Always pair with navy text on green fills.
3. **All buttons are full pills** — `500px` border-radius. No rounded-rectangles at any size.
4. **Three radii only** — `16px` media/photos · `24px` cards/panels · `500px` pills. No other values.
5. **No box-shadows** — elevation through surface contrast only. Exception: floating FABs `0 2px 12px rgba(0,0,0,0.3)`.
6. **Aurora gradient on banner only** — announcement strip at page top, nowhere else.
7. **ServiceNowSans or Inter** — substitute Inter (700 = Bold, 400 = Light, 500 = Book). Negative letter-spacing on display sizes.
8. **Weight ceiling is 700** — Bold is the heaviest in the system.

## 3. Build the Artifact

Read `references/components.md` → Component Prompts for ready-to-use copy/paste prompts for hero sections, CTAs, sub-nav bars, FAB pills, cards, benefit grids, and particle backgrounds.

For detailed specs (full typography table with all sizes, dark-mode surface ladder, responsive breakpoints, image treatment, spacing system), read `references/design-light.md` or `references/design-dark.md`.

## 4. Verify

Read `references/components.md` → Iteration Checklist and run it against the output before delivering.

---

## References

| File | When to read |
|------|-------------|
| `references/tokens.md` | Step 1 — colors for both modes, typography table, hero formula |
| `references/components.md` | Step 3 — component prompts; Step 4 — iteration checklist |
| `references/design-light.md` | Deep-dive: full light-mode spec (430 lines) |
| `references/design-dark.md` | Deep-dive: full dark-mode spec (382 lines) |
