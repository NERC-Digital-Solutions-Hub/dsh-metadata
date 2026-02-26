# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data are from a sample of 1 km squares in Great Britain (GB).
- Measurements are taken at two levels: per square (square-level) and within-square (features inside the square).
- Data types include binary (yes/no) variables and continuous measures (areas, lengths, etc.).

## Location privacy and data access
- Precise locations of CS survey squares are kept confidential by UKCEH to preserve representativeness.
- External users cannot identify whether squares fall within specific areas with precision better than 100 square km.

## Sampling design
- Two levels of sampling: whole square and within-square measurements.
- Squares are not a random subset of all GB squares; the sample is stratified with sub-samples within designated strata.
- Measurements are designed to characterize both the square as a whole and features within the square.

## Stratification and land classification
- Strata for square selection defined by the ITE Land Classification.
- Classification changes over time and by country:
  - Original: 32 land classes.
  - 1998 (Scotland reporting): 42 classes.
  - 2007 (Wales reporting): 45 classes.
- Country-specific classifications now: England 21, Wales 8, Scotland 16.

## Exclusions and representativeness
- Squares excluded from field survey if:
  - More than 90% sea area, or
  - More than 75% urban area (based on 1:250,000 OS maps).
- Official GB/region estimates assume excluded squares have vegetative land composition similar to sampled squares.
- Potential bias is possible if a region has a high proportion of sea or urban squares.

## Estimation methods
- Estimates by land class are produced using ratio estimates (Cochran, 1963).
- Weights are the area of vegetative land within each land class.

## Uncertainty estimation
- Standard errors and confidence intervals are estimated using bootstrap methods (since 1998) due to skewness concerns (Efron and Tibshirani, 1993).

## Practical considerations for analysts
- Account for stratification; ignoring it can lead to non-representative estimates and misestimated variation.
- When combining data across land classes or regions, weight results by the vegetative land area of each class.
- Be aware of country-specific land classifications when making cross-country comparisons.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.