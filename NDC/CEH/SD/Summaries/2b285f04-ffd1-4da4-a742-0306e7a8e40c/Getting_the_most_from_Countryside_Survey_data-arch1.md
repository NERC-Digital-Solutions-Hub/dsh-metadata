# Notes on the downloadable data

- Purpose: Describes confidentiality, sampling design, representativeness, estimation methods, and references for Countryside Survey (CS) data.
  
## Confidentiality and spatial precision
- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify square locations to better precision than 100 square km.
- This limits the ability to determine whether squares fall within defined areas below this threshold.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped; measurements are taken at two levels:
  - Whole-square level (characterizes the square)
  - Within-square level (describes features inside the square)
- Measurements vary in type (binary and continuous).
- The sampling is not a random subset; it is stratified by the ITE Land Classification.
- Land Classification details:
  - Originally 32 classes; updated to 42 in 1998 for Scotland-specific reporting; expanded to 45 classes in 2007 for Wales-specific reporting.
  - Each country (England, Wales, Scotland) effectively has its own classification scheme.
- The sampling design requires accounting for stratification in analyses to obtain representative estimates.

## Representativeness and exclusions
- Not all GB squares were surveyed; excludes squares with:
  - More than 90% sea area, or
  - More than 75% urban area (based on 1:250,000 OS maps).
- Official GB estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is expected to be small unless a region has a high sea/urban proportion.

## Estimation methods and uncertainty
- Estimates by land class are produced using ratio estimation (Cochran, 1963), weighting by the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are derived using bootstrap methods (Efron & Tibshirani, 1993) due to skewness in some features.

## References
- Barr et al. (1993) Countryside Survey 1990 Main Report
- Cochran (1963) Sampling Techniques
- Efron & Tibshirani (1993) An Introduction to the Bootstrap