---
name: theme
description: Apply the Acadia-based house visual theme to ANY work deliverable — Word/.docx, PDF, HTML pages and dashboards, Power BI reports, and slides. Use whenever creating, styling, or branding a document, report, web page, chart, or presentation, or when asked to "make it on-brand", "apply our theme", "use our colors/fonts", or "style this". Defines the official colors (Acadia Blue #004077, Acadia Red #C41424), fonts (Avenir Next / Arial / web fallbacks), the Tableau Classic 10 chart palette, and per-format styling rules.
---

# House Theme (Acadia-based)

This skill is the single source of truth for how all work deliverables should look. Apply it automatically whenever producing a document, HTML file, Power BI report, chart, or slide deck — unless the user explicitly asks for something else.

## Core identity (memorize these)

| Token | Value | Use |
|-------|-------|-----|
| **Acadia Blue** | `#004077` | Primary — headings, headers, key accents, links |
| **Acadia Red** | `#C41424` | Secondary accent — emphasis, callouts, primary chart series start, CTAs |
| **White** | `#FFFFFF` | Backgrounds, reversed text on dark |
| **Heading font** | Avenir Next → Montserrat → Lato → Arial | Titles & headings |
| **Body font** | Arial → Helvetica → Lato → sans-serif | Body text (day-to-day docs) |

**Chart / plot palette — always use Tableau Classic 10, in this order:**
`#4E79A7, #F28E2B, #E15759, #76B7B2, #59A14F, #EDC949, #AF7AA1, #FF9DA7, #9C755F, #BAB0AC`

> Brand colors (blue/red) are for *identity* chrome (headers, accents, KPI highlights).
> Classic 10 is for *data* (chart series, categories). Don't color data with the brand red/blue except for a single deliberate highlight series.

## How to apply, by format

- **HTML / dashboards / web reports** → link or inline [`assets/theme.css`](assets/theme.css). It defines every token as a CSS variable. Start from [`assets/html-template.html`](assets/html-template.html). Load Google Fonts Montserrat + Lato as web-safe stand-ins for Avenir Next.
- **Power BI** → import [`assets/acadia-powerbi-theme.json`](assets/acadia-powerbi-theme.json) (View ▸ Themes ▸ Browse for themes). It sets Classic 10 data colors plus brand structural colors. See [`references/powerbi.md`](references/powerbi.md) for layout conventions.
- **Word / .docx & PDF** → follow [`references/documents.md`](references/documents.md): Acadia Blue headings in Avenir Next (fall back to Arial), Arial body, red reserved for emphasis. When generating .docx use the `docx` skill; for PDF use the `pdf` skill — apply these colors/fonts to them.
- **Slides / .pptx** → blue title bars, white body, Classic 10 for chart series. Use the `pptx` skill with these tokens.
- **Charts (matplotlib/plotly/etc.)** → set the categorical color cycle to Classic 10. Snippets in [`references/charts.md`](references/charts.md).

## Logos

Files in [`assets/logo/`](assets/logo/): `acadia-vertical.png` (stacked) and `acadia-horizontal.png` (side-by-side). Optional white/reversed versions for dark backgrounds. Placement and usage rules in [`references/logos.md`](references/logos.md). On Acadia Blue bands, use a white logo if present, else place the color logo on a white chip.

## Full token reference

All exact values, the neutral gray scale, spacing, and type scale live in [`references/design-tokens.md`](references/design-tokens.md). Read it when you need a value not listed above.

## Rules of thumb

1. One accent at a time — blue is the workhorse; red is a spotlight, used sparingly.
2. Plenty of whitespace; left-aligned headings; generous line height (1.5 body).
3. Data viz uses Classic 10 in the given order, never reordered for aesthetics.
4. Never stretch/recolor a logo; keep clear space around it.
5. When in doubt, prefer the conservative "day-to-day" look: Arial body, blue headings, white background.
