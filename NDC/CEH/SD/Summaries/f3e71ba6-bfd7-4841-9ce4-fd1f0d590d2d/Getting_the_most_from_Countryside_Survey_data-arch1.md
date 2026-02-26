# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are confidential to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision better than 100 square km.

## Sampling design and data structure

- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and measured at two levels: square level (characterising the square) and within-square (features inside the square).
- Measurements include a range of data types from binary to continuous (areas, lengths, etc.).

## Non-random stratified sampling and land classification

- The CS sample is not a random subset of GB squares; it is stratified by the ITE Land Classification.
- Land classification has evolved: originally 32 classes, then 42 (1998) for Scotland separation, and 45 (2007) with Wales reporting; effectively England (21), Wales (8), Scotland (16) classes.
- Estimates ignoring stratification may be unrepresentative and have inaccurate variation estimates.

## Excluded squares and representativeness

- Squares with >90% sea area or >75% urban area were excluded from field survey.
- Official GB estimates assume vegetative land in excluded squares resembles that in sampled squares; bias is generally negligible unless a region has high sea/urban square proportions.

## Estimation approach and uncertainty

- Estimates by land class are produced as ratio estimates, weighted by the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness concerns.

## Practical implications for analysts

- When analyzing CS data, account for stratification by land class, use area-based weighting, and consider bootstrap-derived uncertainty.
- Be cautious with extrapolations to areas or regions where the sampling frame differs (e.g., high proportions of sea or urban land).

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.