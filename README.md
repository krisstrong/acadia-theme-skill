# Acadia Theme Skill

A Claude Code **skill** that applies a consistent Acadia University–based visual theme to every
work deliverable — Word/`.docx`, PDF, HTML pages and dashboards, Power BI reports, slides, and charts.
Install it once and Claude automatically styles anything it produces to match the brand.

## Quickstart

```bash
git clone https://github.com/krisstrong/acadia-theme-skill.git
cp -r acadia-theme-skill/skill ~/.claude/skills/theme      # Windows: see note below
```

Restart Claude Code, then ask for anything — *"make a one-page HTML status report"* — and the theme
applies automatically. Works in the terminal CLI, desktop app, and VS Code (they share `~/.claude`).

> **Windows (PowerShell):** `Copy-Item -Recurse -Force "acadia-theme-skill\skill" "$env:USERPROFILE\.claude\skills\theme"`
> Full options (per-project install, IDEs, updating) are in [Install the skill into Claude Code](#install-the-skill-into-claude-code).

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
   ├─ acadia-powerbi-theme.json Importable Power BI theme ("Acadia 2026")
   └─ assets/                   chart PNGs + logo
```

## Install the skill into Claude Code

A Claude Code "skill" is just a folder containing a `SKILL.md` placed in a `skills/` directory.
Claude discovers it automatically and applies it whenever a request matches its description — you
don't run a command to "load" it, you just put the folder in the right place.

### Where to put it

| Location | Path | Available in |
|----------|------|--------------|
| **Personal** (recommended) | `~/.claude/skills/theme/` | **Every** project on your machine |
| **Project** | `<your-project>/.claude/skills/theme/` | Only that one project (good for sharing via the project's repo) |

For an always-on house theme, use **Personal**.

### A. Install for all future projects (personal)

First get the files — either clone this repo or download it:

```bash
git clone https://github.com/krisstrong/acadia-theme-skill.git
cd acadia-theme-skill
```

Then copy the `skill/` folder into your personal skills directory, named `theme`:

**Windows (PowerShell)**
```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.claude\skills" | Out-Null
Copy-Item -Recurse -Force "skill" "$env:USERPROFILE\.claude\skills\theme"
```

**macOS / Linux**
```bash
mkdir -p ~/.claude/skills
cp -r skill ~/.claude/skills/theme
```

### B. Install for a single project

From inside that project's root:

```bash
mkdir -p .claude/skills
cp -r /path/to/acadia-theme-skill/skill .claude/skills/theme
```

Commit `.claude/skills/theme/` with the project and everyone on the team gets the theme.

### C. Activate and verify

1. **Start (or restart) Claude Code** in your project so it picks up the new skill folder.
2. Confirm it loaded — ask: **"What skills are available?"** or **"Use the theme skill to make a sample HTML page."**
3. From then on, just ask for any deliverable ("make a one-page HTML status report", "draft this memo
   as a Word doc", "build a Power BI theme") and the Acadia theme applies automatically. You can also
   nudge it explicitly: *"apply our theme / use our brand colors."*

### Using it across Claude Code surfaces (terminal, desktop app, VS Code)

Claude Code comes in several forms — the **terminal CLI**, the **desktop app** (macOS/Windows), the
**web app** (claude.ai/code), and **IDE extensions** (VS Code, JetBrains). The important thing:

> **They all read the same personal skills folder (`~/.claude/skills/`).** Install once with
> **Section A** and the theme is available in *every* surface — no per-app setup.

**Desktop app (macOS / Windows)**
1. Do the personal install in **Section A** above.
2. Open the desktop app and open/select your project folder (**Open Project** / recent projects).
3. **Quit and reopen the app** once after installing so it rescans skills.
4. Ask for any deliverable, or *"use the theme skill"* — verify with *"What skills are available?"*

**VS Code (and JetBrains)**
1. Install the **Claude Code** extension from the VS Code Marketplace (search "Claude Code"), or run
   `claude` once in the integrated terminal and accept its offer to install the extension. Sign in.
2. Personal skills from `~/.claude/skills/` load automatically — **Section A** is all you need for it
   to be available in every workspace.
3. To bundle the theme *with a specific project* instead, use **Section B** (`<project>/.claude/skills/theme/`);
   it loads whenever that folder is open in the editor, and travels with the repo for teammates.
4. After adding or changing a skill, **reload the window** (`Ctrl/Cmd+Shift+P` → *Developer: Reload Window*)
   or restart the Claude Code panel so it picks up the change.
5. Open the Claude Code panel and ask for a deliverable; confirm with *"What skills are available?"*

> One install, everywhere: because the CLI, desktop app, and IDE extensions share `~/.claude`,
> updating the skill once (next section) updates it for all of them.

### Updating the skill later

When this repo changes, refresh your installed copy:

```bash
cd acadia-theme-skill && git pull
# then re-run the copy command from section A (or B)
```

> **Tip (stay in sync automatically):** instead of copying, link the folder so edits in the repo apply everywhere.
> - macOS/Linux: `ln -s "$(pwd)/skill" ~/.claude/skills/theme`
> - Windows (admin PowerShell): `New-Item -ItemType SymbolicLink -Path "$env:USERPROFILE\.claude\skills\theme" -Target "$PWD\skill"`
>
> Symlinks can be finicky on OneDrive-synced folders — if it misbehaves, just use the plain copy method.

See [`skill/SKILL.md`](skill/SKILL.md) for the full set of rules Claude follows.

## Using the pieces directly (without the skill)

- **HTML:** link [`skill/assets/theme.css`](skill/assets/theme.css); start from `skill/assets/html-template.html`.
- **Power BI:** View ▸ Themes ▸ Browse for themes ▸ select `skill/assets/acadia-powerbi-theme.json` (theme name **"Acadia 2026"**).
- **Charts:** copy the matplotlib / plotly / D3 snippets in [`skill/references/charts.md`](skill/references/charts.md).
- **Word/PDF:** follow [`skill/references/documents.md`](skill/references/documents.md).

## Trademark notice

The Acadia University name, shield, and wordmark are trademarks of **Acadia University** and are
included here for authorized institutional use. Colors and fonts follow the published
[Acadia brand guidelines](https://www2.acadiau.ca/about-acadia/acadia-brand.html). Do not use the
logos or brand outside of authorized Acadia contexts. The skill code/structure may be reused; the
brand assets may not.
