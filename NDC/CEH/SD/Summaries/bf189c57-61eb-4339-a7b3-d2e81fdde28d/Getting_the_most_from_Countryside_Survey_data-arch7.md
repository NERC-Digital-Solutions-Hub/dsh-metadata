# Notes on the downloadable data

## Overview for GIS applications
- Data derived from Countryside Survey field surveys, with strict confidentiality on precise square locations to protect representativeness.
- External users are limited to location precision no greater than 100 square kilometres; exact survey square locations cannot be identified at finer scales.

## Data structure and content
- Two levels of sampling: whole 1 km squares and within-square measurements (e.g., quadrats with vegetation, soils).
- Measurements include a mix of binary and continuous variables (areas, lengths, etc.).
- Data are not a random sample; they are stratified by land-class categories and include within-square detail.

## Sampling design and stratification
- Squares selected through stratified sampling within designated strata defined by ITE Land Classification.
- Land Classification classifications have evolved by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Historically changes: 32 classes (original) -> 42 (1998) -> 45 (2007) due to country reporting needs.
- Estimates must account for stratification; analyses ignoring stratification may yield biased or non-representative results.

## Coverage and exclusions
- Not all GB squares are surveyed. Exclusions include squares with more than 90% sea or more than 75% urban area (per 1:250,000 OS maps).
- Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; region-wide biases are considered negligible unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty
- Estimates by land class are produced using ratio estimation (Cochran, 1963), weighted by the vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals are derived using bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.

## Practical implications for GIS work
- Incorporate stratification and land-class weights when aggregating or comparing regions.
- Use vegetative land-area weights to compute class-based estimates; avoid naive equal-weight comparatives across classes or countries.
- Treat precise square locations as confidential; analyses should operate at the prescribed coarser scale and rely on aggregated class/area statistics.
- When assessing uncertainty, rely on bootstrap-derived standard errors rather than assuming homoscedastic errors.
- Be mindful of country-specific land-class definitions when cross-border analyses are performed.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.