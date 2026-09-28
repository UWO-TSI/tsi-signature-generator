# tsi-signature-generator

Email signature generator for Tech for Social Impact (TSI) execs.

Live: https://uwo-tsi.github.io/tsi-signature-generator/

## For execs

1. Open the link above.
2. Find your card, click **Copy signature**.
3. Gmail: Settings → See all settings → General → Signature → Create new → paste → Save.

The `email` dropdown switches between your UWO/Ivey email (default) and your preferred email. The `color` dropdown switches the mark and links between ink (default), main blue (#002FA7) and light blue (#1d9bf0).

## How it works

- `index.html` fetches the exec directory Google Sheet as CSV on page load (the sheet must be viewable by anyone with the link). If the fetch fails, a CSV file picker appears as a fallback.
- Columns used: `Name`, `Role`, `Phone`, `Preferred Email`, `UWO/Ivey Email`, `LinkedIn`. LinkedIn only shows if the cell is a full URL.
- `logo.png` (ink), `logo-main-blue.png` (#002FA7) and `logo-blue.png` (#1d9bf0) are the mark, served from this repo via GitHub Pages and referenced by absolute URL in the copied signature.
- Org name, chapter, sheet ID and base URL live in the `CONFIG` object at the top of the script in `index.html`; colors per variant live in `THEMES`.
