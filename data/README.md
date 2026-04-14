# data/ — Source datasets

Mostly gitignored. Only derived/processed data that is safe to publish and small enough to track should be committed. See `.gitignore` at project root for full exclusions.

## Subdirectories

- `copyrighted/` — **Never publishable.** Commercial books (Levinson, Bessen) and paywalled sources. Full contents gitignored. Extract only what you need (tables, specific figures) as CSV or `.md` with page references; do not dump full scans.
- `bls/` — US Bureau of Labor Statistics series. Use sparingly — European-direct sources preferred. Exception: ATM/teller case (Bessen's US series is canonical, no European equivalent).
- `ons/` — UK Office for National Statistics. Open Government Licence; can be tracked if small.
- `eurostat/` — Eurostat open data (EU-LFS, NACE, SES). Eurostat copyright policy; tracking OK for derived series.
- `european-histories/` — European carrier and industry-association workforce archives. Mostly open public data.

## Filing convention

Name files by what they contain, not by what case they feed:
- Good: `teller-employment-series.csv`, `container-penetration-by-port.csv`
- Bad: `atm-case-data.csv`, `dockworkers-retrofit-input.csv`

One source per file where possible. Always include a `source` or `source_ref` column or header with page/URL references.
