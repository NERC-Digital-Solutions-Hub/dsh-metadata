# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares in Great Britain.
- Each selected square is mapped with detailed measurements at multiple levels (square-level and within-square features), including vegetation and soils. Measurements range from binary to continuous.

## Confidentiality and data precision
- The precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify squares with precision finer than 100 square kilometers.
- It is not possible to determine whether any given survey square falls within defined areas below this threshold.

## Sampling design and selection
- The CS sampling is not a random subset of GB squares; it is stratified.
- Stratification is by the ITE Land Classification, with country-specific changes:
  - England: 21 land classes
  - Wales: 8 land classes
  - Scotland: 16 land classes
- Classifications changed over time:
  - 1998: Scotland reporting led to 42 classes (from 32)
  - 2007: Wales reporting led to further changes (overall 45 classes)
- Field survey coverage excludes squares whose area is more than 90% sea or more than 75% urban, as measured from 1:250,000 OS maps.
- Official estimates for GB or regions are derived by ratio estimates within land classes, weighted by vegetative land area in each class.

## Exclusions and representativeness
- The field survey data are representative only of GB squares that meet the exclusion criteria (not predominantly sea/urban).
- Extrapolations to GB or regions assume similar vegetative land composition in excluded squares; this is generally reasonable due to the small total area involved, but issues arise in regions with high sea or urban proportions.

## Estimation, weighting and uncertainty
- Estimates are produced using ratio estimates (Cochran, 1963) within land classes, then combined with weights equal to vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.

## Data structure and measurement levels
- Two sampling levels:
  - Whole square: characterises the square as a unit
  - Within-square: measures features inside the square (e.g., quadrats)
- Data types include binary (yes/no) and continuous measurements (areas, lengths, etc.).

## Implications for analysts
- Analyses must account for stratified sampling and weighting by vegetative land area.
- Avoid naive generalisation from sampled squares to all GB squares; incorporate the stratification structure.
- Use bootstrap-derived standard errors and confidence intervals when assessing uncertainty.
- Be mindful of potential biases if region-specific exclusion (sea/urban) is substantial.
- Maintain consideration of confidentiality constraints when interpreting precise locations and spatial aggregation.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.