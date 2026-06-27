# House Theme — Sample Files

These samples show the **`theme`** skill (Acadia-based house brand) applied across formats.
The theme itself lives at `C:\Users\kstro\.claude\skills\theme\` and is applied automatically
whenever you ask Claude to produce a work deliverable.

## What's here

| File | Format | Shows |
|------|--------|-------|
| `sample-report.html` | HTML / web | Blue header band + logo, KPI cards, red callout, Classic 10 bar chart, branded table, footer. Open in any browser. |
| `sample-report.docx` | Word | Logo, Acadia Blue headings (Avenir Next → Arial), red accent rule, blue table header, embedded charts. |
| `sample-report.pdf` | PDF | The Word report exported to PDF. |
| `acadia-powerbi-theme.json` | Power BI | Import via **View ▸ Themes ▸ Browse for themes**. Sets Classic 10 data colors + Acadia structural colors. |
| `assets/chart-bar.png` | Chart | matplotlib bar chart, Tableau Classic 10. |
| `assets/chart-trend.png` | Chart | matplotlib multi-series line chart, Classic 10 color cycle. |

## Brand at a glance
- **Acadia Blue** `#004077` (primary) · **Acadia Red** `#C41424` (accent, sparing) · White
- Headings: Avenir Next (web: Montserrat/Lato) · Body: Arial
- All chart/plot colors: **Tableau Classic 10**
  `#4E79A7 #F28E2B #E15759 #76B7B2 #59A14F #EDC949 #AF7AA1 #FF9DA7 #9C755F #BAB0AC`

## How these were made
- HTML: hand-built from `theme/assets/theme.css` tokens.
- Charts: Python + matplotlib with the Classic 10 rcParams (see `theme/references/charts.md`).
- Word: Python + python-docx applying the theme colors/fonts.
- PDF: Word document exported to PDF.

> Want a deck, a different report, or these styled with your real data? Just ask — the theme applies automatically.
