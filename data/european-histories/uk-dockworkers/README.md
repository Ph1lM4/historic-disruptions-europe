# UK Dockworkers — containerisation case data

Verified data for the UK containerisation disruption case in the European Disruptions Map.

## Files

- `employment-series.csv` — GB-wide stevedore occupation and port-industry employment, 1961–2011, 7 data points. Source: El-Sahli & Upward (2015), Figure 1.
- `port-level-1961-1967.csv` — 31 major English/Welsh ports with foreign tonnage (1967), port employment (1961), stevedore count (1961). Source: El-Sahli & Upward (2015), Table A1.

## Source

El-Sahli, Z. and Upward, R. (2015) "Off the waterfront: The long-run impact of technological change on dock workers." University of Nottingham GEP Research Paper 2015/06, 44pp. Published 2017 in *British Journal of Industrial Relations*. Filed at `../../../research/academic-papers/elsahli-upward-2015-bjir2017-off-the-waterfront-nottingham-gep-2015-06.pdf`.

Underlying primary sources cited by the paper: UK Census 10% tables (1961, 1971, 2001), New Earnings Survey (1981, 1991), Digest of Port Statistics (1968), ONS Longitudinal Study (individual-level 1971–2011).

## Key quantitative findings (verbatim from paper)

- **Aggregate attrition:** Between 1961 and 2001, the port industry lost **>72%** of its employment; the occupation "dock-worker" lost **>90%**. Dock-worker disappearance accounts for **60%** of total fall in industry employment (p. 4).
- **NDLS timeline:** National Dock Labour Scheme 1947 → banned non-registered dockers in NDLS ports → Jan 1968 Tilbury container-ship ban (lasted until Apr 1970) → 1972 compulsory-redundancy prohibition → NDLS abolished **1989** → **7,200 dockers declared redundant 1989–1992** (Turnbull 1992; Turnbull & Wass 1994) (p. 4).
- **London spatial devastation:** East London port districts lost **~150,000 jobs between 1966 and 1976** due to London Docks closure, ~20% of all jobs in the area (LDDC, footnote 2, p. 1).
- **Pre-container wage premium:** Average full-time docker earned ~**30% more** than the average male worker in Britain mid-1960s (Levinson 2006, cited p. 4).

## Key causal findings (for lag-retrofit)

- **District-level DiD** (Table 1): In 2011 — forty years after peak containerisation — port districts still have employment rates **3.7pp lower**, manufacturing rates **4.7pp lower**, and transport rates **4.5pp lower** than non-port districts. Effects are persistent and statistically significant at every census from 1981 to 2011.
- **Worker-level DiD with matching** (Tables 6–7, panel b): After matching stevedores to observably-similar unskilled men, **no significant long-run disadvantage in individual labour-market outcomes (employment, unemployment, mortality)**. In 1981 stevedores were **6.8pp more likely to be employed** than matched controls (δ¹⁹⁸¹=0.068, SE=0.027) — direct evidence that NDLS job guarantees worked for the protected cohort.
- **Occupational stickiness → exit:** In 1981, stevedores 24.3pp more likely to stay in same occupation than matched controls (δ¹⁹⁸¹=0.243). By 1991 (post-NDLS abolition), this flips to -11.2pp (Table 8) — occupational churn concentrated at the exact moment employment protection ended.
- **No displacement-induced geographic mobility** (Table 8): Despite a 90% occupational collapse, stevedores exhibited *no* additional mobility relative to matched controls. Consistent with small geographic-mobility elasticity for less-skilled workers (Bound & Holzer 2000).

## Relevance to the Disruptions Map retrofit (v0.3)

### Confirms the containerisation case as "income-floor" buffering mode (not mode 2 reallocation, not mode 3 absorbing-employer)
- Mechanism: job guarantees + generous voluntary severance (NDLS 1947–1989) let the incumbent cohort age out; adoption proceeded via non-scheme ports (Felixstowe) outside the guarantee perimeter.
- Empirical test: δ¹⁹⁸¹ employment estimate is **significantly positive** (guarantees worked); δ¹⁹⁹¹ onward indistinguishable from zero (post-abolition, no residual protection advantage but also no disadvantage).

### Resolves key lag parameter for containerisation
- **Technology arrival:** First UK container ships 1966.
- **Peak-annual redundancy rate:** 1989–1992 for the incumbent cohort — a **23-year lag** between technology arrival and displacement of the protected cohort's employment.
- **Spatial displacement (non-protected populations):** 1966–1976, concentrated in East London — near-contemporaneous with adoption, 0–10 year lag.
- **Industry-wide cohort decline:** Smooth from 1961 through 2011, with steepest segment 1971–1991 (stevedores fell from 43k → 6k, -86%).

**Conclusion for parametric lag model:** The UK containerisation case exhibits **two distinct lag regimes within a single disruption** — a fast spatial/non-protected lag (~0–10 yr) and a slow protected-incumbent lag (~23 yr), set by institutional buffering mode. Single-number lag estimates collapse these two regimes. Candidate v0.3 model must support **bifurcated lags conditional on institutional buffering perimeter**.

### Structural caveat
- Paper's aggregate "no worse than controls" finding is control-group specific: unskilled men overall had very poor outcomes in 1980s–90s UK (Nickell & Bell 1995). Stevedores "fared no worse" means "were dragged down with the rest of the unskilled male workforce" — not "were insulated from the shock." Historical record of institutional buffering is **conditional on the counterfactual being bad**, not on the treatment being good. (Relevant for Layer 6 structural-optimism warning.)
