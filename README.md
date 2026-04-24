# servicenow-design

A Claude Code skill that applies ServiceNow's exact design system to any artifact — HTML prototypes, mockups, dashboards, slide designs, or components.

## What it does

- Loads the correct color tokens, typography, and component patterns into every Claude conversation
- Covers light mode (navy-teal canvas) and dark mode (abyssal canvas with 4-tier brightness ladder)
- Enforces non-obvious brand rules: pill-only buttons, three radii, no box-shadows, aurora gradient on banner only
- Runs a 12-point verification checklist before delivering any output

## Install

```bash
git clone https://github.com/wiz0floyd/servicenow-design-skill.git
cp -r servicenow-design-skill/skill ~/.claude/skills/servicenow-design
```

## Structure

```
skill/
├── SKILL.md                  # 44-line workflow — loads on every invocation
└── references/
    ├── tokens.md             # colors, typography, hero formula
    ├── components.md         # component prompts + iteration checklist
    ├── design-light.md       # full light-mode spec
    └── design-dark.md        # full dark-mode spec
```

## Credits

Design tokens sourced from [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md).
