# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify survey squares with precision finer than 100 square km.
- CS Field Survey data are collected from a sample of 1 km squares in GB, with measurements at two levels: the whole square and features within each square (e.g., quadrats for vegetation, soils).

## Sampling design and data structure

- Sampling is not a random subset of GB squares; it is stratified by the ITE Land Classification, with sub-samples within designated strata.
- Measurements include a mix of binary and continuous variables (e.g., areas, lengths).
- The land-class classification has evolved:
  - 32 classes originally
  - 42 classes in 1998 (to accommodate Scotland reporting)
  - 45 classes in 2007 (to accommodate Wales reporting)
  - England: 21 classes; Wales: 8 classes; Scotland: 16 classes

## Representativeness and exclusions

- Not all GB squares were considered for field survey. Squares with more than 90% sea or more than 75% urban area were excluded.
- Official GB or regional estimates assume vegetative land composition in excluded squares is similar to sampled squares; bias is generally small unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty

- Estimates are produced using ratio estimation (Cochran, 1963) for each land class, weighted by the vegetative land area of that class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness in some features.

## Practical implications for data use

- When analyzing CS data, account for stratification by land class and country-specific classifications.
- Use the provided ratio-estimate framework and area-based weights for unbiased estimates.
- Apply bootstrap-derived standard errors and confidence intervals to assess uncertainty.
- Be mindful of the location confidentiality and the implications for spatial precision in analyses.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman & Hall; London.