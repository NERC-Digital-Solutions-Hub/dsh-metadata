# Quality Assurance Report - Analysis of plant species recording bias in Countryside Survey terrestrial vegetation plots Ð summary report

## Background
- Purpose: ensure consistent botanical recording effort and skill across Countryside Survey (CS) field campaigns to prevent recording bias from affecting time-series indices.
- Methods historically used to reduce sensitivity to recording error: categorize less taxonomically demanding species, use cover data sparingly, aggregate by growth-form, omit bryophyte records.
- QA surveys (1990, 1998, 2007) compare CS field team data with independent expert records on subsets (QA plots); earlier results showed more species recorded by QA but no bias in species composition (via DCA) despite richness differences.

## QA 2007 survey results
- Noted decline in botanical recording quality in 2007, possibly due to reduced bryophyte recording rather than skill decline.
- Follow-up analyses (excluding bryophytes) examined:
  - Changes in species richness, composition (DCA axis scores), and mean Ellenberg scores on the triplicate dataset (plots surveyed in 1990, 1998, 2007).
  - Findings suggested small biases, with some indications of increasing differences between QA and CS over time and potential threshold effects in richness and Ellenberg scores.

## Follow-up actions triggered
- Independent statistician consulted; bias-correction factor approaches considered.
- New plant species database assembled from QA plots; all botanical indices recalculated.
- Triplicate QA dataset reanalyzed; 1990–1998–2007 reanalysis conducted; broader QA dataset analyzed with updated modelling.
- Investigations into whether biases could be explained by early CS surveys, botanist skill, timing differences, or plot-related factors, aiming to identify localized bias for exclusion criteria.

## Results (inspection and interpretation)
- QA analyses appeared sound, though methods documentation sometimes limited interpretability.
- Triplicate (1990–1998–2007) dataset showed larger differences in species richness than full 1998–2007 dataset, suggesting potential bias in the smaller subset.
- Development of bias-correction factors enabled estimates of average bias (CS minus QA) and SE for each survey year and index, with potential to derive bias-corrected means, SEs, and CIs for change analyses.

## Development of bias-correction factors
- Implemented statistical framework to estimate average bias per survey year and per botanical index.
- Framework supports deriving bias-corrected means, standard errors, and confidence intervals for analysis of change in plot indices.

## Analysis of QA/CS2007 data – explaining bias
- Earliness of CS survey was the only significant predictor of lower accuracy (CS vs QA) for individual plots; earlier surveys tended to have lower % accuracy.
- Plots subjected to QA tended to have slightly higher botanical skill than the overall CS2007 dataset.
- Bias appeared diffuse across the dataset rather than driven by a few outliers or individuals.

## Analysis of total QA dataset using statistical modelling
- Built a comprehensive QA dataset (1990, 1998, 2007 excluding bryophytes) and applied a mixed-effects model with survey square as a random effect.
- Differences in bias for species richness across surveys were not significant; some derived measures (e.g., Ellenberg scores) showed significant but small differences.
- Possible explanations include representativeness issues in matched triplicate data and averaging effects across plots.
- Bias-correction factors computed for all years and response variables.

## Conclusions
Draft recommendations (as per Scott et al.)
- 1) Exclude bryophytes from CS2007 analysis, as done previously. Implemented.
- 2) Do not adjust CS results to correct for CS–QA bias. Implemented.
- 3) For derived measures (potentially Ellenberg scores) consider adjusting 1990 results to account for inter-survey bias. Implemented.
- 4) Apply static adjustment to derived measure values before full analysis. Implemented.
- 5) If necessary, adjust standard errors for 1990 estimates post-analysis using computed corrections. Not implemented.
- 6) Incorporate lessons for future surveys on training, botanist recruitment, data quality vs. quantity, and plot recording QC.

## Annexes
- QA Plots 1, 2, 3.