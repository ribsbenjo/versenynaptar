# Versenynaptár

EVK case competition deadlines on a calendar. It's a static site: `index.html` reads `casecomp.csv` in the browser, so there's no backend.

## Updating the list

1. Edit `casecomp.csv` (Excel: *Save As → CSV UTF-8*, keep the column headers as they are).
2. Commit and push. GitHub Pages redeploys in about a minute.

Only the month and day of `Jelentkezési határidő` matter. The page maps them onto the current school year (Aug–Jul).

## Running it locally

Opening `index.html` by double-clicking won't load the CSV (browsers block that). Run this instead:

```bash
python3 -m http.server
```

Then open http://localhost:8000.
