# Acadia Theme Skill

A Claude Code **skill** that applies a consistent Acadia University–based visual theme to every
work deliverable — Word/`.docx`, PDF, HTML pages and dashboards, Power BI reports, slides, and charts.
Install it once and Claude automatically styles anything it produces to match the brand.

## Brand at a glance

- **Acadia Blue** `#004077` (primary) · **Acadia Red** `#C41424` (accent, used sparingly) · White
- Headings: **Avenir Next** (web fallbacks Montserrat / Lato) · Body: **Arial**
- All chart/plot colors: **Tableau Classic 10**
  `#4E79A7 #F28E2B #E15759 #76B7B2 #59A14F #EDC949 #AF7AA1 #FF9DA7 #9C755F #BAB0AC`

> Brand blue/red are for *identity* (headers, accents, one highlight). Classic 10 is for *data*.

## Repository structure

```
.
├─ skill/        The installable Claude Code skill (this is the product)
│  ├─ SKILL.md                  Triggers + how to apply per format
│  ├─ references/               design-tokens, documents, powerbi, charts, logos
│  └─ assets/                   theme.css, html-template.html, Power BI theme JSON, logos
└─ samples/      Example deliverables produced with the theme
   ├─ sample-report.html        Branded web report (open in a browser)
   ├─ sample-report.docx        Branded Word document
   ├─ sample-report.pdf         The Word report exported to PDF
   ├─ acadia-powerbi-theme.json Importable Power BI theme
   └─ assets/                   chart PNGs + logo
```

## Install the skill

Copy the `skill/` folder into your Claude Code skills directory as `theme` (or any name you like):

**Windows**
```powershell
Copy-Item -Recurse "skill" "$env:USERPROFILE\.claude\skills\theme"
```

**macOS / Linux**
```bash
cp -r skill ~/.claude/skills/theme
```

Then in Claude Code, ask for any deliverable ("make a one-page HTML status report", "draft this memo
as a Word doc") and the theme applies automatically. See [`skill/SKILL.md`](skill/SKILL.md) for details.

## Using the pieces directly (without the skill)

- **HTML:** link [`skill/assets/theme.css`](skill/assets/theme.css); start from `skill/assets/html-template.html`.
- **Power BI:** View ▸ Themes ▸ Browse for themes ▸ select `skill/assets/acadia-powerbi-theme.json`.
- **Charts:** copy the matplotlib / plotly / D3 snippets in [`skill/references/charts.md`](skill/references/charts.md).
- **Word/PDF:** follow [`skill/references/documents.md`](skill/references/documents.md).

## Trademark notice

The Acadia University name, shield, and wordmark are trademarks of **Acadia University** and are
included here for authorized institutional use. Colors and fonts follow the published
[Acadia brand guidelines](https://www2.acadiau.ca/about-acadia/acadia-brand.html). Do not use the
logos or brand outside of authorized Acadia contexts. The skill code/structure may be reused; the
brand assets may not.
