# QA and bias in vegetation recording

## Executive Summary
- QA analyses of Countryside Survey 2007 indicate potential under-recording of vegetation species compared with earlier surveys, influenced by the higher expertise of QA teams.
- Under-recording could bias assessments of change over time; cryptogams are particularly problematic and were poorly recorded in 2007.
- When cryptogams are removed, there is no significant difference in under-recording of species across surveys for the remaining data.
- Derived measures (e.g., Ellenberg scores) show bias that differs for 1990 compared with later surveys, suggesting time-dependent bias in these metrics.
- Recommendations:
  - Exclude cryptogams from CS2007 analyses (as in previous surveys).
  - Do not apply corrections for under-recording of other species.
  - Consider a static adjustment to 1990-derived measures (e.g., Ellenberg scores) to align with 1998 and 2007, if comparisons across years are required.
  - If adjustments are used, apply them prior to full analysis; post-analysis adjustments to standard errors could be considered if necessary.

## Background
- Quality assurance (QA) is a central element of CS vegetation monitoring, using independent experts to repeat recordings on a subset of plots to assess botanical accuracy.
- Historically, QA teams recorded more species than field surveyors, which is expected given their remit and expertise; this did not generally translate into differences in derived measures.
- The 2007 QA indicated a decline in recording quality relative to earlier surveys, largely due to cryptogams, prompting supplementary analyses.
- Supplementary analyses included:
  - Full 2007 QA dataset (cryptogams excluded).
  - A time-sequence dataset (1990, 1998, 2007) with plots recorded in all three years (matched triplicates), analyzed with and without cryptogams.
- Findings from analyses with cryptogams excluded show reduced differences between QA and field results; the matched triplicate dataset, while showing no significant differences after cryptogams exclusion, has lower statistical power due to smaller sample size.

## Analysis
### 2.1 Data and Statistical Methods
- Bias for each plot and year was computed as the difference between QA and CS values.
- A mixed-effects model (plot as unit, year as repeated measurement, square as random effect) estimated bias per year and changes across years; an alternative model assumed equal bias across years for comparison.

### 2.2 Species Richness Measures
- Bias is significant for all species richness measures except non-native richness; QA generally records more species than CS field teams.
- Magnitude of under-recording varies by group; grass richness showed a notable year-to-year difference, though this may not remain significant after multiple testing.
- Overall, there is little evidence that the level of under-recording changed systematically across survey years once cryptogams are excluded.

### 2.3 Derived Measures
- Most derived measures (e.g., Ellenberg indices) show significant bias, reflecting the link between species counts and derived metrics.
- Ellenberg light and radius were not significantly biased; others (e.g., Ellenberg fertility, pH, wetness, fertility) show time-related bias.
- Investigations suggest 1990 biases often differ from 1998/2007, while biases for 1998 and 2007 are more similar for several measures.
- A secondary analysis comparing 1990 versus 1998/2007 indicates six of seven derived measures differ in 1990, while C radius may not.

## Discussion, Conclusions and Recommendations
- There is demonstrable under-recording bias in CS vegetation monitoring, affecting derived measures such as Ellenberg indices.
- The differences in species richness are expected given QA vs field survey expertise and time pressures; QA results may not be directly comparable to those from broader-scale studies.
- Cryptogams recording is particularly problematic and its exclusion from analyses is justified; the unusually poor 2007 cryptogam recording requires ongoing attention.
- Differences in bias across surveys are chiefly a concern for derived measures; species richness measures show no consistent change in bias when cryptogams are excluded.
- Recommendations:
  - Exclude cryptogams from CS2007 analyses (consistent with prior surveys).
  - Do not adjust CS results to correct for CS vs QA bias in species richness measures.
  - For derived measures (likely Ellenberg scores), consider a static adjustment to 1990 results to account for bias differences with 1998/2007, using the proposed values (Table 3) if cross-year comparisons are needed.
  - Apply the adjustment to derived measures before full analysis; if needed, adjust standard errors post-analysis using the provided SEs and appropriate formulas.

## References
- Prosser, M. and Wallace, H. (2008a). Countryside Survey 2007 Quality Assurance Exercise. Ecological Surveys (Bangor).
- Prosser, M. and Wallace, H. (2008b). Countryside Survey 2007 Quality Assurance Exercise: Additional Analyses. Ecological Surveys (Bangor).
- Scott, W.A. and Hallam, C.J. (2003). Assessing species misidentification rates through quality assurance of vegetation monitoring. Plant Ecology.