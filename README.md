# How Victorians Commute

FIT2179 Data Visualisation 2 submission project for Yinglun Guo (35964952).

## Structure

- `index.html`: single-page visualisation for GitHub Pages.
- `style.css`: typography, layout and responsive styling.
- `data/*.json`: cleaned public data used by the Vega-Lite views.
- `specs/*.json`: readable Vega-Lite JSON specification for each chart, as required by the assignment brief.
- `moodle-description.md`: draft 500-word Moodle response covering domain, who, what, why and how.

## Run locally

Use a small local web server because the page fetches JSON files.

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## GitHub Pages

Push this folder to a public GitHub repository and enable Pages from the repository root or `main` branch. Submit the GitHub Pages URL plus the sketch PDF URL on Moodle.

## Data sources

- Australian Bureau of Statistics, Census of Population and Housing 2011, 2016 and 2021: https://www.abs.gov.au/census
- ABS 2021 Victoria QuickStats: https://www.abs.gov.au/census/find-census-data/quickstats/2021/2
- Australian Bureau of Statistics, Australia's Journey to Work, 2022: https://www.abs.gov.au/articles/australias-journey-work
- Australian Bureau of Statistics, QuickStats and Community Profiles, 2021.
- ABS digital boundary files / public geographic boundary references for the simplified Victoria outline.
