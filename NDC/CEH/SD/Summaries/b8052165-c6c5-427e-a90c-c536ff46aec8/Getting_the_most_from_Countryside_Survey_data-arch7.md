# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify square locations with precision better than 100 square km.
- This confidentiality means users cannot determine whether specific survey squares fall within defined areas.

## Sampling design and data levels
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Measurements occur at two levels: the whole square and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Data types range from binary (yes/no) to continuous (areas, lengths).

## Stratification and land classification
- The sampling is stratified, not random, within designated strata defined by the ITE Land Classification.
- Land classification history:
  - Originally 32 classes.
  - 1998: Scotland-specific reporting increased to 42 classes.
  - 2007: Wales-specific reporting increased to 45 classes.
  - Currently, England has 21 classes, Wales 8, Scotland 16.
- Estimates must account for stratification; analyses that ignore it may be non-representative.

## Exclusions and representativeness
- Squares excluded from field survey: those with >90% sea area or >75% urban area (based on 1:250,000 OS maps).
- Official GB estimates are derived from the included squares, with the assumption that vegetative land in excluded squares is similar to that in sampled squares.
- In practice this assumption generally produces negligible bias, unless a region has a high proportion of sea or urban squares.

## Estimation methods and uncertainty
- Estimates are produced using ratio estimation (Cochran, 1963) for each land class, weighting by the vegetative land area of each class.
- Land class estimates are then combined using the total vegetative land area as weights for the class as a whole.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness in some features.

## Practical implications for GIS analyses
- When using CS data in map-based analyses, account for stratification by Land Classification and the weighting scheme.
- Be mindful of confidentiality constraints limiting precise location information to avoid misinterpretation of spatial relationships.
- Use bootstrap-derived uncertainty measures to convey variability in estimates.
- Recognize that GB-wide estimates rely on assumptions about excluded squares; regional analyses may be affected if excluded areas are non-representative.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.