# X MPs

A transparency tool tracking UK Members of Parliament who have declared income from X Corp (formerly Twitter), built from the [Register of Members' Financial Interests](https://publications.parliament.uk/pa/cm/cmregmem/contents2425.htm).

**Live site:** [easterlymould.github.io/x-mps](https://easterlymould.github.io/x-mps/)

## What it shows

- MPs receiving income from X Corp since 1 January 2026
- Total amounts received, number of payments, and declared hours
- Individual payment breakdowns with dates (click any MP to expand)
- Links to each MP's [TheyWorkForYou](https://www.theyworkforyou.com/) profile

Data updates automatically via GitHub Actions syncing from the parliamentary register.

## Project structure

```text
├── index.html                          # Main app (single-page, inline JS/CSS)
├── about.html                          # Context, methodology, and limitations
├── donation_data/                      # CSV data (auto-synced)
├── .github/workflows/sync-donation-data.yml
└── .gitignore
```

## Running locally

The site fetches CSV files, so you need a local server:

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

Note: `donation_data/` is populated by the GitHub Action. Locally, the folder may be empty unless you have access to the source data.

## Data source

Data is derived from the UK Parliament Register of Members' Financial Interests via [structured datasets from mySociety](https://pages.mysociety.org/parl_register_interests/datasets/commons_rmfi/latest). This project does not generate the underlying parliamentary data. Original records remain subject to Parliamentary licensing terms.

## Licence

Code is licensed under the [MIT Licence](LICENSE). Parliamentary source data remains subject to its original licensing terms.
