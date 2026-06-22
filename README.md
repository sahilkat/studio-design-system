# Studio Design System

A refined, client-presentable design system covering colour, typography, spacing, components, and data visualisation. Built as a single self-contained HTML file that serves as a living style guide — and as a visual reference for AI coding tools.

## What's inside

**Foundations**
- Colour system — Warm Stone (primary), Sage (secondary), neutrals, and semantic palettes
- Typography — Cormorant Garamond for headings, DM Sans for body
- Spacing — base-4 scale from 4px to 96px

**Components**
- Buttons (5 variants, 3 sizes, disabled/loading states)
- Form elements (input, select, textarea, checkbox, radio, toggle)
- Badges & tags (filled and outline variants)
- Cards (default, elevated, tinted)
- Alerts (info, success, warning, error)
- Tables
- Navigation / header

**Data visualisation**
- KPI cards with sparklines
- Bar / column charts
- Line & area charts
- Donut charts
- Six-colour series palette aligned to the design tokens

## Using in a project

### Option 1 — Copy the folder

Copy this repo into your project directory:

```bash
cp -r studio-design-system ./design-system
```

Claude Code will automatically read `CLAUDE.md` from the subfolder. For Cursor, copy the contents of `.cursorrules` into your project root `.cursorrules` and update the path to `./design-system/design-system.html`.

### Option 2 — Git submodule

```bash
git submodule add https://github.com/sahilkat/studio-design-system.git design-system
```

Pull updates across all projects later with:

```bash
git submodule update --remote
```

### Option 3 — Raw URL (Claude Code only)

Claude Code can fetch the file directly. Add this to your project's `CLAUDE.md`:

```
Before writing any UI code, fetch and read the design system:
https://raw.githubusercontent.com/sahilkat/studio-design-system/main/design-system.html
```

## AI tool integration

| File | Tool |
|---|---|
| `CLAUDE.md` | Claude Code — auto-loaded from any subdirectory |
| `.cursorrules` | Cursor, Windsurf — must be at project root |

Both files instruct the AI to read `design-system.html` before writing any UI code, and document the non-negotiable rules (colour tokens, typefaces, spacing scale, component classes, chart palette).

For other tools, point them to the HTML file manually:

| Tool | File |
|---|---|
| GitHub Copilot | `.github/copilot-instructions.md` |
| Codex / OpenAI Agents | `AGENTS.md` |

## Viewing the design system

Open `design-system.html` in any browser — no build step, no dependencies (Chart.js loads from CDN).
