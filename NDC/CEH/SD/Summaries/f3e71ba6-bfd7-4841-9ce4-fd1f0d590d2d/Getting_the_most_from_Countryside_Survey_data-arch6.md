# Notes on the downloadable data

## Overview
- CEH holds precise locations of Countryside Survey (CS) squares in confidence to preserve representativeness; external users cannot identify square locations with greater precision than 100 square km.
- This limits users from pinpointing whether survey squares fall within defined areas below the 100 sq km threshold.

## Sampling design and data structure
- CS field survey data are from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and measured at two levels: the whole square and within-square features.
- Measurements include varied types, from binary to continuous (e.g., areas, lengths); multiple quadrats collected for vegetation, soils, etc.
- The sample is not a random subset; it is stratified by ITE Land Classification, with sub-samples within strata.
- Land Classification evolution:
  - Original: 32 classes.
  - 1998: Scotland-specific reporting led to 42 classes.
  - 2007: Wales-only reporting led to 45 classes.
  - Current arrangement: separate classifications by country (England: 21 classes, Wales: 8, Scotland: 16).
- Implication: Estimates that do not account for stratification may be not representative and may misstate variation.

## Representativeness and exclusions
- Not all GB squares were considered for field survey.
- Excluded criteria (from 1:250,000 OS maps): area more than 90% sea or more than 75% urban.
- Official GB estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is generally small, unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty
- Official land class estimates are produced using ratio estimates that weight vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods to address skewness in some features (Efron & Tibshirani).

## Practical implications for data work
- Analyses should incorporate stratification by the appropriate Land Classification and country-specific classifications.
- Use ratio estimates with area-based weights; apply bootstrap-derived uncertainty where available.
- Exercise caution when generalising findings beyond the surveyed and weighted areas; recognize the confidentiality constraint on precise locations.
- When combining CS data with other sources, preserve the sampling design, representativeness assumptions, and the stated limitations about extrapolation.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.