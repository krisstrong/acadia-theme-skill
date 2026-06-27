# Power BI conventions

## Importing the theme
1. Power BI Desktop → **View** ribbon → **Themes** → **Browse for themes**.
2. Select [`../assets/acadia-powerbi-theme.json`](../assets/acadia-powerbi-theme.json).
3. All new visuals inherit Classic 10 data colors + Acadia structural colors.

The theme sets: data colors (Classic 10), table/matrix headers in Acadia Blue with white text, KPI cards in Acadia Blue, good/neutral/bad = green/yellow/red, diverging/sequential ramps anchored on Acadia Blue, hyperlinks Acadia Blue.

## Report layout conventions
- **Page background:** White; canvas outspace (wallpaper) Gray 100 `#F5F6F8`.
- **Header band:** rectangle in Acadia Blue `#004077` across the top with white report title (Segoe UI Semibold) and the white logo. Segoe UI is the safe Power BI substitute for Avenir Next/Arial.
- **KPI cards:** top row, Acadia Blue value, Gray 500 category label; optional 4px blue top accent shape.
- **Slicers:** left rail; header in Acadia Blue.
- **Accent:** a thin Acadia Red `#C41424` rule under the header, or for a single highlighted measure. Don't flood the page with red.
- **Spacing:** align visuals to an 8px grid; consistent gutters.

## Data color rules
- Categorical series → Classic 10 in order (theme handles this automatically).
- Single highlight (e.g., "this region vs. rest") → set the highlighted point to Acadia Red `#C41424`, others to Gray 300 `#D7DAE0`.
- Conditional formatting scales → min `#E6EDF3` → max `#004077`.
- KPI status → good `#59A14F`, warning `#EDC949`, bad `#E15759`.

## Fonts in Power BI
Power BI cannot embed Avenir Next reliably. Use **Segoe UI Semibold** for titles/headers and **Arial** (or Segoe UI) for labels — both ship on Windows and read as on-brand.
