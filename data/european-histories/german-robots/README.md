# German Robots — industrial-robot displacement case data

Verified data for the German industrial-robots disruption case in the European Disruptions Map. This is the primary European counterpart to the Acemoglu/Restrepo US robots case (`../../../research/academic-papers/acemoglu-restrepo-2017-jpe2020-robots-and-jobs-w23285.pdf`).

## Files

- `coefficients.csv` — headline IV coefficients from Dauth et al. (2017) Tables 1–7. Standardized effect sizes per additional robot per 1,000 workers, 1994–2014.
- `robot-density-series.csv` — industrial-robot stock per 1,000 workers, Germany vs. Europe vs. US, 1994–2014. Source: Figure 1a.

## Source

Dauth, W., Findeisen, S., Südekum, J., Woessner, N. (2017) "German Robots — The Impact of Industrial Robots on Workers." *IAB-Discussion Paper 30/2017*, 63pp. Institute for Employment Research, Federal Employment Agency (Germany). ISSN 2195-2663. Filed at `../../../research/academic-papers/dauth-findeisen-suedekum-woessner-2017-iab-dp30-german-robots.pdf`. Same authors + analysis as the CEPR Discussion Paper 12306 version previously cross-referenced; IAB DP 30/2017 is the IAB working-paper release.

Underlying primary sources used by the paper: International Federation of Robotics (IFR) industry-level robot stocks 1994–2014; Establishment History Panel (BHP) for German employment; EUKLEMS for other European employment; Bureau of Labor Statistics for US; German Integrated Employment Biographies (IEB) v12.00.00 for worker-level analysis (993,184–2,677,990 worker panel depending on specification); COMTRADE for trade controls.

## Key quantitative findings (verbatim or direct calculation from paper)

### Aggregate employment (Tables 1–2, IV specifications, 1994–2014)

- **Zero effect on total local employment** (Table 2, Panel A, col 1, IV): −0.0058 (SE 0.120), statistically indistinguishable from zero. Preferred specification with region dummies, demographics, industry shares, and dropping Wolfsburg + Dingolfing-Landau automotive outliers.
- **Negative effect on manufacturing employment** (Table 2, Panel A, col 2, IV): **−0.3837** log-points (SE 0.152, p<0.05) per additional robot per 1,000 workers.
- **Positive offsetting effect on non-manufacturing employment** (Table 2, Panel A, col 5, IV): **+0.4177** log-points (SE 0.206, p<0.05) per additional robot per 1,000 workers. Manufacturing loss fully offset by service-sector gain.
- **Manufacturing employment/population ratio** (Table 2, Panel F, col 2, IV): **−0.0595** percentage points (SE 0.027, p<0.05) per additional robot per 1,000 workers. Against base-year ratio 0.2812, this implies **2.12 manufacturing jobs lost per additional robot per 1,000 workers** (p. 27).
- **Headline aggregate loss:** Total German robot stock 130,428 units installed 1994–2014 → **276,507 manufacturing jobs lost = 23% of the 1.2M manufacturing employment decline** (p. 27). Remaining 77% driven by other factors (trade, ICT, offshoring).
- **US comparison:** Acemoglu & Restrepo estimate 6.2 US manufacturing jobs lost per robot per 1,000 workers (p. 27). **German coefficient (2.12) is approximately one-third the US coefficient.** This is the primary quantitative contrast.

### Robot density (Figure 1a, IFR data)

- **Germany 1994:** ~1.9 robots per 1,000 workers (2× European average, 4× US).
- **Germany 2014:** **7.6 robots per 1,000 workers** (vs. Europe 2.7, US 1.6). Quadrupled over two decades (p. 7).
- **Industry concentration:** automotive-sector concentration in Wolfsburg + Dingolfing-Landau districts drives outlier density; these districts excluded from preferred specification.

### Worker-level effects (Tables 3–4, IV, 1994–2014)

- **Incumbent manufacturing workers are MORE likely to remain employed.** Days employed, cumulated over 20 years (Table 3, Panel B col 6, IV, all controls + automotive dropped): **+1.1534** additional days employed (SE 0.596, p<0.10) per additional robot per 1,000 workers. Headline specification col 1: +3.56 days.
- **Decomposition: the positive effect is entirely in-firm retention, not cross-firm reallocation.** Table 4, Panel A (Industry mobility, IV):
  - Same employer: **+11.4410** days (SE 2.124, p<0.01) ← the mechanism
  - Same sector, different employer: **−4.6514** days (SE 1.475, p<0.01)
  - Different manufacturing industry: −2.0260 days (SE 1.669, insignificant)
  - Outside manufacturing: **−3.9632** days (SE 0.363, p<0.01)
  - Net across all employers: +0.8003 days (SE 0.349, p<0.05)
