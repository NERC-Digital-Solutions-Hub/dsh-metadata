# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify square locations to better than 100 square kilometres.
- This limits the ability to determine whether survey squares fall within defined areas at finer scales.

## Sampling and data structure

- CS field survey data come from a sample of 1 km squares in Great Britain. Each selected square is mapped and measured at two levels: the whole square and within-square features.
- Measurements are diverse, including binary and continuous variables (e.g., areas, lengths).
- The sample is not a random subset of all GB squares; it is stratified by Land Classification, with sub-samples within designated strata.
- Land Classification history:
  - Original 32 classes
  - 1998: expanded to 42 classes (Scotland reporting necessitated changes)
  - 2007: expanded to 45 classes (Wales reporting necessitated further revision)
  - Today, England, Wales, and Scotland use country-specific classifications (21, 8, and 16 classes respectively).
- Estimates that ignore stratification may be unrepresentative or have incorrect variation estimates.

## Excluded squares and representativeness

- Squares with more than 90% sea or more than 75% urban area (based on 1:250,000-scale OS maps) were excluded from field surveys.
- Official GB estimates assume excluded squares are similar in vegetative land composition to sampled squares; this assumption introduces potential bias mainly in regions with many sea/urban squares, though the overall bias is typically small because the excluded area is usually small.

## Estimation and uncertainty

- Land-class estimates are derived using ratio estimation for each land class, weighting by the vegetative land area of each class.
- Weights are based on vegetative land area across the land class as a whole.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features (Efron and Tibshirani).

## Practical implications for analysts

- When analyzing CS data, account for the stratified sampling design and country-specific Land Class schemes.
- Use the appropriate weights and ratio-estimator framework to obtain unbiased estimates.
- Consider uncertainty estimates derived from bootstrap resampling to reflect skewness in the data.
- Be mindful that conclusions drawn for GB or regional levels rely on the assumption that excluded squares are comparable to sampled squares.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.