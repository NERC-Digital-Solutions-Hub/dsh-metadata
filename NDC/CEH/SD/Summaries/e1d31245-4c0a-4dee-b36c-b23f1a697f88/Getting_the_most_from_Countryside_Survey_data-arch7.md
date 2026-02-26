# Notes on the downloadable data

- To preserve representativeness of the wider countryside, the precise locations of CS survey squares are kept confidential by CEH. External users are not provided with precision better than 100 square kilometres, so it is not possible to identify whether specific survey squares fall within defined areas below this threshold.

## Overview for GIS specialists

- Countryside Survey (CS) field data come from a sample of 1 km squares in Great Britain (GB), with measurements at both the whole square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
- The data are not a random subset; they are stratified by Land Classification. Estimates must account for this stratification to be representative.

## Sampling design and classifications

- Two levels of sampling:
  - Whole square level (characteristics of the square)
  - Within-square level (features inside the square)
- Square selection is stratified by the ITE Land Classification; country-specific classifications have evolved:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Not all GB squares were surveyed; squares with >90% sea area or >75% urban area were excluded from field survey.
- Official GB estimates assume that vegetative land in excluded squares is similar to sampled squares, which may introduce bias only if a region has a high proportion of sea or urban squares.

## Representativeness and scope

- Estimates are based on ratio estimates (Cochran, 1963) by land class and are weighted by the vegetative land area within each land class.
- Because of the sampling design and exclusions, official GB or regional estimates may be biased if the stratification or excluded areas are not properly accounted for.

## Estimation, uncertainty, and methods

- Weights are the area of vegetative land in each land class.
- Since 1998, due to concerns about skewness in some features, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993).

## Practical implications for GIS analyses

- When creating map-based products, account for:
  - Stratified sampling design and land-class weighting
  - Area-based weights by vegetative land in each class
  - Uncertainty estimates derived from bootstrap SEs
  - The confidentiality of precise square locations (no high-precision spatial identification beyond 100 km²)
- Be cautious in interpreting region- or GB-wide estimates; ensure methods reflect the sampling frame and exclusions.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.