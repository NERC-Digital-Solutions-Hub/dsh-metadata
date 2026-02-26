# Notes on the downloadable data

## Overview
- Documents how Countryside Survey (CS) field data are collected, represented, and analyzed.
- Sets constraints to preserve representativeness: precise square locations are withheld to 100 square km accuracy.
- Data are meant to enable robust inference about vegetative land, with careful attention to sampling design and estimation methods.

## Data collection and sampling design
- Field data come from a sample of 1 km squares across Great Britain; each square is mapped and measured at two levels (whole square and within-square features).
- Measurements include a mix of binary and continuous variables (e.g., vegetation, soils, quadrat-based data).
- The sampling is not a simple random subsample; it is stratified by the ITE Land Classification, with country-specific adaptations:
  - England: 21 land classes
  - Wales: 8 land classes
  - Scotland: 16 land classes
- Not all GB squares are surveyed: squares >90% sea or >75% urban are excluded from field survey.
- Consequently, CS estimates are produced using ratio estimation by land class, weighted by the vegetative land area within each class.

## Representativeness, limitations, and implications
- Because the sample is stratified and not all squares are surveyed, estimates that ignore stratification may be biased or misrepresent variation.
- Excluded squares (large sea or urban areas) could bias regional estimates only if such areas are disproportionately large in a region; overall bias is expected to be small due to the relatively small area affected.
- Official GB and regional estimates assume excluded squares are similar in vegetative composition to sampled ones; this assumption underpins broader inferences.

## Analysis methods and uncertainty
- Estimation uses ratio estimates (Cochran, 1963) by land class, then combines classes with weights equal to vegetative land area.
- Standard errors and confidence intervals have been estimated with bootstrap methods (Efron & Tibshirani, 1993) since 1998 to address skewness in features.

## Data privacy, access, and usage notes
- Exact survey square locations are kept confidential beyond a 100 square km precision to protect representativeness.
- Users cannot identify whether specific survey squares fall within defined areas below the precision threshold.
- When using CS data, analytical approaches should account for stratification, weighting by vegetative land area, and bootstrap-based uncertainty.

## Practical references
- Barr et al. (1993) Countryside Survey 1990 Main Report
- Cochran (1963) Sampling Techniques
- Efron & Tibshirani (1993) An Introduction to the Bootstrap