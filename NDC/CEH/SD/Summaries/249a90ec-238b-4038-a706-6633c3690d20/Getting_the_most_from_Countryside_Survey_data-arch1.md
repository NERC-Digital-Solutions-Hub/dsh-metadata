# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify whether squares fall within defined areas with a precision finer than 100 square kilometres.

## What the data are and how they are collected

- CS field survey data come from a sample of 1 km squares across Great Britain (GB), with measurements made at two levels: the square level and features within each square (e.g., quadrats for vegetation, soils, etc.).
- Measurements are varied, including binary and continuous variables, and are designed to characterize both the overall square and within-square features.
- The sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16). The Land Classification classifications have evolved over time (32 -> 42 -> 45 classes) to support separate country reporting.

## Sampling design and representativeness

- Not all GB squares were considered for field survey. Squares with more than 90% sea or more than 75% urban area were excluded.
- Estimates for GB or regional scales assume that vegetative land in excluded squares is similar in composition to sampled squares; bias is considered small except in regions with high sea/urban square proportions.
- Because of stratification and exclusions, analyses must account for the design to avoid biased inferences.

## Estimation and uncertainty

- Official estimates are produced using ratio estimation techniques (Cochran, 1963) by land class, weighting by the area of vegetative land within each class.
- From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness in some features.
- Data are designed so that some measurements describe the whole square while others describe inside-square features, enabling both square-level and within-square characterizations.

## Practical implications for analysts

- analyses should incorporate the stratified sampling design and country-specific land classifications to obtain valid inferences.
- When pooling data across squares or countries, apply the appropriate weights (e.g., area of vegetative land by land class) and consider bootstrap-based uncertainty estimates.
- Be mindful of the confidentiality constraint on precise locations when linking CS data to other datasets or geographic areas.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.