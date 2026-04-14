# data/bls/ — US Bureau of Labor Statistics

**Europe-first project — use sparingly.** BLS data is proxy for European labour markets. Prefer European statistical sources (Eurostat, ONS, BFS, national carriers) unless no European equivalent exists.

## Legitimate exception

**ATM/bank teller case** — Bessen's US teller employment series (1970–2023) is canonical and has no European longitudinal equivalent at similar quality. BLS data supplements Bessen for this case.

## Classification break at 1999

**Important:** BLS transitioned to Standard Occupational Classification (SOC) in 1999. Pre-1999 OES data uses different occupation codes and is **not directly comparable** with 1999+ data. For pre-1999 US series, use Bessen's and Feigenbaum/Gross's reconstructed series rather than trying to splice BLS archives.

## Files

- `bls-bulletin-2545-oes-1999.pdf` — Occupational Employment and Wages 1999 tables (Bulletin 2545, published April 2001). Contains national/state/MSA employment-by-SOC-code at 1999. Primary anchor year for SOC-coded US data.
- `bls-oes-1999-survey-methods-appendix-b.pdf` — 1999 survey methodology. Reference only.

## Key reference URLs

- `bls.gov/oes/tables.htm` — current OES/OEWS tables, 1997–present
- `bls.gov/opub/hom/oews/history.htm` — Handbook of Methods OEWS history (classification transitions)

## What to extract from the bulletin

If pulling 1999 anchor data, priority SOC codes:

| SOC code | Occupation | Retrofit case |
|---|---|---|
| 43-3071 | Tellers | ATM case (anchor year) |
| 17-3011 | Architectural & Civil Drafters | CAD case (optional cross-check) |
| 17-3013 | Mechanical Drafters | CAD case (optional cross-check) |
| 51-5022 | Typesetters & Compositors | DTP case (optional cross-check) |
| 43-2021 | Telephone Operators | Tel ops case (optional cross-check) |

One row per occupation: year 1999, national employment, mean wage, source page.
