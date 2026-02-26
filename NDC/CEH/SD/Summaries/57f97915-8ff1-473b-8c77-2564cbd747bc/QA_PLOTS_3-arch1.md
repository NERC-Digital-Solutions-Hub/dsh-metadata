# QA and bias in vegetation recording

## Executive summary
- Analyses of Countryside Survey 2007 quality assurance (QA) data indicate a possible increase in under-recording of vegetation species relative to previous surveys, linked to QA team expertise and cryptogams recording difficulties.
- Under-recording bias could bias estimates of change over time in vegetation, so understanding its level is crucial.
- Cryptogams recording is substantially poorer in CS2007 and has been excluded from analyses in CS surveys; this exclusion is recommended for consistency.
- After excluding cryptogams, there is no significant difference in under-recording of species across surveys for species richness measures.
- Derived measures (e.g., Ellenberg scores) show biases that differ across surveys, notably between CS1990 and later surveys.
- Recommendations:
  - Exclude cryptogams from CS2007 analysis (as in previous surveys).
  - Do not apply corrections for under-recording of other species between CS and QA results.
  - Consider a one-off adjustment to CS1990 derived measures (e.g., Ellenberg indices) to account for bias differences with later surveys, using values from Table 3.
  - Apply the adjustment as a static pre-analysis correction; and if needed, adjust standard errors post-analysis using Table 3.

## 1. Background
- QA is used to assess the validity of vegetation monitoring; independent QA teams record plots to compare with CS field teams.
- Historically, QA records more species than CS field teams, which is expected given expertise and remit. Differences in raw species counts did not translate to differences in derived measures like DCA.
- QA2007 suggested reduced recording quality and larger gaps between QA and field teams, largely driven by cryptogams recording difficulties.
- Cryptogams have been excluded from published CS analyses due to identification challenges.
- Supplementary analyses (Prosser & Wallace 2008b) examined full 2007 QA data with cryptogams excluded and a matched triplicate dataset (1990, 1998, 2007) with cryptogams excluded; results differed in the full dataset but aligned more closely in the smaller matched set.
- This report presents further analyses using the full QA dataset (three surveys, cryptogams excluded) to rectify previous comparisons, and discusses implications for analyses of CS2007 data.

## 2. Analysis
### 2.1 Data and statistical methods
- Most QA plots were recorded by both QA and CS teams; bias per plot was computed as QA value minus CS value.
- A mixed-effects model was used: year as repeated measures, plot as the unit, square as a random effect; another model assumed equal bias across all three years to increase power and account for non-independence within squares.
- The aim was to estimate year-specific biases and to test whether bias levels differed across surveys.

### 2.2 Species richness measures
- Across all richness measures, there was a clear and significant bias: QA records more species than CS, with variability in the magnitude of bias depending on the group (e.g., non-native richness showed less or no bias).
- There was little evidence that the extent of under-recording changed over time, with the exception of grass richness (p ≈ 0.045, but significance would not survive adjustment for multiple testing).
- Overall, excluding cryptogams reduces the apparent difference between QA and CS but does not eliminate it for all measures; grass richness showed a potential time-related bias, though the statistical significance is marginal after correction.

### 2.3 Derived measures
- Derived measures (e.g., Ellenberg indices) also showed significant bias for most measures; Ellenberg light and radius were exceptions in terms of significant bias.
- Unlike species richness, there is some evidence that the bias size changed over time for Ellenberg scores; notably, biases for CS1990 differed from CS1998 and CS2007 for several derived measures.
- A model assuming equal bias for 1998 and 2007 (and allowing 1990 bias to differ) indicates:
  - Six of seven derived measures show a significant difference between 1990 and later surveys.
  - Only C radius did not show a significant year effect.
- Table 3 (equal 1998/2007 bias) demonstrates that the 1998 and 2007 biases are similar, while 1990 biases differ, suggesting a potential static adjustment only for the 1990 values.
- A static adjustment to 1990 derived measures (before full analysis) could align 1990 values with later surveys; errors could be adjusted post-hoc if needed using Table 3 SEs.

## 3. Discussion, conclusions and recommendations
- There is a demonstrable under-recording of species in CS vegetation monitoring, which propagates into biases in derived measures such as Ellenberg scores.
- The level of bias in species richness measures does not show a significant time trend once cryptogams are excluded, implying that trend analyses for richness remain robust (within the limitations of residual bias).
- Cryptogams recording is notably poorer in 2007; exclusion of cryptogams from analyses is warranted to avoid spurious changes.
- Differences in bias for derived measures are concentrated around the 1990 survey; 1998 and 2007 biases are more consistent with each other.
- Recommendations:
  1) Exclude cryptogams from the CS2007 data analysis (as in previous surveys).
  2) Do not adjust CS results to correct for CS–QA bias in general for species counts.
  3) For derived measures (especially Ellenberg indices), consider a static adjustment to CS1990 values to account for differences relative to 1998/2007, using the differences summarized in Table 3.
  4) Apply the adjustment to derived measures prior to full analysis (static adjustment).
  5) If necessary, adjust the standard errors of the 1990 estimates post-analysis using Table 3 standard errors and the formulae for the standard error of a sum of variables.

## 4. References
- Prosser, M. and Wallace, H. (2008a). Countryside Survey 2007 Quality Assurance Exercise. Ecological Surveys (Bangor).
- Prosser, M. and Wallace, H. (2008b). Countryside Survey 2007 Quality Assurance Exercise: Additional Analyses. Ecological Surveys (Bangor).
- Scott, W.A. and Hallam, C.J. (2003). Assessing species misidentification rates through quality assurance of vegetation monitoring. Plant Ecology, 165(1): 101-115.