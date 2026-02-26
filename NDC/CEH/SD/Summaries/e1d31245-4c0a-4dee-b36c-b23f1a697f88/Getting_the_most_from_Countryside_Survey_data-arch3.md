# Notes on the downloadable data

## Overview
- Explains how Countryside Survey (CS) data are collected, the sampling design, estimation methods, and confidentiality considerations for precise locations.
- Highlights how representativeness is maintained and the implications for analysis and interpretation.

## Data privacy and availability
- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify squares with precision finer than 100 square kilometers.

## Sampling design and levels
- CS field data come from a sample of 1 km squares across Great Britain.
- Each selected square is mapped and measured at two levels:
  - Whole-square characterisation
  - Within-square measurements (e.g., quadrats for vegetation, soils, etc.)
- Measurements vary from binary to continuous.
- The sample is not random; it is stratified by ITE Land Classification.
  - Land classifications differ by country: England (21 classes), Wales (8), Scotland (16); classifications have evolved (32 → 42 → 45 classes).
- Not all GB squares are considered for field survey:
  - Excluded if >90% sea or >75% urban (per 1:250000 OS maps).
  - Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

## Implications for analysis
- Analyses must account for stratification; ignoring it can yield non-representative estimates and incorrect estimates of variation.
- Extrapolation to GB or regional scales relies on the assumption of similarity between included and excluded squares.

## Estimation methods
- Official GB land-class estimates are produced using ratio estimates that weight by the vegetative land area within each land class.
- Land-class estimates are combined using weights equal to the total vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness concerns.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.