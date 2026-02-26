# Notes on the downloadable data

- Confidentiality and representativeness
  - Precise locations of Countryside Survey (CS) squares are kept confidential by CEH.
  - External users cannot identify square locations with precision finer than 100 square km, limiting ability to determine if squares fall within defined areas.

## Sampling design and data structure
- CS field survey data are from a sample of 1 km squares across Great Britain.
- Each selected square is mapped and measured both at the square level and within-square (e.g., quadrats for vegetation, soils, etc.).
- Data types vary from binary to continuous measures.

## Stratified, non-random sampling
- The CS sample is not a random subset; it is stratified within designated strata.
- Land Classification classifications are country-specific:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Classifications have evolved (32 → 42 → 45 overall; separate classifications per country).

## Exclusions and representativeness
- Squares with more than 90% sea or more than 75% urban area were excluded from field survey.
- Official GB estimates are calculated using included squares; extrapolations assume excluded land is similar to included land. This introduces potential bias mainly in regions with high sea/urban square proportions, though the impact is typically small.

## Estimation methods
- Estimates are produced as ratio estimates for each land class, weighting by the vegetative land area within each class.
- Land-class estimates are combined using weights equal to the vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness concerns (Cochran, bootstrap references).

## Implications for analysis
- Analyses that ignore stratification and weighting may be unrepresentative or misstate variation.
- Proper handling requires accounting for the stratified design, area-based weights, and potentially bootstrap-derived uncertainty.

## References
- Barr, C.J. et al. Countryside Survey 1990 Main Report (1993)
- Cochran, W.G. Sampling Techniques (2nd ed., 1963)
- Efron, B. & Tibshirani, R.J. An Introduction to the Bootstrap (1993)