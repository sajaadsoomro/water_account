# SIDA AWB Live Excel Dashboard

This package turns the existing static HTML dashboard into a live GitHub Pages-ready dashboard.

## Files

- `index.html` — the live dashboard page.
- `data/lbc.xlsx` — Left Bank canals workbook. Keep this exact filename.
- `data/nara.xlsx` — Nara Canal System workbook. Keep this exact filename.

## How to publish on GitHub Pages

1. Create a GitHub repository, for example `sida-awb-dashboard`.
2. Upload `index.html` and the full `data` folder to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main`, folder `/root`, then save.
6. Open the GitHub Pages URL after deployment finishes.

## How updates work

When the dashboard opens, it fetches:

- `data/lbc.xlsx`
- `data/nara.xlsx`

The browser parses them with SheetJS and refreshes the charts/tables automatically. While the page is open, it checks again every 5 minutes. You can also click **Reload Excel now**.

## Daily update workflow

1. Update your Excel workbook locally.
2. Rename/copy the new Left Bank file as `lbc.xlsx` and the new Nara file as `nara.xlsx`.
3. Replace the two files in the GitHub repository inside the `data` folder.
4. Refresh the dashboard page.

Important: a web browser cannot automatically read an Excel file from your personal computer for security reasons. The Excel file must be uploaded to GitHub or another public/static hosting location that the dashboard can fetch.
