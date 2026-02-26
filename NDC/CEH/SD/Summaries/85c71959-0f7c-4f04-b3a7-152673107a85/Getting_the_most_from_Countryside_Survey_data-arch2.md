# Notes on the downloadable data

- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with detailed measurements inside selected squares (within-square) and for the whole square.
- Measurements include a mix of binary and continuous variables (e.g., vegetation, soils, quadrats) collected at two levels to characterize both the square and its internal features.
- The sampling design is not a random subset of all GB squares; it is stratified by the ITE Land Classification, with sub-samples within designated strata.

## Spatial confidentiality and precision
- To preserve representativeness of the wider countryside, precise locations of CS survey squares are confidential.
- External users cannot identify square locations with precision finer than 100 square kilometres.

## Sampling design in detail
- Strata are defined by the ITE Land Classification; classifications have evolved over time:
  - Original 32 classes
  - 1998 update for Scotland: 42 classes
  - 2007 Wales reporting: 45 classes
  - Each country (England, Wales, Scotland) now has its own classification (England: 21, Wales: 8, Scotland: 16).
- Not all GB squares were surveyed:
  - Excluded if more than 90% sea or more than 75% urban (per 1:250,000 OS maps).
  - Official GB or regional estimates assume remaining vegetative land in excluded squares is similar to sampled squares; bias is considered small except in regions with high sea/urban coverage.
- The data are designed to provide country-specific outputs, with estimates derived from ratio estimation methods that account for land class areas.

## Representativeness and limitations
- The CS estimates are representative only of the squares meeting the inclusion criteria; applying these estimates to the entire GB or to other regions requires caution.
- Because the sampling is stratified and not purely random, analyses that ignore stratification may yield biased estimates of variation.

## Estimation and statistical methods
- Estimates by land class are calculated using ratio estimates (Cochran, 1963), incorporating the area of vegetative land in each sample square.
- Land class estimates are combined using weights proportional to the vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.

## Practical guidance for analysts
- When using CS data, apply the stratification and weighting structure appropriate to the country and land class.
- Be mindful of the confidentiality constraint on precise locations when interpreting spatial results.
- Use bootstrap-based uncertainty measures to reflect skewness and sampling variability.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.