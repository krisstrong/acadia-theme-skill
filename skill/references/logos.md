# Logos

Logo files live in [`../assets/logo/`](../assets/logo/). Expected filenames (referenced by templates and conventions):

| File | Description | Use |
|------|-------------|-----|
| `acadia-vertical.png` | Shield stacked above "ACADIA UNIVERSITY" wordmark | Cover pages, square/portrait spaces, centered headers |
| `acadia-horizontal.png` | Shield left of the "ACADIA UNIVERSITY" wordmark | Document/web headers, footers, wide bands |
| `acadia-vertical-white.png` | *(optional)* all-white reversed vertical | On Acadia Blue / dark backgrounds |
| `acadia-horizontal-white.png` | *(optional)* all-white reversed horizontal | On Acadia Blue / dark header bands |

## Placement rules
- **Clear space:** keep margin ≥ the height of the wordmark "A" on every side.
- **Never** stretch, skew, recolor, add shadows, or place on a busy background.
- **Minimum size:** keep "ACADIA UNIVERSITY" legible — roughly ≥ 28px tall (horizontal) on screen, ≥ 0.4" in print.

## Color vs. white versions
- The full-color logo (blue/red shield, blue wordmark) only reads on **white or very light** backgrounds.
- On an **Acadia Blue header band**, the color wordmark disappears. Two options:
  1. Use a **reversed/white** logo (`*-white.png`) if available, or
  2. Place the color logo inside a **white chip/area** within the blue band.
- The HTML template and document conventions default to option 2 (white area) until white logo files are added.

## Web favicon / app icon
Crop the shield (no wordmark) from `acadia-vertical.png` for favicons and small app icons.
