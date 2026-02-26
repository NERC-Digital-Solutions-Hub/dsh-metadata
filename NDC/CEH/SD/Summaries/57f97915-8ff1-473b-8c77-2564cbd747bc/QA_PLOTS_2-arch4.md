# Countryside Survey 2007: Quality Assurance Exercise. Appendix

- Purpose and scope
  - Assess whether variation in CS2007 surveyors’ species records introduced bias into the dataset.
  - Compare CS2007 surveyors with QA2017 assessors using two data sets: Full QA2007 (532 samples across 266 plots) and Matched Triplicate (108 plots common to 1990, 1998 and 2007 QA exercises).
  - Use presence/absence data and remove cryptogams to improve comparability with historical analyses; analyse with multivariate methods and Ellenberg indicators.

- Data modifications and methods
  - Cryptogams (mosses, liverworts, lichens) eliminated for comparability.
  - Data converted to presence/absence prior to multivariate analyses to reduce cover-variation effects.
  - Analyses include:
    - Species richness comparisons by plot type and landscape class (paired t-tests, ANOVA, Tukey tests).
    - Multivariate ordination (DCA) on full QA2007 data and on the Matched Triplicate data.
    - Ellenberg indicator values (Light, Fertility, Moisture) calculated per quadrat and linked to axis scores.
    - Repeat measures ANOVA and Wilcoxon tests to detect surveyor vs time effects and differences between CS and QA.

- Key findings: overall richness and bias
  - After cryptogams removal, CS2007 records still show lower species richness than QA2007 in most plot types; overall shortfall about 13% (CS2007 vs QA2007), though not accounting for record accuracy.
  - Land-class differences persist: upland squares more under-recorded than lowland plots with cryptogams removed; hedge and arable plots show notable discrepancies.
  - Individual land classes show significant under-recording by CS2007 across several categories (e.g., some plots and classes with p-values < 0.01 for CS vs QA comparisons).

- Matched Triplicate data: changes over time and proxy biases
  - Including cryptogams: significant differences across six surveys (1990, 1998, 2007 CS and QA) with p < 0.001.
  - Excluding cryptogams: CS2007 shows declines in several groups compared to 1998 and 1990 (e.g., grasses show ~10% lower recording by CS2007; sedges show a modest decline; woody species increase in both CS and QA since 1998).
  - Grass and sedge recording gaps suggest CS2007 under-recording relative to the 1998 level; Juncaceae shows mixed patterns; forbs account for roughly half of all records and show a general decline in CS after 1998.
  - Sphagna (a cryptogam group) remain poorly recorded by CS2007 relative to QA, though correct group allocation is high when recorded.
  - Wolf-like trend: CS2007 tends to record fewer grasses and sedges than would be expected if 1998 levels were maintained; overall declines are influenced by plot type and surveyor; QA records generally remain higher than CS records, but the gap narrows in some plot types.

- Plot-type and landscape-specific patterns
  - X-plots (arable-like): CS under-recording persists; significant CS vs QA differences over time.
  - Y-plots, hedge, stream, verge, boundary plots: declines in CS records over time; QA often shows less pronounced declines or different trajectories.
  - Hedge and stream plots show notable between-year differences; verges and boundaries show mixed but generally decreasing richness in CS2007 relative to QA.
  - Lowland vs upland: upland squares show stronger differences and time-related declines in CS, while lowland patterns are closer to QA in some years but still show gaps.

- Ordination and Ellenberg indicators
  - DCA axis analysis indicates Axis 1 is strongly related to Fertility (Ellenberg N) and shows a significant fertility-related gradient; Axis 2 relates to shade exposure; Axis 3 is less clear.
  - Across full and matched triplicate datasets, there are no strong directional biases between CS and QA on mean axis scores, though small differences exist (e.g., Axis 1 and Ellenberg N in some analyses show statistically significant but modest deviations).
  - Across the matched triplicate data, CS1990 to CS2007 changes appear exaggerated relative to QA1990 to QA2007, particularly for Axis 1 and Ellenberg N; there is evidence of increasing shade tolerance (Axis 2) over time.

- Epilogue: adjustment considerations (par scores)
  - Provisional adjustment estimates to reconcile CS2007 with CS1998 levels (cryptogams excluded):
    - Hedge plots: 0 additional species needed.
    - Boundary plots: ~0.3 more species per plot.
    - Stream plots: ~0.8 more species per plot.
    - Verge (Y) plots: ~1.9 more species per plot.
    - X and U plots: ~2.1 more species per plot.
  - These par scores are crude extrapolations based on matched-triplicate results and intended to guide calibration rather than precise corrections.

- Implications for data quality and governance
  - Systematic differences exist between CS surveyors and QA assessors, particularly in plot-type and landscape contexts; however, there is no strong directional bias across time in axis-related ordination results.
  - Cryptogams present persistent recording challenges; removal improves comparability but under-recording by CS2007 remains a concern.
  - Data collection protocols show time- and plot-type-dependent biases that should be documented in metadata and considered in trend analyses and policy-related interpretations.
  - The appendix provides a framework for quality assurance, including standardization of recording practices, presence/absence data usage, and explicit bias assessments across surveys and time.

- Practical takeaways for Data Leaders
  - When integrating multi-timepoint vegetation datasets, use presence/absence data and consider removing non-target taxa (cryptogams) for comparability.
  - Implement regular bias assessments between field surveyors and QA evaluators, stratified by plot type and landscape class.
  - Document and monitor data quality indicators (e.g., species richness per plot, group-specific recording rates, Ellenberg-related gradients) to detect systematic shifts over time.
  - Consider calibration or par-score adjustments for legacy comparisons and clearly communicate any inferred biases or corrections to stakeholders.
  - Maintain thorough metadata on survey methods, plot types, and terrain features to support cross-time and cross-surveyor comparisons.