# AT&T telephone operators — Feigenbaum & Gross 2021 / MS 2025 extraction

Numerical extraction from Feigenbaum, J.J. & Gross, D.P. (2021/2023) "Organizational and Economic Obstacles to Automation: A Cautionary Tale from AT&T in the Twentieth Century," NBER Working Paper 29580 (revised July 2023); published as Feigenbaum & Gross 2025 in *Management Science*. 69pp + Web Appendix.

Source PDF: `../../research/academic-papers/feigenbaum-gross-2021-ms2025-att-obstacles-to-automation-w29580.pdf`. Accessed 2026-04-14.

## Files

- `industry-employment-1902-1937.csv` — US telephone industry workforce Table 1 (Census of Electrical Industries quinquennial)
- `dial-penetration-1913-1972.csv` — Bell System dial penetration S-curve (Figure 1)
- `cutover-event-study-coefficients.csv` — 15 DiD event-study coefficients (Tables 3, 4)

## Key verified anchors

### The capability-to-deployment gap — resolved [v0.1 handoff citation flag]

The handoff flagged "~40-year AT&T capability-to-deployment gap" as a pending citation. Paper gives three candidate gaps:

| Measurement | Years |
|-------------|-------|
| Strowger patent → first AT&T commercial dial deployment (Norfolk VA) | **1889 → 1919 = 30 years** |
| Strowger patent → 50% Bell System mechanization | **1889 → ~1937 = 48 years** (Figure 1 chart read-off) |
| Strowger patent → 100% Bell System mechanization (Catalina Island) | **1889 → 1978 = 89 years** |

The "~40 year" figure in v0.1 is closest to the 50% penetration benchmark (48 yr). More precise v0.3 framing: **first commercial deployment lagged the patent by 30 years; full mechanization took another 59 years after that**.

### The organizational-complexity-as-lag-driver claim — VERIFIED

The paper's thesis (formally modelled in Section 4, empirically tested in Section 5 event study, further developed in Section 6): automation of an "integral task" (one that interacts with nearly every other activity in the production system) is retarded by the interdependencies the integral task imposes. Call switching was AT&T's integral task. Figure 3 Panel A maps the dependencies: handsets, PBX, number plan, directory, pay phones, subscribers, local services, long distance, accounting/billing, regulator, management, switching equipment, call monitoring, equipment manufacturing — all connected to call switching as the fulcrum.

Mechanizing call switching required changes across all of these. Figure 3 Panel B enumerates the complementary innovations required at: AT&T corporate (test equipment + mfg scale + manager education + regulatory stance), Central Offices (equipment install + rewire + auto-manual integration + new services + transitional labor), user behavior (acceptance + training + media campaign + secretarial substitution), user technology (new handsets + numbering plans + directories + alphanumeric-to-numeric mapping), regulators (rate changes + public concerns).

**Formal model prediction (Proposition 3, paper p. 19):** when the replacement technology's productivity advantage (α) is small relative to its fixed-cost investment (θ), complete automation is not profitable, even for a monopolist. The system stays manual despite the available technology. Reopens the monopolist's automation choice when technology improves (α rises) OR market grows (M rises).

**Empirical verification (Table 6):** a doubling of city population is associated with a **+12.5pp probability of mechanization by 1940**. Largest 50 cities (1910): 98% mechanized by 1940. Cities 51-100: 79%. Cities 101-500: 31%. All others: 7%. Market size drove adoption; young-women's employment rates did not — labour-market tightness was not the binding constraint, network complexity × market scale was.

### Workforce effects (Table 3, 4, 5) — cutover city event study

Sample: 2,846 US cities with population ≤100,000 in 1920; 261 had a cutover pre-1940. Identification: staggered city-level cutover dates from hand-collected newspaper reports (>26,000 newspaper pages, 3 source databases, 688 cutovers identified by 1940).

- **Female operators −44.3%** in cutover cities (log, p<0.01). Nearly 50% reduction in the operating force.
- **Young operators (16-25): −53.6%; older (26+): −32.6%.** Retained cohort aged up: average operator age +1.55 years; share aged 26+ up 6.1pp.
- **All workers in telephone industry −26.2%** — operators dominate aggregate but overall industry shrinks by ~30% in mechanized markets
- **Countervailing growth:** clerks +10.0%, electrical engineers +13.0%, mechanics +6.9%, managers +8.8%, inspectors +5.3% — residual tasks and new mechanical-maintenance roles absorb some of the operator labor displacement within the industry
- **Substitution:** electricians −10.8% while electrical engineers +13.0% — skill upgrade in the electrical workforce
- **Managerial span of control:** −12.8 workers/manager post-cutover. Operator rows were the high-leverage supervision; when operators disappeared, supervisory leverage collapsed with them.

### International comparison (Section 7)

- **UK:** first automatic exchange 1912 → last manual exchange ceased 1976 (**64-year adoption window**). Ran by state-owned postal service.
- **Australia:** 1912 → 1991 (**79-year adoption window**). Similar state-owned structure.
- **US:** 1919 → 1978 (**59-year adoption window**).

**Convergent 60–80 yr windows across three jurisdictional structures:** regulated monopoly (US), state-owned postal service (UK, Australia). The common factor is not regulatory regime but the underlying organizational-complexity problem. Regulatory structure shifts the distribution of rents but not the fundamental adoption duration.

## Implications for the retrofit v0.3

### Telephone operators as a new Case 5 — two classes in a single shock (like UK containerisation)

