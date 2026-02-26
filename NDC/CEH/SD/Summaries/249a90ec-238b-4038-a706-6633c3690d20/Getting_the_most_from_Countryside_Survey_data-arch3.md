# Notes on the downloadable data

## Key points
- Location privacy: precise locations of Countryside Survey (CS) field squares are kept confidential; external users cannot identify squares to better than 100 square km, preserving representativeness.
- Data and sampling structure: CS data come from a sample of 1 km squares in Great Britain, with two levels of measurement (whole square characteristics and within-square features) and varied variable types from binary to continuous.
- Non-random, stratified sampling: the sample is stratified by ITE Land Classification, with country-specific class counts (England: 21, Wales: 8, Scotland: 16). Analyses that ignore stratification may yield unrepresentative estimates and incorrect variation.
- Excluded squares and potential bias: squares with >90% sea or >75% urban area were excluded from field surveys; official GB estimates assume excluded squares are similar in vegetative land composition to sampled squares, with bias generally negligible except in regions with many sea/urban squares.
- Estimation approach: official estimates use ratio estimates by land class, weighted by vegetative land area. Since 1998, standard errors and confidence intervals are estimated via bootstrap due to skewness in some features.
- Data provenance and references: foundational guidance comes from Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) on sampling techniques; Efron & Tibshirani (1993) on the bootstrap.

## Methodological notes for monitoring frameworks
- Account for stratification by Land Classification when analyzing CS data; do not treat the sample as random across GB.
- Apply ratio estimation by land class with area-based weights to derive representative GB or regional estimates.
- Use bootstrap methods to quantify uncertainty, especially for skewed features.
- Be mindful of exclusions (sea/urban areas) and their potential regional impact on representativeness; document and justify any extrapolations.
- Ensure metadata and data governance considerations are addressed when sharing datasets, given confidentiality and provenance constraints.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.