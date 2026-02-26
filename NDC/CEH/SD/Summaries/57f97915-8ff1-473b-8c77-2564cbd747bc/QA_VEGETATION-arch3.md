# Quality Assurance Report - Analysis of plant species recording bias in Countryside Survey terrestrial vegetation plots Ð summary report

## Background
- Goal: ensure consistent recording effort and taxonomic skill to keep botanical indices representative of environmental signals (eutrophication, disturbance, succession).
- QA surveys compare CS field teams with independent experts on subsets of plots across 1990, 1998, and 2007.
- Findings across earlier QA rounds showed more species recorded by QA but no bias in species composition (via DCA), supporting use of the indices; challenges include data quality, metadata gaps, and the need for transparent data sharing.

## QA 2007 survey results
- 2007 QA indicated a decline in botanical recording quality, potentially due to reduced bryophyte recording.
- Follow-up analyses excluding bryophytes examined whether bias patterns changed when bryophytes were removed and across a triplicate dataset (1990, 1998, 2007).
- Key observations:
  - Tablet PC software errors were minor.
  - Increase in overlooked species in 2007 likely reflects surveyor effort rather than misidentification.
  - Ambiguity in whether mean differences between QA and CS (e.g., richness, Ellenberg N) changed over time; some evidence of a potential threshold effect.
  - Notable patterns: reduced CS recording of sedges in 2007 (QA +28% vs CS; 17% in 1998) and grasses (QA +17% vs CS; 6% in 1998).

## Actions triggered by follow-up work
- Independent statistician review and development of bias-correction factors based on QA/CS data.
- Creation of a bryophyte-excluded QA plot database and re-calculation of botanical indices in preparation for validation and bias correction.
- Re-analysis of triplicate QA data (1990, 1998, 2007) and broader QA data with new modelling.
- Investigations into potential sources of bias (earliness of CS survey, botanist skill, timing between CS and QA visits) to assess if exclusion of certain plots is warranted.

## Results
- QA analysis appears sound, though some methodological reporting was insufficient for full replication.
- Triplicate subset suggested larger apparent differences in richness than seen in full QA data, indicating possible bias in the smaller subset.
- Development of a formal bias-correction framework:
  - Estimates average bias (CS minus QA) and its standard error for each survey and botanical index.
  - Enables bias-corrected means, standard errors, and confidence intervals for change analyses.
- Factors explaining bias:
  - Early CS surveys tended to have lower accuracy relative to QA; overall CS2007 plots showed higher average botanical skill.
  - Bias appears diffuse across the dataset rather than driven by a few outliers.
- Modelling across the full QA dataset (excluding bryophytes) with a mixed-effects model found:
  - Differences in bias levels for richness across surveys were not significant.
  - Some differences for derived measures (e.g., Ellenberg scores) were significant but small.
  - Reasons for variance include representativeness of matched QA/CS triplets and averaging effects over plots.
- Conclusion: bias correction factors were computed for all years and response variables; overall, substantial adjustments to core indices were not deemed necessary, but adjustments for specific derived measures (notably 1990 Ellenberg scores) were considered.

## Conclusions
- Recommendations (draft):
  1) Exclude bryophytes from CS2007 analyses (implemented).
  2) Do not adjust CS results to correct for CS–QA bias in general (implemented).
  3) For derived measures (potentially Ellenberg scores), apply a static adjustment to 1990 values to align with other surveys (implemented).
  4) Implement static adjustments to derived measures before full analysis (implemented).
  5) Consider post-analysis adjustment of standard errors for 1990 using the correction factors (not implemented).
  6) Document and apply lessons for future surveys on training, recruitment, data quality vs. quantity, and plot recording QC.

## Annexes
- Annexes: QA Plots 1, QA Plots 2, QA Plots 3.