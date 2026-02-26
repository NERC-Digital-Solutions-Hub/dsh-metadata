# Notes on the downloadable data

- Precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify squares with precision better than 100 square km.
- Consequently, you cannot determine whether any survey square falls within defined areas below this threshold.

## Sampling Considerations in the use of Countryside Survey Data

- The CS field survey data come from a sample of 1 km squares in GB, with measurements at two levels: the entire square and features within the square.
- Measurements include a mix of binary (yes/no) and continuous variables (areas, lengths, etc.).
- The CS sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification. Country-specific classifications have evolved:
  - Originally 32 classes
  - 1998: 42 classes (Scotland reporting necessitated changes)
  - 2007: 45 classes (Wales reporting changes)
  - England: 21 classes, Wales: 8, Scotland: 16
- Analyses that ignore stratification may yield non-representative estimates and incorrect estimates of variation.
- Some squares were excluded from field survey:
  - Exclusion criteria: area more than 90% sea or more than 75% urban (based on 1:250,000 OS maps)
  - CS estimates are representative only of squares meeting these criteria; extrapolation to GB or regions assumes excluded vegetative land resembles sampled squares. Bias is generally small unless a region has substantial sea/urban coverage.
- Official estimates are produced using ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals have been estimated with bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.

## Implications for Analysis

- Ensure stratification by ITE Land Classification is accounted for in analyses.
- Apply area-weighting by vegetative land within land classes when aggregating estimates.
- Where possible, use bootstrap-based standard errors and CIs as provided or appropriate for skewed features.
- Be cautious with regions that may include high proportions of sea or urban squares due to potential bias from exclusions.
- Understand that some data are deliberately withheld or generalized for confidentiality, which may affect local-level precision.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.