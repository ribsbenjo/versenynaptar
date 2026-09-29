# Versenynaptár

EVK case competition deadlines on a calendar. It's a static site: `index.html` reads `casecomp.csv` in the browser, so there's no backend.

## Updating the list

1. Edit `casecomp.csv` (Excel: *Save As → CSV UTF-8*, keep the column headers as they are).
2. Commit and push. GitHub Pages redeploys in about a minute.

Only the month and day of `Jelentkezési határidő` and `Verseny kezdete` matter. The page maps them onto the current school year (Aug–Jul). `Verseny vége` is used for the length of the competition, so a start and end in different years still works.

The **Idővonal** view shows each competition as a bar from start to end, with a diamond on its deadline.

## Running it locally

Opening `index.html` by double-clicking won't load the CSV (browsers block that). Run this instead:

```bash
python3 -m http.server
```

Then open http://localhost:8000.