- **Occupational mobility within the same employer** (Table 4, Panel B, IV): +6.39 days same occupation, +5.05 days different occupation same employer. Workers are reassigned to new tasks within the same firm; they are NOT displaced then rehired elsewhere.

### Entry mechanism (Table 5, IV)

- **New young-worker entry into robot-exposed manufacturing industries is FORECLOSED.** Dependent variable: change in manufacturing-entrant share of all regional entries 1994–2014, IV:
  - Effect on young-worker entry: **−0.1335** percentage points (SE 0.068, p<0.05) per additional robot per 1,000 workers.
  - Effect on returnee re-entry (from unemployment): +0.0297 percentage points (SE 0.079, insignificant).
- **This is the aggregate mechanism.** Incumbent workers are retained in-firm; the 276k manufacturing-job decline is driven by foreclosed entry for the next cohort, not displacement of the current cohort.

### Earnings and wages (Table 6, IV, 1994–2014)

- **Average individual wages fall despite longer cumulative employment.** Table 6, Panel B (average daily wage, IV col 6): **−0.0649** log-points (SE 0.015, p<0.01) per additional robot per 1,000 workers.
- **Medium-skilled workers bear the cost** (Figure 6, Panel c). Completed-apprenticeship workers (~75% of the German manufacturing workforce) experience significant negative earnings effects. High-skilled (university-educated, ~9% of sample) gain; low-skilled effects negative but imprecisely estimated.
- **By occupation:** Machine operators lose; management/law and technical/natural-sciences gain. Consistent with the skill-biased interpretation.
- **Magnitude benchmark (p. 35):** A worker at the 75th percentile of robot exposure loses €1,266 cumulative over 20 years relative to a 25th-percentile worker (€63/year). Comparing 90th vs. 10th percentile: €15,930 loss over 20 years (€800/year).

### Aggregate distribution (Table 7, IV, 2004–2014)

- **Robots raise productivity, not wages.** Per additional robot per 1,000 workers:
  - Labor productivity (GDP/worker): **+0.5365** log-points (SE 0.268, p<0.05)
  - Average gross pay per employee: −0.3109 log-points (SE 0.249, insignificant)
  - Labor productivity minus gross pay: **+2.0757** log-points (SE 0.945, p<0.05) ← productivity gain captured by non-labor income (capital/profit), not wages
  - Unemployment rate: −0.0693 pp (p<0.10) — slight reduction
- **Interpretation (Section 7, p. 41, verbatim, <20 words):** robots "contribute to the decline of the labor income share."

## Key causal findings (for lag-retrofit)

### Explicit Mode 3 mechanism (direct quote, <20 words)

Per Section 7 (p. 41–42): German unions accept "wage cuts to stabilize jobs for incumbent insiders" through co-determination and works councils.

### The three-element buffering mechanism (paraphrased, with citations)

1. **Co-determination law (Betriebsverfassungsgesetz 1972) + works councils** collectively determine task reassignment within the firm when new technology is deployed — per Section 7 interpretation (p. 41).
2. **Unions accept wage restraint in exchange for job security** — per Section 7 interpretation citing Dustmann et al. 2014 on the post-mid-2000s "employment miracle." Median-skilled workers lose wages; insiders retain jobs.
3. **Apprenticeship system (completed-apprenticeship workers = ~75% of manufacturing workforce)** provides the re-trainable task base that allows within-firm reassignment rather than layoff → rehire.

### Differs from US (Acemoglu & Restrepo 2020)

- **US:** one more robot per 1,000 workers reduces total employment/population by 0.37 pp → 6.2 total jobs lost per robot (preferred specification); no offsetting employment gains in any occupation or education group.
- **Germany:** one more robot per 1,000 workers reduces manufacturing jobs by 2.12; zero effect on total employment; offsetting gain in non-manufacturing services; incumbents retained via in-firm reallocation; aggregate loss driven by foreclosed youth entry.
- **The ~3× US/Germany gap is consistent with institutional divergence:** same technology, different labor-market architecture, different outcomes.

### Distributional cost of Mode 3 buffering

