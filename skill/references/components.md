# ServiceNow Component Prompts & Verification

## Ready-to-Use Component Prompts

**Dark hero section:**
> "Create a hero on `#032d42` background. ServiceNowSansBold 64px, weight 700, -0.64px letter-spacing, 1.10 line-height. Apply 'Put [X] to work for [Y]' — keyword in `#63df4e`, trailing phrase in white. 16px body at 1.50 line-height. Two CTAs: green filled pill + white outlined pill."

**Primary CTA pill:**
> "Green (`#63df4e`) background, navy (`#032d42`) text, ServiceNowSansBook 16px, `500px` radius, `10px 20px` padding."

**Secondary pill (on dark):**
> "Transparent background, white text, `2px solid #ffffff` border, `500px` radius, `10px 20px` padding."

**Sub-nav bar:**
> "`#032d42` background. Family label ServiceNowSansBold 28–32px left. Horizontal tabs right. Active tab: white text + 3px `#63df4e` underline. Inactive: 70% white opacity."

**Floating FAB pills:**
> "Fixed right edge, two stacked green pills (`#63df4e` fill, `#032d42` text, `500px` radius). 'Contact' + chat icon, 'Demo' + monitor icon. Shadow: `0 2px 12px rgba(0,0,0,0.3)` (dark mode only)."

**Feature card (light):**
> "Background `#ffffff`, `1px solid #848484` border, `24px` radius."

**Feature card (dark):**
> "Background `#042f45`, `1px solid rgba(255,255,255,0.10)` border, `24px` radius, padding 28px."

**Gradient-border featured card:**
> "`24px` radius, `#042f45` background, `2px solid linear-gradient(135deg, rgba(82,184,255,0.7), rgba(99,223,78,0.6), rgba(112,87,199,0.6))` border."

**3-column benefit grid:**
> "White canvas `#ffffff`. Center heading ServiceNowSansBold 38–48px in `#032d42`. Three columns, each with bold 20–22px heading + 15–16px body in `#1d1d1d`. No borders, no shadows — whitespace separation only. Stack to 1 column on mobile."

**Dotted particle background:**
> "Scatter ~2–4px dots in `#63df4e` and `#52b8ff` across the dark canvas for aurora/starfield effect."

**Dark pill badge:**
> "Background `#1d1d1d`, text `#63df4e`, `1px solid #63df4e` border, `500px` radius, 12–14px mono."

**Aurora announcement banner:**
> "`linear-gradient(90deg, #b4ea9f 0%, #7fd8ce 40%, #52b8ff 70%, #9c87df 100%)` full-width strip at page top. Text `#032d42`, outlined navy pill on right."

---

## Iteration Checklist

Before finalizing any ServiceNow-styled artifact:

- [ ] Canvas is `#032d42` (light) or `#021a26` (dark) — not pure black or generic navy
- [ ] Dark mode brightness ladder: `#021a26 → #032d42 → #042f45 → #063e5a`
- [ ] ServiceNow Green (`#63df4e`) on CTAs, hero keyword, active-tab — not as body text
- [ ] All buttons are `500px` radius pills — no rounded-rectangles
- [ ] Radius system: `16px` media, `24px` cards, `500px` pills — no other values
- [ ] Typography: Bold/Inter 700 for display with negative letter-spacing applied
- [ ] Dark mode body text is `rgba(255,255,255,0.78)` — not full white
- [ ] No box-shadows (except floating FABs)
- [ ] Aurora gradient on announcement banner only — not repeated elsewhere
- [ ] "Put X to work for Y" hero formula: green keyword, white trailing phrase
- [ ] Floating FAB pills (Contact, Demo) present on product pages
- [ ] Sub-nav bar with green underline on active tab for product family pages

---

## Known Gaps

- Aurora banner gradient stops are approximated reconstructions, not extracted exact values
- Form field styling not extracted (gated behind trial flows)
- Semantic colors (error/warning) not documented — Brand Green for success; error outside brand surface
- "Give Feedback" vertical right-edge pill hex not captured as a named token
- ServiceNowSans is proprietary — Inter is the substitute
- Animation/transition timing not captured (static extraction only)
