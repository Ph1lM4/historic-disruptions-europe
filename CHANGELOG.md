## [Unreleased] — Cross-case structured metrics rendered + findings deduped (2026-04-29 v0.2)

Closes the L3 render gap surfaced in Layer 6 scoping suite verification. The 2026-04-14 retrofit shipped 5 new top-level keys into `disruptions-data.json` (`structured_metrics`, `spreadsheets_counterfactual`, `incumbent_vs_cohort_displacement`, `capability_vs_adoption_gap`, `institutional_response_scope_statement`) — render scripts now display them.

**`/cases.html`:**
- All 20 case studies named and grouped by feasibility tier (7 high / 8 medium / 5 low)
- Inline structured metrics block per case with full 5 metrics for high-feasibility cases
- Medium-feasibility cases populated with values + uncertainty bands (v0.2 data ingestion)
- U-flag handling rule: U → hidden numeric + tooltip explaining unreliability; L → wide range; M → narrow range; H → point estimate
- Top-level explanation of "cross-case structured metric" concept + collapsible 5-metric legend per case

**`/findings.html`:**
- Three new sections: Spreadsheets Counterfactual (3 augmentation conditions + AI-application table + reinstatement/structural-bias warnings), Two Eras of Institutional Response (pre-1880 / post-1930), Methodological Appendix (full 20-row feasibility matrix)
- Counterfactual numbering bug fixed (previously rendered doubled numbers)
- Metric definitions legend now includes named categories (Time to 50% Task Displacement, Institutional Response Lag, Reskilling Adjacency, Geographic / Demographic Concentration, Peak Annual Displacement Rate)
- Spreadsheets / Two Eras / Methodological Appendix kept brief — full treatment in `/analysis.html` (canonical home; findings is summary + jump link)

**Methodology compliance:** every derived metric ships with `derivation_method` + `uncertainty_band` per BR-21 (Layer 6 framework requirement). 20×5 feasibility matrix published as methodological appendix.
