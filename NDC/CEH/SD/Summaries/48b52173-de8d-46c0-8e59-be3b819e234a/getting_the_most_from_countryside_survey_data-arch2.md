# Notes on the downloadable data - Sampling Considerations in the use of Countryside Survey Data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at both the square level and within-square features.
- Measurements are a mix of binary and continuous variables (e.g., vegetation, soils), enabling characterisation of squares and internal features.

## Geographic confidentiality and precision
- The exact locations of CS survey squares are kept confidential by UKCEH to preserve representativeness.
- External users cannot identify locations with precision finer than 100 square kilometers.
- Consequently, it is not possible to determine whether specific survey squares lie within defined areas below this threshold.

## Sampling design and implications for analysis
- The CS sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification.
- The Land Classification has evolved:
  - Originally 32 classes; expanded to 42 in 1998 for Scotland reporting.
  - Further revision leading to 45 classes in 2007 (England 21, Wales 8, Scotland 16).
- Analyses that ignore stratification may yield non-representative estimates and incorrect variation.
- Two sampling levels:
  - Whole square (1 km square level)
  - Within-square (feature-level) measurements
- Not all GB squares were surveyed; squares >90% sea or >75% urban were excluded from field work.
- Inference for GB or regions relies on the assumption that vegetative land in excluded squares is similar to sampled squares; bias is generally considered negligible unless a region has a high proportion of sea/urban squares.

## Estimation methods and uncertainty
- Official land class estimates are produced using ratio estimators, weighting by the vegetative land area within each land class.
- Post-1998 adjustments: standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features.

## Practical guidance for analysts
- Ensure stratification by Land Classification is incorporated in analyses.
- Apply area-weighted land-class estimates to reflect vegetative land distribution.
- Use bootstrap-based confidence intervals to quantify uncertainty, particularly for skewed features.
- Be mindful of the limited precision of square locations when linking CS data to other geographic areas.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.