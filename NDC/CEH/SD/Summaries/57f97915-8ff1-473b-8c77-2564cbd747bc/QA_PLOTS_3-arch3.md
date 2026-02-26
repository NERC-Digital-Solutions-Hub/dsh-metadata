# QA and bias in vegetation recording

## Executive Summary
- Analyses of Countryside Survey (CS) 2007 QA data indicate possible increased under-recording of vegetation species compared with previous surveys, likely due to the higher expertise of QA staff.
- Recording of cryptogams is particularly problematic and was substantially worse in 2007, contributing to observed differences in species richness.
- When cryptogams are removed from the data, models show no significant differences in under-recording bias across the three surveys for most species richness measures.
- For derived measures (e.g., Ellenberg scores), there is evidence that bias differed between 1990 and later surveys, though 1990 vs 1998/2007 is the key contrast.
- Recommendations:
  - Exclude cryptogams from CS2007 analyses, as with previous surveys.
  - Do not adjust CS results to correct for bias between CS and QA for general measures.
  - For derived measures (likely Ellenberg scores), adjust 1990 values to account for differences in bias relative to later surveys, using the provided difference values.
  - Apply a static adjustment to derived measure values before full analysis; consider post-analysis SE adjustments if necessary.

## 1. Background
- Quality assurance is a core element of major vegetation monitoring, with independent QA teams conducting repeat recordings to assess botanical accuracy.
- Historically, QA results show more species than CS field teams, which is expected given QA's expertise and remit.
- Previously, differences in the number of species did not translate into significant differences in derived measures (e.g., DCA-based metrics).
- The 2007 QA report suggested a decline in recording quality relative to earlier surveys, partly due to cryptogams, leading to larger richness differences.
- Cryptogams have long been known to be difficult to record, and analyses prior to 2007 typically exclude them.

## 2. Analysis
- Approach: compare bias between QA and CS recordings at the plot level across years, using differences (QA minus CS) and mixed models with plot as the unit and survey year as repeated measures.

### 2.1 Data and methods
- Most QA plots were recorded by both QA and CS teams across years; a few plots varied by year.
- Bias per plot per year was modeled directly; a mixed model with year as a repeated measure and square as a random effect was used.
- A supplementary model assumed equal bias across years to maximize power and use all data.

### 2.2 Species richness measures
- Across measures, there is clear and significant bias: QA and CS field crews differ, with QA recording more species.
- The magnitude of bias varied by measure and plot, reflecting differing likelihoods of missing species.
- When testing for change over time, little evidence suggests the extent of under-recording changed significantly for most measures; only grass richness showed a marginal year effect (p = 0.045) before correction for multiple testing.

### 2.3 Derived measures
- For derived measures (e.g., Ellenberg indices, R radii), most showed significant bias, indicating that differences in species recording translate into differences in derived properties.
- The pattern differed from species richness: few measures showed significant time-based changes in bias, but 1990 often differed from 1998/2007.
- A targeted analysis allowing 1990 bias to differ from 1998/2007 revealed that six of seven derived measures showed significant differences between 1990 and later surveys; one (C radius) did not.

## 3. Discussion, Conclusions and Recommendations
- There is measurable under-recording in CS vegetation monitoring, which affects derived measures such as Ellenberg indices.
- The bias in species richness is expected and not a cause for concern regarding CS trend interpretation, given QA’s expertise and timing pressures on CS field teams.
- Cryptogams' poor recording in 2007 is a longstanding issue; exclusion from analyses remains warranted.
- Differences in bias across surveys are more concerning for derived measures; 1990 shows distinct bias relative to later years.
- Recommendations:
  1) Exclude cryptogams from CS2007 analyses, as with prior surveys.
  2) Do not adjust CS results to correct for CS–QA bias in general.
  3) For derived measures (likely Ellenberg), adjust the 1990 values to account for bias differences relative to 1998/2007, using the differences outlined in the report.
  4) Apply a static adjustment to derived measure values prior to full analysis.
  5) If needed, adjust the standard errors of 1990 estimates post-analysis using the reported SEs and standard-error-sum formulas.

## 4. References
- Prosser, M. and Wallace, H. (2008a). Countryside Survey 2007 Quality Assurance Exercise. Ecological Surveys (Bangor).
- Prosser, M. and Wallace, H. (2008b). Countryside Survey 2007 Quality Assurance Exercise: Additional Analyses. Ecological Surveys (Bangor).
- Scott, W.A. and Hallam, C.J. (2003). Assessing species misidentification rates through quality assurance of vegetation monitoring. Plant Ecology.