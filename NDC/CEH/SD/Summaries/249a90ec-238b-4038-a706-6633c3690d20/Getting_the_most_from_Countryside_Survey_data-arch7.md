# Notes on the downloadable data

## Data confidentiality and spatial precision
- Precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify square locations with precision greater than 100 square km.
- As a result, users cannot determine whether specific survey squares fall within defined areas below this threshold.

## Data structure and sampling levels
- CS field survey data come from a sample of 1 km squares across Great Britain.
- Two sampling levels:
  - Whole-square level: general characterisations per square.
  - Within-square level: detailed measurements within selected squares (e.g., quadrats for vegetation, soils, etc.).
- Measurements encompass varied data types, from binary variables to continuous measures (areas, lengths).

## Sampling design and regional classifications
- The square sample is not a random subset; it is stratified within designated strata.
- Strata are defined by the ITE Land Classification (country-specific versions):
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
  - Overall: 45 land classes (country-specific classifications have evolved over time)
- Estimates derived from CS data must account for stratification to be representative; unadjusted estimates may misstate variation.

## Exclusion and representativeness
- Not all GB squares were surveyed:
  - Squares with more than 90% sea area or more than 75% urban area were excluded from field survey.
- Official estimates assume vegetative land in excluded squares resembles that of sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty
- Estimates are produced using ratio estimation for each land class, weighted by vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness and sampling variability.

## References
- Barr et al. (1993) Countryside Survey 1990 Main Report
- Cochran (1963) Sampling Techniques
- Efron & Tibshirani (1993) An Introduction to the Bootstrap