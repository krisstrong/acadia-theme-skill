# Word (.docx) & PDF conventions

Apply these when generating documents (use the `docx` skill for Word, `pdf` skill for PDF). All values from [`design-tokens.md`](design-tokens.md).

## Fonts
- **Headings:** Avenir Next. If unavailable on the target machine, fall back to **Arial Bold** (do not substitute a serif). Color: Acadia Blue `#004077`.
- **Body:** Arial, 11pt, color Ink `#1A1A1A`, line spacing 1.15–1.5.
- **Emphasis/callouts:** Acadia Red `#C41424`, used sparingly.

## Heading styles
| Style | Font | Size | Weight | Color |
|-------|------|------|--------|-------|
| Title (cover) | Avenir Next/Arial | 26–32pt | Bold | `#004077` |
| Heading 1 | Avenir Next/Arial | 18pt | Bold | `#004077` |
| Heading 2 | Avenir Next/Arial | 14pt | Semibold | `#004077` |
| Heading 3 | Avenir Next/Arial | 12pt | Semibold | `#3D3D3D` |
| Body | Arial | 11pt | Regular | `#1A1A1A` |
| Caption | Arial | 9pt | Regular | `#6B6B6B` |

## Page layout
- Margins 1" (2.54cm) all sides; letter size unless specified.
- Optional accent rule: a thin Acadia Red (`#C41424`) or Blue line under the title or in the header band.
- Header band (reports): solid Acadia Blue band with white logo + document title.
- Footer: page number + document name in Gray 500, with a 3px Acadia Red top border.

## Tables
- Header row: Acadia Blue `#004077` fill, white bold text.
- Body: white rows, alternating Gray 100 `#F5F6F8` for zebra striping.
- Borders: Gray 300 `#D7DAE0`, thin.

## Cover page pattern (reports)
1. White or Acadia Blue full-bleed background.
2. Logo top-left (white logo if blue background).
3. Title in Avenir Next, then subtitle in Gray.
4. Acadia Red accent rule between title and subtitle.
5. Date + author at bottom in Gray 500.

## Charts inside documents
Always use Tableau Classic 10 series colors (see [`charts.md`](charts.md)). Export charts at white background so they sit cleanly on the page.
