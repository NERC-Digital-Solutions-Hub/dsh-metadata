# Notes on the downloadable data

- Privacy: precise locations of CS survey squares are kept confidential by CEH; external users cannot identify whether squares fall within defined areas more precise than 100 square km.
- Data scope: Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at two levels—square level and within-square features.
- Data types: measurements range from binary (yes/no) to continuous (areas, lengths), collected via mapped squares and quadrats for vegetation, soils, etc.
- Sampling design and representativeness:
  - The CS sample is not a random subset of all GB squares; it is stratified by Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16).
  - Sampling classifications have evolved (32 → 42 → 45 classes) to accommodate separate country reporting.
  - Some squares are excluded from field survey: those with more than 90% sea area or more than 75% urban area on 1:250,000 OS maps.
  - Official GB estimates assume that vegetative land in excluded squares is similar to that in sampled squares; bias is generally small except in regions with high sea/urban square proportions.
- Estimation approach:
  - Estimates are produced as ratio estimates by land class, using the vegetative land area of each class as weights.
  - Standard errors and confidence intervals are calculated via bootstrap methods from 1998 onward due to skewness in some features.
- References for methodology:
  - Barr et al. 1993; Countryside Survey 1990 Main Report.
  - Cochran 1963; Sampling Techniques (2nd ed.).
  - Efron & Tibshirani 1993; An Introduction to the Bootstrap.

## Sampling Considerations in the use of Countryside Survey Data

- Two-level sampling: analyses should consider both the whole square and within-square measurements to properly characterize features.
- Stratification: analyses must account for Land Classification strata and country-specific classifications to avoid biased inferences.
- Representativeness and extrapolation:
  - Estimates pertain to GB squares meeting inclusion criteria and may not generalize to excluded sea/urban-dominated regions.
  - When combining data across land classes or regions, apply the appropriate area-based weights.
- Precision and uncertainty:
  - Use bootstrap-derived standard errors and confidence intervals as provided or computed with the stratified design in mind.
- Practical guidance:
  - Verify the alignment between the analysis units (squares, within-square features) and the study question.
  - Be cautious about interpreting outputs without accounting for the sampling design and weighting.
  - When communicating results, note the representativeness limitations due to the sampling framework and exclusions.