Consistent pattern with UK containerisation: **a single technology shock produces multiple class-assignments at different levels**.

At the **cutover-city level** (incumbent young female operators): Class A — immediate displacement within a single city event, −53.6% for 16-25yo operators. No Mode 1/2/3 buffering — voluntary separation, attrition, residual-task reassignment. AT&T did not maintain the operator cohort as an absorbing employer because the residual-task workload was smaller than the displaced headcount.

At the **industry level through 1927**: Class C-like — industry employment grew from 262,629 (1917) → 312,015 (1922) → 375,272 (1927) even as dial penetration hit ~20% by 1927. Demand-side growth of phone service absorbed most of the mechanization effect at the industry aggregate. Operator share of industry workforce stayed at 55-65% through 1920–1940.

After 1927 the industry contracts: 375k → 334k (1932) → 333k (1937). Female employment peaks in 1927 and declines: 243k → 205k → 203k. This is partly Depression + partly mechanization crossing the threshold where output growth could no longer absorb the operator displacement.

**Refinement to Takeaway 10 (A/B/C taxonomy):** Class membership is not only per-cohort-within-case but also **per-geographic-scale-within-case**. The same shock can produce Class A at city level and Class C at national industry level. City-level workers experienced immediate displacement; national-level industry employment grew through 1927. Both are true. Single-class assignments per case lose resolution. v0.3 model must support class × scale resolution.

### Mode 3 absorbing-employer buffering — partially verified, partially falsified

Previous 3-mode taxonomy assigned AT&T as the canonical Mode 3 (absorbing-employer) case — the regulated monopoly that reassigns workers internally rather than laying them off. Feigenbaum & Gross data supports part of this:
- **Supports:** compositional shift within cutover cities to clerks, electrical engineers, mechanics, managers — residual-task reassignment. Transitional-labor period before each cutover. AT&T's internal advice per Gherardi 1917 anticipated 70-80% reduction in operator requirements but did not mandate layoffs.
- **Falsifies (partially):** cutover effect on operator count is **−44.3%**, not −10% or −20% that would signal strong absorbing-employer buffering. Aggregate industry employment in cutover cities falls −26.2%. This is not Mode 3 "absorbing" — it is "some reassignment but net large reduction." The Mode 3 narrative was overstated in the 3-mode taxonomy v2.

**v0.3 revision:** AT&T operators is a **weak Mode 3** case — some internal reassignment, but net displacement of ~30% of the industry workforce per cutover, and ~50% of the operator occupation specifically. The canonical strong Mode 3 case may need to come from elsewhere (Germany co-determination under Dauth et al. 2017 robots is a candidate, but it operates at a different scale — the firm not the industry). Flag: revisit the Mode 3 canonical-case assignment after step 5 (Acemoglu/Restrepo + Dauth robots).

### The "two clocks" finding strengthened

AT&T data reinforces the two-clocks finding from UK containerisation:
- **Industry-cost/productivity clock:** ~10 years from 1917 AT&T advisory → 1927 industry employment peak to early 1930s industry contraction (the industry cost structure resets within ~15 years of the firm commit decision)
- **Complete-mechanization clock:** 1889 → 1978 = 89 years (the last manual exchange persisted for nearly a century after the technology was available)

The two clocks differ by a factor of **~6x** for AT&T (vs ~5x for UK containers). Historical convergent evidence: institutional + economic buffering has to operate on a timescale of order 50-100 years after the technology becomes available for the long-tail population served by small markets, rural areas, or economically marginal applications to be fully converted. This far exceeds the lifetime of the displaced incumbent cohort. **Long-tail adoption is slower than the incumbent workforce's productive life.**

### Framework input for Lens 1 class router (Takeaway 10)

Empirical contribution:
- Cohort-level: Class A (cutover event displaces ~half of operator cohort immediately in each city)
- Industry-level, early adoption: Class C-like (industry grows through 1927 despite mechanization)
- Industry-level, middle adoption: shifts to Class A as output-growth absorbing capacity runs out
- **Transition is endogenous** — a case can start Class C and become Class A when market saturates. Previous v0.3 framing treated class as static per case-cohort; AT&T data shows the class can **flip when the demand-elasticity condition stops binding**.

This is a stress-test on the static-class assumption in the v0.3 router. Needs to be integrated in step 6 Lens 1 spec: either class assignment becomes time-varying, OR the router re-runs at fixed intervals (5-year census cycles are natural in the historical data).

## Citation hygiene

All numbers in CSVs are direct extractions from tables or chart read-offs with uncertainty bands marked. Key prose claims are paraphrased rather than quoted, except where the paper states a specific penetration percentage verbatim.

Cite as: Feigenbaum, J.J. & Gross, D.P. (2023). "Organizational and Economic Obstacles to Automation: A Cautionary Tale from AT&T in the Twentieth Century." NBER Working Paper 29580. Published 2025 in *Management Science*.

Underlying sources for numerical claims:
- Table 1: US Census of Electrical Industries 1902-1937
- Figure 1: AT&T Archives and History Center, box 85-04-03-02, "Bell System Distributions of Company Telephones"
- Tables 3-4: IPUMS complete-count census 1910-1940 + hand-collected newspaper cutover data (688 cutovers from 26,000 newspaper pages)
- Figure 3: AT&T archival records + Lipartito (1994a,b) + Freeman (1937) "History of the Panel Machine Switching System"
