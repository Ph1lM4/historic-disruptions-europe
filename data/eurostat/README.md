# data/eurostat/ — Eurostat SES & related microdata references

## Files in this directory

- `ses-microdata-variables-list-2014.xls` — Official SES microdata variable list. Documents all variables available in the Structure of Earnings Survey at individual employee level. Key variable: **B23 = Occupation in reference month (ISCO-08)**. All earnings (B41-B43), contract (B28), tenure (B26), location (A11), NACE (A13) variables present at employee granularity.

- `eurostat-microdata-availability-table-2026-03.pdf` — Official availability table (version 25-03-2026) showing which microdatasets are available via SUF (Scientific Use File, downloadable) vs Safe Centre (Luxembourg or accredited remote access only), by country and year/wave.

## Access tiers

| Tier | Access | Timeline | Constraint |
|---|---|---|---|
| **Public tables** | Eurostat data browser, free download | Immediate | Only ISCO-2-digit typically |
| **SUF microdata** | Application + approval, then downloadable | ~4–6 weeks | Non-commercial research only |
| **Safe Centre** | Luxembourg premises or accredited remote access point | Longer | Some countries (esp. DE) Safe-Centre-only |

## SES waves available (per PDF)

1995 (Safe Centre only), 2002, 2006, 2010, 2014, 2018, 2022. Both SUF and Safe Centre for most waves.

## Country constraints noted

- **Germany:** Safe Centre only for most SES waves
- **UK:** SES 2018 SUF (Brexit affects later waves)
- **Switzerland:** SES 2018 and 2022 only

## Decision for this project (2026-04-14)

**Do NOT apply for SES microdata access at this time.** Timeline (4–6 weeks) doesn't match retrofit v0.3 pace. Public ISCO-2-digit tables are sufficient for retrofit case trajectory comparison.

**Reconsider microdata application if:**
- Layer 6 corridor assignments require ISCO-3-digit distinctions ISCO-2 can't resolve
- Germany-specific buffering-taxonomy validation becomes load-bearing (requires Safe Centre)
- Any part of this work is formalised into published research (SES access restricts to non-commercial research)

## Relation to Cedefop finding

Both Eurostat SES public tables and Cedefop Skills Forecast 2025 stop at ISCO-2-digit for public release. Same structural constraint for different reasons (Eurostat: microdata disclosure protection; Cedefop: projection aggregation methodology). Both require workarounds (SES microdata application; Cedefop ISCO-2-to-3 distribution via ESCO weights) for full ISCO-3 analysis.
