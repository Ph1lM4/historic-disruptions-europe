# What Happened Every Other Time: Historic Technology Disruptions and European Labour

580 years of technology disruptions analysed to extract patterns that predict how AI will reshape European labour markets. Part 3 of 7 in the European AI Labour Market suite. Companion to the [AI Exposure Map](https://github.com/Ph1lM4/ai-job-impact-europe) and the [Job Market Map](https://github.com/Ph1lM4/job-market-europe).

**What makes this different:** Most AI-and-labour commentary cites one or two historic analogies (usually ATMs and horses). This project analyses 20 case studies across 580 years — 9 general-purpose technologies and 11 occupation-level disruptions — and extracts 5 distinct disruption patterns with 6 diagnostic variables that predict which pattern a given occupation will follow.

## Live Site

**[disruptions.nexalps.com →](https://disruptions.nexalps.com)** *(static site, no backend)*

## What's Included

| Page | Description |
|------|-------------|
| [Overview](https://disruptions.nexalps.com/) | GPT timeline, disruption taxonomy, 10 key patterns |
| [Case Studies](https://disruptions.nexalps.com/cases.html) | 20 case study deep dives with ISCO codes |
| [Findings](https://disruptions.nexalps.com/findings.html) | Cross-case synthesis and diagnostic variables |
| [Outcomes](https://disruptions.nexalps.com/outcomes.html) | 8 displaced worker outcomes, retraining evidence, age gradient |
| [Sources](https://disruptions.nexalps.com/sources.html) | ~52 academic and institutional sources with tier ratings |
| [llms.txt](https://disruptions.nexalps.com/llms.txt) | Machine-readable project summary |

## Key Findings

- Every general-purpose technology follows a **20–50 year arc** from market entry to measurable productivity gains
- Disruptions cluster into **5 distinct patterns**: Demand Creation, Transformation + Expansion, Role Absorption, Market Restructuring, Full Elimination
- **6 diagnostic variables** predict which pattern a given occupation will follow
- Retraining programmes show **"modest positive effects at best"** (Card/Kluve/Weber 207-study meta-analysis)
- Worker recovery **collapses after age 50**: reemployment probability halved, earnings loss doubled
- **Geographic scarring lasts 30–50 years** (UK coalfields, US Rust Belt — still no convergence)
- European institutional frameworks (works councils, *Kurzarbeit*, co-determination) produce **measurably different outcomes** than US labour-market flexibility (Dauth et al. CEPR 2017)
- **Children of displaced workers earn 9% less** — displacement transmits across generations
- AI is currently a **net hiring driver in Europe** (ECB SAFE survey, 5,300 firms, March 2026) — but 25% of German firms expect AI job cuts within 5 years (ifo 2025). Displacement is delayed, not cancelled.

## The 20 Case Studies

### 9 Macro — General Purpose Technologies

| # | Technology | Period | Arc |
|---|---|---|---|
| 1 | Printing Press | 1440s–1600s | 160 years |
| 2 | Mechanised Loom | 1760s–1850s | 90 years |
| 3 | Steam / Railways | 1800s–1870s | 70 years |
| 4 | Electricity | 1880s–1930s | 50 years (40-year productivity lag) |
| 5 | Assembly Line | 1910s–1950s | 40 years |
| 6 | Computer / Mainframe | 1950s–1980s | 40 years (Solow paradox) |
| 7 | PC / Office Automation | 1980s–2000s | 25 years |
| 8 | Internet / E-commerce | 1995–2015 | 20 years |
| 9 | Mobile / Platform Economy | 2007–2020 | 13 years |

### 11 Micro — Occupation-Level Disruptions

| # | Disruption | Pattern |
|---|---|---|
| 1 | ATMs → Bank Tellers | Type 2 (employment doubled before mobile banking reversed it) |
| 2 | Spreadsheets → Accountants | Type 2 (market expansion, accountants grew) |
| 3 | Containerisation → Dockworkers | Type 5 (90%+ reduction, 40-year geographic scarring) |
| 4 | CAD → Technical Drafters | Type 3 (absorbed into engineering) |
| 5 | Telephone Operators | Type 5 (full elimination over 60 years) |
| 6 | Elevator Operators | Type 5 (50-year adoption despite mature technology) |
| 7 | DTP → Typesetters | Type 5 (high-skill role eliminated in 15 years) |
| 8 | Industrial Robots → Manufacturing | Type 2/5 hybrid (Germany vs US divergence) |
| 9 | GPS/Ride-hailing → Taxi | Type 4 (restructuring + absorption) |
| 10 | E-commerce → Retail | Type 2 → Type 4 transition |
| 11 | LLMs → Knowledge Workers | Type 2 early stage (74.5% programmer task coverage; no net unemployment yet, young-worker hiring slowed 14%) |

## The 5 Disruption Patterns

- **Type 1 — Demand Creation.** New occupations appear. The technology creates roles that did not exist before.
- **Type 2 — Transformation + Market Expansion.** The role changes, but the market expands faster than productivity rises. Employment grows (ATM pattern).
- **Type 3 — Role Absorption.** The skill folds into an adjacent, higher-skilled role (CAD into engineering).
- **Type 4 — Market Restructuring.** The work continues but ownership, licensing, and income structure change (Uber/taxi).
- **Type 5 — Full Task Automation.** Tasks are automated end-to-end; the occupation shrinks sharply (containerisation, telephone operators, typesetting).

## The Suite

This is Part 3 of 7 in the European AI Labour Market suite:

1. **[AI Exposure Map](https://ai-exposure.nexalps.com)** — AI exposure scores for ~130 occupation groups × 36 countries
2. **[Job Market](https://job-market.nexalps.com)** — Hiring trends and career intelligence across 9 roles × 34 countries
3. **[Disruptions](https://disruptions.nexalps.com)** — What happened every other time (this repo)
4. *Coming soon*
5. *Coming soon*
6. *Coming soon*
7. *Coming soon*

**How the three products connect:**

- `ai-exposure.nexalps.com` = **which jobs** AI hits
- `job-market.nexalps.com` = **where demand** is going
- `disruptions.nexalps.com` = **what happened every other time**

ISCO-08 codes bridge all three products. Shared design system (shadcn dark, Geist font, #f97316 orange accent).

## Tech Stack

- **Pure HTML/CSS/JavaScript** — no framework, no build step
- **D3.js** for interactive timelines and charts
- **Netlify** for hosting with security headers and caching (`netlify.toml`)
- **Geist** font from Google Fonts

## Preview Locally

```bash
cd site && python3 -m http.server 8092
# Open http://localhost:8092
```

## Data Sources

~52 primary academic and institutional sources across 3 tiers:

| Tier | Definition | Examples |
|------|------------|---------|
| Tier 1 | Peer-reviewed economics journals or official statistics | Dittmar (QJE 2011), Paul David (AER 1990), Acemoglu & Restrepo (JPE 2020), Feigenbaum & Gross (QJE 2024), Card/Kluve/Weber meta-analysis, Autor/Dorn/Hanson, Dauth et al. (CEPR 2017), BLS OEWS, Eurostat |
| Tier 2 | Industry reports with documented methodology | IFR World Robotics, McKinsey, BLS *Beyond the Numbers*, Burning Glass Institute |
| Tier 3 | Historical scholarship and expert analysis | Levinson (*The Box*), Thompson (*Making of the English Working Class*) |

Full bibliography at [disruptions.nexalps.com/sources.html](https://disruptions.nexalps.com/sources.html).

## Methodology

1. **Case selection.** 20 disruptions chosen to span 580 years and cover both general-purpose technologies (9) and occupation-level automation events (11).
2. **Pattern extraction.** Each case coded on 6 diagnostic variables: task substitutability, capital intensity, market elasticity, skill adjacency, institutional buffering, geographic concentration.
3. **Clustering.** Patterns cluster into 5 types (see above). Each type has a characteristic employment trajectory and institutional response profile.
4. **European cross-check.** For post-1970 cases, European outcomes compared to US outcomes where data permits (Dauth robots study, EU AI adoption, Kurzarbeit vs US layoffs).
5. **AI mapping.** Current AI deployment patterns mapped onto the five types using ECB SAFE, ifo, Anthropic Economic Index, Brynjolfsson/OpenAI productivity studies.

Unlike the AI Exposure Map (which scores occupations) and the Job Market Map (which reports current hiring), this product is **research-authored synthesis**. There is no scoring pipeline or scraping script — the data file (`site/disruptions-data.json`) is hand-curated from cited primary sources.

## License

**Dual-licensed:**

- **Code** (`site/*.html`, `site/*.js`, `site/*.css`): [MIT](LICENSE-CODE)
- **Analysis and structured data** (`site/disruptions-data.json`, case narratives, taxonomy): [CC-BY 4.0](LICENSE-DATA) — © Philipp Maul - Nexalps

Built on academic research cited throughout; see [Sources](https://disruptions.nexalps.com/sources.html) and `LICENSE-DATA` for upstream source licensing.

## Author

Built by [Philipp Maul](https://www.linkedin.com/in/pmaul/) at [Nexalps](https://nexalps.com).

## Contributing

Issues and PRs welcome. Additional historic cases, corrections to cited figures, or extensions to non-European contexts especially appreciated. If you extend the taxonomy or refine a diagnostic variable, please share back.
