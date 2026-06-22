# Studio Design System

This directory contains the canonical design system for all client and product work.

## Visual Reference

Before writing any UI code, HTML, or CSS, read the design system file:

```
./design-system.html
```

Open it with the Read tool and study the rendered components, colour swatches, typography scale, and spacing values before producing any output.

## What the file contains

- **Colour system** — full primary (Warm Stone), secondary (Sage), neutral, and semantic palettes with exact hex values
- **Typography** — Cormorant Garamond for all headings/display; DM Sans for body, labels, and UI text
- **Spacing scale** — base-4 tokens from `space-1` (4px) to `space-24` (96px)
- **Components** — buttons (5 variants, 3 sizes), form inputs, checkboxes, radios, toggles, badges, cards, alerts, tables, navigation
- **Data visualisation** — KPI cards, bar charts, line/area charts, donut charts; colour palette for chart series

## Non-negotiable rules

1. **Never hardcode a colour.** Use the CSS custom properties defined in `:root` in the design system.
2. **Never use a system font or fallback font** as the primary typeface. Always load Cormorant Garamond and DM Sans from Google Fonts.
3. **Match border-radius exactly.** `--radius-sm` (2px), `--radius-md` (4px), `--radius-lg` (6px). No large rounded corners.
4. **Use the spacing tokens.** Never write arbitrary `padding: 13px` or `margin: 22px`. Map to the nearest token.
5. **Shadows are warm-toned.** Use `rgba(100, 80, 60, …)` tint — not grey or black shadows.
6. **Chart colours follow the palette.** Series 1 = #A38572, Series 2 = #6F9370, Series 3 = #6B8DB5, Series 4 = #C99A4E, Series 5 = #B87878.
7. **One primary action per view.** Use `.btn-primary` sparingly; default to `.btn-outline` or `.btn-ghost` for secondary actions.
8. **Tables are borderless-cell.** Use the `.ds-table` pattern: header background `neutral-50`, no cell borders except row separators.

## Tone

The aesthetic is a premium design consultancy — refined, airy, client-presentable. Avoid:
- Loud gradients
- Dark backgrounds (unless explicitly requested)
- Overly rounded corners (`border-radius > 8px`)
- Dense, information-heavy layouts without whitespace
- Any colour not in the defined palette
