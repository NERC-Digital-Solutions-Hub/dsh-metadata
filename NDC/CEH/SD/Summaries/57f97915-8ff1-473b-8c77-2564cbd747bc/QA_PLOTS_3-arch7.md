# QA and bias in vegetation recording

## Executive Summary
- Independent QA recorded more vegetation species than Countryside Survey (CS) field teams, suggesting under-recording by CS staff that could bias change estimates.
- Recording of cryptogams is notoriously difficult; in CS2007 cryptogams recording is substantially worse, leading to potential bias if analyzed.
- After excluding cryptogams, statistical modelling shows no significant differences in species richness bias across CS1990, CS1998, and CS2007.
- Derived measures (e.g., Ellenberg scores) show bias that varies across surveys, with notable differences between CS1990 and later surveys.
- Recommendations:
  - Exclude cryptogams from CS2007 analyses, as in previous surveys.
  - Do not apply general corrections for under-recording of other species.
  - If needed, adjust derived measures (primarily Ellenberg scores) to account for 1990 bias differences using the provided values (static adjustment before analysis; possible post-analysis SE adjustment).

## Background
- QA (Quality Assurance) is an ongoing element of Countryside Survey vegetation recording; independent experts repeat plot recordings and compare to CS field teams to gauge accuracy.
- Historically, QA reports show more species than CS field teams, reflecting expertise differences; differences in species counts did not translate into major changes in derived composition metrics in earlier surveys.
- 2007 QA suggested a decline in botanic recording quality, largely due to cryptogams, which affects species richness counts and subsequent derived measures.
- Supplementary analyses separated: (1) full 2007 QA dataset with cryptogams excluded; (2) time-sequence analysis on a small matched triplicate dataset (1990, 1998, 2007) excluding cryptogams.
- Key finding: matched triplicate data show no significant QA vs CS differences for all years once cryptogams are excluded, but the smaller sample size reduces statistical power.

## Analysis

### Data and Methods
- Bias per plot was calculated as the difference between QA and CS values for each year.
- A mixed model with plot as the unit, square as a random effect, and year as the repeated measure estimated bias in each year and changes across years.
- A model with equal bias across years provided a combined view and increased power.

### Species Richness Measures
- Most richness measures show a clear and significant bias: CS under-records more species than QA.
- Magnitude of bias varies by group; under-recording is not limited to a narrow subset of species groups.
- Temporal change in bias is not strongly supported; only grass richness showed a marginal year-to-year difference (p ≈ 0.045), which would not hold after correcting for multiple tests.

### Derived Measures
- Derived metrics (e.g., Ellenberg scores, radius measures) also show bias, with many measures affected.
- Unlike species richness counts, some derived measures show time-related changes in bias; in particular, several Ellenberg indices differed in CS1990 compared with CS1998/CS2007.
- A further model suggests that 1990 biases differ from later years for multiple derived measures, while 1998 and 2007 biases are more similar for some metrics (though not all).
- For Ellenberg and other derived metrics, several measures show significant bias differences, and others show non-significant trends.

## Discussion, Conclusions and Recommendations

### Conclusions
- There is a measurable under-recording bias in CS vegetation monitoring relative to QA, affecting measures derived from species composition (e.g., Ellenberg indices).
- Species richness differences themselves are not a major concern for change detection, given QA expertise and the exclusion of cryptogams in analyses.
- Cryptogams present a substantial recording challenge; excluding them remains the recommended practice to avoid bias.
- Differences in biases across surveys, especially for derived measures, can affect cross-year comparisons if not addressed.

### Recommendations
- Cryptogams: Exclude cryptogams from the CS2007 dataset, as done in previous surveys.
- Corrections for under-recording: Do not apply blanket corrections to CS results to account for CS vs QA biases in species richness.
- Derived measures adjustments: If cross-year comparability is required for derived measures (notably Ellenberg scores), apply a static adjustment to 1990 results to align with 1998/2007 biases using the values given in Table 3.
- Adjustment implementation: Apply the static adjustment to derived measures before full analysis; if desired, adjust the standard errors for 1990 estimates post-analysis using Table 3 SEs and standard-error propagation formulas.
- Documentation: Clearly document the cryptogam exclusion and any adjustments to derived measures when producing map-based products, ensuring users understand potential cross-year biases.

References (core sources)
- Prosser, M. and Wallace, H. (2008a). Countryside Survey 2007 Quality Assurance Exercise. Ecological Surveys (Bangor).
- Prosser, M. and Wallace, H. (2008b). Countryside Survey 2007 Quality Assurance Exercise: Additional Analyses. Ecological Surveys (Bangor).
- Scott, W.A. and Hallam, C.J. (2003). Assessing species misidentification rates through quality assurance of vegetation monitoring. Plant Ecology.