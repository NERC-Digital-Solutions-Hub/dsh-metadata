# Notes on the downloadable data

## Overview
- Locations of Countryside Survey squares are kept confidential by UKCEH; precise identification beyond 100 square km is not provided to external users.
- This confidentiality constraint affects the ability to determine whether survey squares fall within specific areas.

## Sampling design and data content
- Field survey data come from a sample of 1-km squares in Great Britain.
- Each selected square is mapped and measured at two levels: the square level and within-square (e.g., quadrats) level.
- Data types include binary and continuous measurements (e.g., areas, lengths).

## Representativeness and limitations
- The CS sample is not a random subset of all GB 1-km squares; it is stratified by the ITE Land Classification.
- Land classification details have evolved by country (England, Wales, Scotland) leading to a total of 45 classes across the three countries.
- Estimates that do not account for stratification may be biased; proper weighting by vegetative land area per land class is necessary.
- Not all 1-km squares were surveyed; exclusions include squares with more than 90% sea area or more than 75% urban area at 1:250,000 scale OS maps.
- In practice, national estimates assume excluded squares have vegetative land composition similar to sampled squares; bias is considered small unless a region has a high proportion of sea/urban squares.

## Estimation and analysis methods
- Official GB estimates are produced using ratio estimation within each land class, weighted by the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to handle skewness in some features.

## Implications for data stewardship
- When releasing or documenting data, include clear metadata on:
  - Confidentiality constraints and geolocation precision (100 km2 threshold).
  - Sampling design: stratification by ITE Land Classification, country-specific classifications, and the 45 classes.
  - Exclusions and their rationale (sea/urban cutoffs) and the assumption about excluded areas.
  - Weighting scheme and the use of ratio estimates for class-level totals.
  - Bootstrap methodology for standard errors and CIs (with references).
- Ensure users understand limitations on representativeness and the need to apply appropriate weighting and stratification in analyses.
- Maintain provenance and methodological references for reproducibility (Barr et al. 1993; Cochran 1963; Efron & Tibshirani 1993).

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.