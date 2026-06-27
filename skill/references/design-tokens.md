# Design Tokens — single source of truth

Every deliverable derives its colors, fonts, and spacing from this file. The CSS, Power BI theme, and document conventions are all generated from these values — keep them in sync.

## Brand colors

| Name | Hex | RGB | CMYK | Pantone |
|------|-----|-----|------|---------|
| Acadia Blue (primary) | `#004077` | 0, 64, 119 | 100, 60, 0, 40 | 294 C |
| Acadia Red (accent) | `#C41424` | 196, 20, 36 | 0, 100, 90, 20 | 186 C |
| White | `#FFFFFF` | 255, 255, 255 | 0, 0, 0, 0 | — |

### Derived brand tints/shades (for hovers, backgrounds, borders)
| Token | Hex | Use |
|-------|-----|-----|
| Blue dark | `#002F58` | hover/active on blue, dark headers |
| Blue 700 | `#004077` | base primary |
| Blue 200 | `#B3C6D6` | light blue fills, borders |
| Blue 50 | `#E6EDF3` | subtle blue background bands |
| Red dark | `#9E1019` | hover/active on red |
| Red 50 | `#FBE7E9` | red callout background |

## Neutral scale (grays)

| Token | Hex | Use |
|-------|-----|-----|
| Ink (body text) | `#1A1A1A` | default text |
| Gray 700 | `#3D3D3D` | strong secondary text |
| Gray 500 (muted) | `#6B6B6B` | captions, labels, axis text |
| Gray 300 (border) | `#D7DAE0` | borders, dividers, table rules |
| Gray 100 (surface alt) | `#F5F6F8` | zebra rows, page background bands, cards |
| White | `#FFFFFF` | base surface |

## Semantic / status colors

| Token | Hex | Use |
|-------|-----|-----|
| Success | `#59A14F` | positive deltas, on-track |
| Warning | `#EDC949` | caution (use dark text on it) |
| Error | `#E15759` | negative, off-track (distinct from brand red) |
| Info | `#4E79A7` | neutral informational |

> Status colors are pulled from Classic 10 so dashboards stay coherent. Brand `#C41424` is identity-only, not a status color.

## Chart palette — Tableau Classic 10 (categorical, fixed order)

```
#4E79A7  #F28E2B  #E15759  #76B7B2  #59A14F
#EDC949  #AF7AA1  #FF9DA7  #9C755F  #BAB0AC
```

- Use in order; do not reorder for aesthetics.
- For a single "highlight vs. rest" chart: highlight series = Acadia Red `#C41424`, all others = Gray 300 `#D7DAE0`.
- Sequential/heatmap ramp (when continuous): Blue 50 `#E6EDF3` → Acadia Blue `#004077`.

## Typography

| Role | Stack | Notes |
|------|-------|-------|
| Headings | `"Avenir Next", "Montserrat", "Lato", Arial, sans-serif` | Avenir Next is macOS marketing font; Montserrat/Lato are Google web fallbacks |
| Body | `Arial, "Helvetica Neue", Helvetica, "Lato", sans-serif` | Arial = official day-to-day font |
| Mono (code/data) | `"Cascadia Code", "Consolas", monospace` | tables of figures, code |

### Type scale (rem / pt)
| Level | Size | Weight | Line height |
|-------|------|--------|-------------|
| Display / cover title | 2.5rem (~32pt) | 700 | 1.15 |
| H1 | 2rem (~26pt) | 700 | 1.2 |
| H2 | 1.5rem (~20pt) | 600 | 1.25 |
| H3 | 1.25rem (~16pt) | 600 | 1.3 |
| Body | 1rem (~11pt) | 400 | 1.5 |
| Small / caption | 0.85rem (~9pt) | 400 | 1.4 |

Headings: Acadia Blue. Body: Ink. Links: Acadia Blue, underline on hover.

## Spacing scale (8px base)

`4, 8, 12, 16, 24, 32, 48, 64` px. Default paragraph spacing 16px; section gap 32–48px.

## Radius & elevation
| Token | Value |
|-------|-------|
| Radius small | 4px |
| Radius medium | 8px |
| Card shadow | `0 1px 3px rgba(0,0,0,.12)` |

## Logo usage
- Maintain clear space ≥ the height of the wordmark "A" on all sides.
- Never stretch, recolor, or add effects.
- Use full-color on white; reversed (white) logo on Acadia Blue.
- No sub-unit may create its own logo without brand consultation.
