# tsi-signature-generator

Email signature generator for Tech for Social Impact (TSI) execs, directors and developers.

Live: https://uwo-tsi.github.io/tsi-signature-generator/

## How to use

1. Open the link above.
2. Pick **execs** or **directors & developers**, find your card, click **Copy signature**.
3. Gmail: Settings → See all settings → General → Signature → Create new → paste → Save.

The `email` dropdown switches between your UWO/Ivey email (default) and your preferred email. The `color` dropdown switches the mark and links between light blue (#1d9bf0, default) and main blue (#002FA7).

## How it works

- `index.html` fetches both tabs of the directory Google Sheet (Executives, Directors/Developers) as CSV on page load (the sheet must be viewable by anyone with the link). If the fetch fails, a CSV file picker appears as a fallback.
- Columns used: `Name`, `Role` (Executives) or `Position (Director/Developer)` and `Project Team/Portfolio` (Directors/Developers), `Phone`, `Preferred Email`, `UWO/Ivey Email` or `UWO Email`, `LinkedIn`. Directors show as `<Portfolio> Director`, developers as `Developer`. Phone only shows on Executives cards. LinkedIn only shows if the cell is a linkedin.com link or a full URL.
- `logo-main-blue.png` (#002FA7) and `logo-blue.png` (#1d9bf0) are the mark, served from this repo via GitHub Pages and referenced by absolute URL in the copied signature. `logo.png` is the favicon; keep it, because signatures copied when ink was an option still load it.
- Org name, chapter, sheet ID, tab gids and base URL live in the `CONFIG` object at the top of the script in `index.html`; colors per variant live in `THEMES`.
