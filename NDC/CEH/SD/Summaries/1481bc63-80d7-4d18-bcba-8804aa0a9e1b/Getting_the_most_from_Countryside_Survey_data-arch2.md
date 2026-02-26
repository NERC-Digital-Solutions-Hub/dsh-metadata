# Notes on the downloadable data

## Privacy and data access
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify squares with precision better than 100 square kilometers.
- Consequently, it is not possible to determine whether any survey squares fall within defined areas below this threshold.

## Sampling design
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured in detail at two levels: the square level and within-square features.
- Measurements include both binary (yes/no) variables and continuous variables (areas, lengths, etc.).
- The sample is not a random subset of all GB squares; it is stratified with sub-samples within designated strata.
- Stratification is defined by the ITE Land Classification, which has evolved:
  - Originally 32 land classes.
  - 1998: Scotland reporting led to 42 classes.
  - 2007: Wales reporting led to 45 classes.
  - England: 21 classes; Scotland: 16; Wales: 8.
- Estimates that ignore stratification may be unrepresentative and have incorrect variation estimates.

## Exclusions and representativeness
- Squares excluded from field survey if:
  - More than 90% sea area, or
  - More than 75% urban.
- Official GB estimates assume vegetative land in excluded squares is similar in composition to sampled squares; this is generally a small potential bias, except in regions with a high proportion of sea or urban squares.

## Estimation methods
- Estimates by land class are produced using ratio estimation (Cochran, 1963), incorporating the area of vegetative land in each sample square.
- Land class estimates are then combined using weights equal to the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron and Tibshirani, 1993) due to skewness concerns.

## Practical implications for analysts
- When using CS data, account for the stratified sampling design and country-specific land classifications.
- Use ratio-estimator approaches with appropriate weighting by vegetative land area.
- Apply bootstrap-based standard errors and confidence intervals for robust inference.
- Be mindful of the exclusion criteria and potential biases in regions with high sea/urban square proportions.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.