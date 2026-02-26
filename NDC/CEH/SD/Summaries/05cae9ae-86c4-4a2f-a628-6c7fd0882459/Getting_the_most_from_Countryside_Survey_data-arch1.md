# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify whether squares fall within defined areas beyond a 100 square km precision.
- CS field survey data come from a sample of 1 km squares in Great Britain, with measurements at both the square level and within-square features (e.g., quadrats for vegetation, soils).
- The sample is not a random subset; it is stratified by the ITE Land Classification, which has been adjusted over time (32 → 42 → 45 classes) and now yields country-specific classifications (England: 21, Wales: 8, Scotland: 16).
- Some squares were excluded from field survey: those with more than 90% sea area or more than 75% urban area, as measured on a 1:250,000 OS map. Estimates for GB or regions assume excluded squares are similar in vegetative land composition to sampled squares; this assumption is generally acceptable due to the small total land area affected, but regional biases can occur if a region has a high proportion of sea/urban squares.
- Because of the sampling design, official GB estimates are produced using ratio estimates by land class, weighted by the vegetative land area of each land class. This weighting is essential for representative estimates.
- Since 1998, standard errors and confidence intervals are estimated with bootstrap methods (Efron & Tibshirani), addressing skewness concerns in certain features.
- Data provenance, stratification, and the method of extrapolation to unsampled areas have important implications for analysis and interpretation; analysts should account for stratification, non-random sampling, and potential biases when drawing inferences.

## Practical implications for analysts

- When analyzing CS data, incorporate the stratification by land class and country-specific classifications to obtain valid variance estimates.
- Do not treat CS samples as simple random samples; use ratio-estimator approaches with the appropriate weights.
- Be mindful of the confounding effect of excluded squares (sea/urban) on regional estimates and the assumptions used to extrapolate to GB or regional scales.
- Use bootstrap-derived standard errors and confidence intervals to reflect skewness and sampling design.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.