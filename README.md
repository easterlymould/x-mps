X MPs

A static transparency site listing UK Members of Parliament who have declared income linked to X Corp (formerly Twitter).

The site displays:

Total income received since 1 January 2026

Number of payments

Declared hours (where available)

Individual payment breakdowns

Click the header title “X MPs” to return to the main page.
The About page explains context and methodology.

Data source

Data is derived from the UK Parliament Register of Members’ Financial Interests (RMFI) via structured datasets.

This repository does not generate the underlying parliamentary data.
The donation_data/ folder is automatically synced from a private source repository.

Original records remain subject to Parliamentary licensing terms.
This project does not claim ownership of the underlying public records.

Project structure
/
├── index.html
├── about.html
├── donation_data/
└── .github/workflows/

Running locally

Because the site fetches CSV files, use a local server:

python3 -m http.server 8000


Then open:

http://localhost:8000

Deployment

This site is deployed using GitHub Pages from the main branch.

Updating data

Data is synced automatically via GitHub Actions.
No manual deployment is required when source data updates.

Licence

This project’s code is licensed under the MIT Licence.

Parliamentary source data remains subject to its original licensing terms.