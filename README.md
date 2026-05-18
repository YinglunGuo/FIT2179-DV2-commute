# How Victorians Commute

FIT2179 Data Visualisation 2 submission for Yinglun Guo (35964952).
A single-page Vega-Lite story on Victorian and Australian journey-to-work patterns 2011–2021, with one 1976–2021 long-run view.

## Structure

- `index.html` — story-structured single page (hero → 4 chapters → 14 charts incl. 1 custom small-multiples and 1 linked-views panel → methodology → footer).
- `style.css` — typography (Source Serif 4 display + Inter body), layout, responsive breakpoints.
- `data/*.json` — cleaned, public ABS-derived data used by the Vega-Lite views.
- `specs/*.json` — readable Vega-Lite v5 JSON specifications for every chart, as required by the brief.
- `moodle-description.md` — Moodle response (under 500 words) covering domain, who, what, why, how with explicit Munzner What/Why/How framing.
- `sketch.pdf` — hand-drawn sketch (required for the Sketch component, 2%).

## Run locally

The page fetches JSON specs at runtime, so it must be served over HTTP — opening `index.html` from disk will fail.

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## GitHub Pages

Push this folder to a public GitHub repository and enable Pages → Deploy from a branch → `main` / root. The marker URL is the GitHub Pages root, e.g. `https://YinglunGuo.github.io/FIT2179-DV2-commute/`.

## Data sources (deep links)

Every figure on the page traces to a public ABS page or to id.com.au community profiles (ABS-derived).

### National-level

- ABS, **Australia's Journey to Work** (3 Nov 2022) — Method of travel, GCCSA breakdowns, WFH 1976–2021 state matrix, PT mode counts, active transport totals: <https://www.abs.gov.au/articles/australias-journey-work>
- ABS press release — **2.5 million people working from home on Census day** (28 June 2022): <https://www.abs.gov.au/media-centre/media-releases/2021-census-25-million-people-working-home-census-day>
- ABS Australia QuickStats 2021: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/AUS>

### State / territory

- ABS 2021 Victoria QuickStats: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/2>
- All state/territory codes: NSW `1`, VIC `2`, QLD `3`, SA `4`, WA `5`, TAS `6`, NT `7`, ACT `8`.

### Greater capital cities

- Greater Sydney: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/1GSYD>
- Greater Melbourne: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/2GMEL>
- Greater Brisbane: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/3GBRI>
- Greater Adelaide: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/4GADE>
- Greater Perth: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/5GPER>
- Greater Hobart: <https://www.abs.gov.au/census/find-census-data/quickstats/2021/6GHOB>

### Victorian LGAs (used in charts 02, 03, 04, 05, 13)

| LGA | ABS QuickStats | profile.id travel-to-work |
| --- | --- | --- |
| Melbourne City | [LGA24600](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA24600) | [melbourne](https://profile.id.com.au/melbourne/travel-to-work) |
| Port Phillip | [LGA20605](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA25340) | [port-phillip](https://profile.id.com.au/port-phillip/travel-to-work) |
| Yarra | [LGA27260](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA27350) | [yarra](https://profile.id.com.au/yarra/travel-to-work) |
| Stonnington | [LGA26350](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA26350) | [stonnington](https://profile.id.com.au/stonnington/travel-to-work) |
| Boroondara | [LGA21110](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA21110) | [boroondara](https://profile.id.com.au/boroondara/travel-to-work) |
| Darebin | [LGA22310](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA22310) | [darebin](https://profile.id.com.au/darebin/travel-to-work) |
| Whitehorse | [LGA26980](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA26980) | [whitehorse](https://profile.id.com.au/whitehorse/travel-to-work) |
| Monash | [LGA25060](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA25060) | [monash](https://profile.id.com.au/monash/travel-to-work) |
| Wyndham | [LGA27260](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA27260) | [wyndham](https://profile.id.com.au/wyndham/travel-to-work) |
| Whittlesea | [LGA27070](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA27070) | [whittlesea](https://profile.id.com.au/whittlesea/travel-to-work) |
| Hume | [LGA23270](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA23270) | [hume](https://profile.id.com.au/hume/travel-to-work) |
| Melton | [LGA24650](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA24650) | [melton](https://profile.id.com.au/melton/travel-to-work) |
| Knox | [LGA23670](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA23670) | [knox](https://profile.id.com.au/knox/travel-to-work) |
| Frankston | [LGA22170](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA22170) | [frankston](https://profile.id.com.au/frankston/travel-to-work) |
| Mornington Peninsula | [LGA25340](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA25340) | [mornington-peninsula](https://profile.id.com.au/mornington-peninsula/travel-to-work) |
| Greater Geelong | [LGA22750](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA22750) | [geelong](https://profile.id.com.au/geelong/travel-to-work) |
| Ballarat | [LGA20570](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA20570) | [ballarat](https://profile.id.com.au/ballarat/travel-to-work) |
| Greater Bendigo | [LGA22620](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA22620) | [bendigo](https://profile.id.com.au/bendigo/travel-to-work) |
| Greater Shepparton | [LGA22830](https://www.abs.gov.au/census/find-census-data/quickstats/2021/LGA22830) | [shepparton](https://profile.id.com.au/shepparton/travel-to-work) |

### Method-of-travel definitions

- ABS Method of Travel to Work — 15 modes classification (MTW15P): <https://www.abs.gov.au/census/guide-census-data/census-dictionary/2021/variables-topic/transport/method-travel-work-15-travel-modes-mtw15p>
- Greater Capital City Statistical Areas (GCCSA) standard: <https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs-edition-3/jul2021-jun2026/main-structure-and-greater-capital-city-statistical-areas/greater-capital-city-statistical-areas>

### Vehicle ownership

- ABS Number of Motor Vehicles per Household (VEHRD) variable used for chart 13: <https://www.abs.gov.au/census/guide-census-data/census-dictionary/2021/variables-topic/family-and-household/number-motor-vehicles-vehrd>

## Definitions used in this project

- **"Drove" / "Car as driver"**: ABS strict definition (employed persons aged 15+ whose main method of travel was driving a car). Used for state and national figures.
- **"Drove" (LGA-level only, charts 02–05)**: id.com.au "Private vehicle" composite (driver + passenger + truck + motorbike), which is the only LGA-level time-series ABS publishes via the community-profiles channel. Typically runs 2–4 percentage points higher than strict car-as-driver. The chart source-notes flag this.
- **"Public transport"**: train + bus + tram/light rail + ferry combined (ABS sums these in the headline "PT use ~~halved~~" stat).
- **"Active transport"**: bicycle + walked-only combined (matches ABS Active Transport Users table).

## Reuse / referencing

Source: Australian Bureau of Statistics, Census of Population and Housing 2011, 2016 and 2021; ABS Australia's Journey to Work (2022). Visualisation by Yinglun Guo for FIT2179, Monash University, May 2026.