The canonical Mode 3 case in the retrofit v0.3 taxonomy now rests on a verified mechanism that is **not costless**:
- Incumbents: more stable jobs, lower wages (−€63 to −€800/year depending on exposure gradient).
- Medium-skilled workers (~75% of sample) bear the wage cost.
- High-skilled workers gain.
- Aggregate labor income share falls; productivity gains accrue to capital.
- Young workers: foreclosed entry into robot-exposed manufacturing industries.

**Mode 3 protects the incumbent at the cost of the cohort.** This is structurally identical to the containerisation "buffered incumbent, displaced next-cohort" pattern observed in UK dockworkers (El-Sahli & Upward 2015) — same structure, different mechanism (wage restraint vs. income floor).

## Relevance to the Disruptions Map retrofit (v0.3)

### Confirms Germany as the canonical strong Mode 3 case

Prior retrofit versions assigned AT&T (telephone operators) as the canonical Mode 3 "absorbing-employer" case. Feigenbaum & Gross (2023/2025) partially falsified that: operator cutover produced −44.3% occupation employment and −26.2% all-workers in the cutover city; residual-task reassignment covered only a minority of displaced headcount. AT&T is a **weak Mode 3** case.

**Dauth et al. 2017 verifies Germany as a strong Mode 3 case.** The +11.4410 same-employer days coefficient at the 1% significance level, paired with the Section 7 institutional mechanism, resolves the pending assignment: Germany moves from HYPOTHESIS to VERIFIED canonical strong Mode 3 case at the firm level.

### Resolves the Class A (US) + Class B (Germany) bifurcation

Same technology (industrial robots); different institutional perimeter; different class assignment. Structurally identical to UK containerisation's Class A + Class B split (non-NDLS ports vs. NDLS-protected cohort). Robots are the second retrofit case to exhibit class bifurcation contingent on institutional architecture, not technology characteristics.

### Sharpens the three-mode buffering framework

- **Mode 1 (income-floor, UK dockworkers):** Protected cohort stays in job occupation until protection ends; adoption proceeds *outside* the protected perimeter (Felixstowe). Spatial displacement is the externality.
- **Mode 3 (absorbing-employer, German robots):** Protected cohort reassigned to new tasks *within* the protected perimeter; adoption proceeds *inside* the firm via task reassignment. Wage cost and cohort foreclosure are the externalities.
- **Both modes buffer the incumbent and push the cost to an adjacent cohort or geography.** The displacement is not eliminated; it is rerouted. This reinforces the Layer 6 structural-optimism warning: institutional buffering slows and redistributes displacement, but does not prevent it in aggregate.

## Confidence levels

| Claim | Confidence | Source |
|---|---|---|
| −0.3837 manufacturing employment coefficient | HIGH | Table 2 Panel A, IV, SE 0.152 |
| +0.4177 non-manufacturing offsetting gain | HIGH | Table 2 Panel A, IV, SE 0.206 |
| 2.12 manufacturing jobs lost per robot/1,000 workers | HIGH | Table 2 Panel F direct calculation, p. 27 |
| 23% of manufacturing decline, 276,507 jobs | HIGH | Abstract + p. 27 |
| +11.44 same-employer days retention | HIGH | Table 4 Panel A, IV, SE 2.124 |
| −0.1335 youth-entry foreclosure | HIGH | Table 5 col 1, IV, SE 0.068 |
| −0.0649 log-point wage effect | HIGH | Table 6 Panel B col 6, IV, SE 0.015 |
| +0.5365 productivity gain captured by capital | MEDIUM–HIGH | Table 7 col 1, IV, SE 0.268; based on 2004–2014 subsample |
| Mode 3 canonical strong-case assignment | HIGH | Mechanism directly described Section 7 p. 41–42 |
| US vs. Germany contrast (2.12 vs. 6.2 jobs per robot) | HIGH | Direct paper comparison p. 27 |

---

**Extracted:** 2026-04-14 (session closing retrofit v0.3 Dauth pending-flag resolution)
**Resolves PENDING flags in:**
- `retrofit-lag-reconstruction.md` Case 6 (Step 5b, lines 867–895, 984, 1008, 1013)
- `site/disruptions-data.json` structured_metrics.robots_manufacturing class_assignment_germany + metrics (b)(c)(e)(f)
- `skills/disruption-analysis/SKILL.md` Takeaway 16 Mode 3 assignment
