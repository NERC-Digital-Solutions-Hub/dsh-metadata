# QA and bias in vegetation recording

## Executive summary
- Quality assurance (QA) in Countryside Survey (CS) 2007 shows under-recording of vegetation species by CS field teams compared with QA specialists.
- Cryptogams (mosses, liverworts, fungi) are particularly poorly recorded in 2007; excluding cryptogams reduces but does not eliminate differences between QA and field teams.
- After cryptogams are excluded, there is no significant change in bias for species richness across CS years; however, derived measures (e.g., Ellenberg scores) show bias differences between 1990 and later surveys.
- Recommendations:
  - Exclude cryptogams from CS2007 analyses (as in prior surveys).
  - Do not adjust CS results to correct for general CS–QA under-recording for most outputs.
  - For derived measures (primarily Ellenberg scores), consider a static adjustment to 1990 results to account for bias differences relative to later surveys, using values in the provided table.
  - Apply any adjustment to derived measures before full analysis; adjustments to standard errors of 1990 estimates can be considered post-analysis if needed.

## Background
- QA is used to assess the validity of vegetation findings by having independent experts repeat a subset of plots and compare with CS field teams.
- Historically, QA records more species than CS teams; differences in species counts did not translate into significant differences in derived measures.
- QA2007 suggested a decline in recording quality, largely due to cryptogams; previous CS analyses excluded cryptogams due to identification difficulties.
- Supplementary analyses (full dataset with cryptogams excluded; and a reduced “matched triplicate” dataset) show:
  - Full QA dataset: CS field teams still under-record beyond cryptogams, though the gap narrows when cryptogams are removed.
  - Matched triplicate dataset: no significant QA–field differences once cryptogams are excluded, but smaller sample size reduces statistical power.

## Analysis

### Data and statistical methods
- QA plots overlapped closely with CS plots; bias estimated as the difference QA minus CS for each plot and year.
- A mixed-effects model (square as random effect; plots as units; year as repeated measure) estimated bias per year and changes over time.
- A model assuming equal bias across years was also used to maximize power and account for non-independence among plots within squares.

### Species richness measures
- Most species richness measures show significant bias (QA records more species than CS) except non-native richness.
- The magnitude of bias varies by group (larger differences for many groups due to higher likelihood of overlooking species).
- Little evidence that bias magnitude changes over time; only grass richness showed a marginal year effect (but not robust after multiple testing correction).

### Derived measures
- Derived measures (e.g., Ellenberg indices, R radius, C radius, etc.) also show bias, with Ellenberg light and R radius often non-significant, but several indices showing significant bias.
- Time-related changes: most derived measures indicate that CS1990 bias differed from later surveys (1998/2007) for several measures; CS1990 consistently differed in multiple derived indices.
- When testing 1990 vs 1998/2007 jointly, six of seven derived measures showed significant bias differences; one (C radius) did not.
- Tabled adjustments suggest a static difference between 1990 and later surveys for derived measures; applying a uniform adjustment to 1990 data is suggested if derived measures are used for cross-year comparisons.

## Discussion, conclusions and recommendations
- There is persistent under-recording in CS vegetation monitoring, which affects both species counts and derived measures like Ellenberg scores.
- QA experts’ performance is expected to exceed CS field surveyors due to expertise and time pressure; thus differences reflect method rather than a flaw in CS data alone.
- Cryptogams’ poor recording confirms the need to exclude them from published analyses, as done in previous CS reports.
- Implications for long-term change detection: since bias in species richness is relatively stable across surveys (after cryptogams exclusion), change assessments remain robust for raw richness; however, derived measures may be biased, especially with respect to historical baselines (1990).
- Recommendations:
  1) Exclude cryptogams from CS2007 analyses (maintained).
  2) Do not adjust CS results to correct for general CS–QA bias for most outputs.
  3) For derived measures (primarily Ellenberg scores), adjust 1990 results to account for bias differences relative to 1998/2007, using the differences outlined in Table 3.
  4) Implement the adjustment as a static pre-analysis correction for derived measures.
  5) If necessary, adjust the standard errors of 1990 estimates post-analysis using the provided standard errors and standard-sum variance formulas.

## References
- Prosser, M. and Wallace, H. (2008a). Countryside Survey 2007 Quality Assurance Exercise. Ecological Surveys (Bangor).
- Prosser, M. and Wallace, H. (2008b). Countryside Survey 2007 Quality Assurance Exercise: Additional Analyses. Ecological Surveys (Bangor).
- Scott, W.A. and Hallam, C.J. (2003). Assessing species misidentification rates through quality assurance of vegetation monitoring. Plant Ecology, 165(1):101-115.