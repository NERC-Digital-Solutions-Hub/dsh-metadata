# Notes on the downloadable data

## Key purpose and confidentiality
- The document describes Countryside Survey (CS) field survey data and how to use them responsibly in analyses and policy evaluation.
- Precise locations of CS survey squares are kept confidential to protect representativeness; external users cannot identify squares with precision finer than 100 square km.

## Sampling design and structure
- Data come from a sample of 1 km squares across GB, with measurements at two levels: the square level and within-square features.
- Sampling is not a random subset; it is a stratified sample defined by the ITE Land Classification.
- Land Classification details:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- The Land Classification has evolved (32 → 42 → 45 classes) due to country-specific reporting needs; each country effectively has its own classification.

## Representativeness and limitations
- Estimates without accounting for stratification may be unrepresentative and have inaccurate variation estimates.
- Not all GB squares were surveyed: squares with >90% sea or >75% urban area were excluded from field surveys.
- General GB estimates assume excluded squares have vegetative land composition similar to sampled squares; this assumption may introduce bias, particularly in regions with high sea/urban square proportions.

## Estimation methodology
- Official GB estimates are produced using ratio estimation by land class, weighting by the vegetative land area in each class.
- Because some features are skewed, standard errors and confidence intervals have been estimated using bootstrap methods since 1998 (Efron and Tibshirani).

## Data governance, metadata and accessibility considerations
- The need to preserve data confidentiality and the complexity of the stratified design imply careful handling of metadata and sampling frames for reuse.
- Where data are reused or shared, ya need to respect the confidentiality constraints and account for the stratified sampling in analysis and interpretation.

## Practical implications for analysts and policymakers
- When using CS data in monitoring frameworks, incorporate:
  - Stratification by land class and country-specific classifications
  - Weights based on vegetative land area
  - Bootstrap-based uncertainty measures for robust inference
- Be cautious about extrapolating from included squares to larger regions or the entire GB, especially in areas with many excluded squares.
- Ensure transparent reporting of data provenance, sampling design, and any assumptions used to fill gaps or adjust for missing data.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.