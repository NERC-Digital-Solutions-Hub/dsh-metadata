# Quality Assurance Report - Analysis of plant species recording bias in Countryside Survey terrestrial vegetation plots Ð summary report

## Overview
- Examines recording bias in Countryside Survey botanical data across 1990, 1998, and 2007.
- Focuses on ensuring time-series integrity by separating true ecological signal from changes due to recording effort and expertise.
- Led to development of bias-correction factors and data-processing steps to improve reliability of derived botanical indices.

## Background
- Consistent recording effort and identification skill are crucial for valid time-series indices.
- QA surveys compare field teams to independent experts on a subset of plots to assess recording quality.
- Past QA found more species recorded by QA than CS, but no bias in species composition; 2007 suggested a decline in recording quality, potentially linked to reduced bryophyte recording.

## Data and Methods
- QA surveys conducted in 1990, 1998, and 2007; bryophytes often poorly censused and were treated differently across surveys.
- Analyses repeated after excluding bryophytes to test bias trends; used a matched triplicate dataset (plots surveyed in all three years) and a full QA dataset.
- Derived indices include species richness, mean Ellenberg N scores, and DCA axis scores.
- Statistical approach included mixed-effects modelling (survey square as random effect) and derivation of bias-correction factors.
- Created a new combined QA plot database (excluding bryophytes) and recalculated indices for validation.

## Findings (Key Points)
- 2007 QA results suggested a decline in recording quality, likely due to less comprehensive bryophyte recording; omitting bryophytes clarified trends.
- Within the triplicate dataset, differences in species richness and Ellenberg N between CS and QA were possible but small; some results suggested a threshold where bias differences could increase over time, but overall effects were modest.
- Specific taxa showed notable differences when CS vs QA were compared in 2007 (sedges and grasses were under-recorded by CS compared with QA), indicating localized under-sampling in some groups.
- The primary driver of accuracy variation across plots was the earliness of the CS survey; early surveys tended to have lower CS accuracy relative to QA, though the worst plots were associated with the best botanists, suggesting diffuse rather than unitary bias sources.
- Bias appeared to be a diffuse dataset-wide issue rather than concentrated in a small number of plots or individuals.
- Re-analysis with the full QA dataset and new modelling showed:
  - Differences in bias for species richness across surveys were not significant.
  - Differences for some derived measures (e.g., Ellenberg scores) were statistically significant but of small magnitude.
  - Reasons for discrepancies included representativeness of the matched triplicate subset and averaging effects when censusing varied by plot type.
- Bias-correction factors were computed for all survey years and response variables.

## Actions Taken
- Involve independent statistician to review QA results; plan bias-correction methodology.
- Assemble QA plots into a unified database; re-calculate all botanical indices for validation.
- Re-analyze triplicate and full QA data using new modelling approach.
- Investigate potential drivers (survey timing, botanist skill level, visit timing) to determine if plot exclusion is appropriate.
- Develop bias-correction factors and apply them where appropriate.

## Data Products / Bias Correction
- Developed an approach to estimate average bias (CS minus QA) and its standard error for each survey and index.
- Possible bias-corrected estimates, confidence intervals, and standard-errors adjustments prepared for derived measures.
- Bias-correction factors computed for all years and indices; potential static adjustments identified (notably for 1990 Ellenberg-derived measures).
- Implementations:
  - Bryophytes excluded from analyses (as in prior surveys).
  - No general adjustment to CS results to correct for CS–QA bias (policy implemented).
  - For derived measures, a static adjustment to 1990 values recommended (and implemented) prior to full analysis.
  - Post-analysis SE adjustments for 1990 estimates possible but not implemented.

## Conclusions and Recommendations
- Bryophytes should continue to be excluded from CS2007 analyses (and previous surveys) to maintain consistency.
- No broad bias adjustment applied to CS results relative to QA results; outputs should be treated with caution for derived measures.
- For derived measures (potentially Ellenberg scores), consider a static adjustment to 1990 values to harmonize across surveys; implemented.
- If needed, adjust standard errors for 1990 estimates using computed correction factors and their SEs (not yet implemented).
- Future survey design should incorporate clear training, recruitment, data quality versus quantity considerations, and QC of plot recording to minimize bias in time-series data.

## Annexes
- Annexes detail QA Plots and supplementary materials used in analyses.