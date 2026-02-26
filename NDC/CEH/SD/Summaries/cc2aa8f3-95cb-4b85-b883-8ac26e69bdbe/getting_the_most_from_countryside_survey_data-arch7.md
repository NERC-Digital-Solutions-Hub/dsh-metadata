# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data derive from a sample of 1 km squares in Great Britain, with measurements at both the whole-square level and within-square features (e.g., vegetation quadrats, soils).

## Location privacy and precision
- To preserve representativeness of the wider countryside, precise locations of CS survey squares are held confidential by UKCEH.
- External users cannot identify square locations to better than 100 square km precision, so you cannot determine whether squares fall within defined areas below this threshold.

## Sampling design and data structure
- Two levels of sampling: whole squares and within-square measurements.
- The sample is not a random subset of GB squares; it is stratified by ITE Land Classification.
- Land Classification classifications have evolved:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
  - Originally 32 classes; updated to 42 (1998) and 45 (2007) with country-specific reporting.
- Measurements include varied data types, from binary (yes/no) to continuous (areas, lengths).

## Exclusions and representativeness
- Some squares were excluded from field survey: more than 90% sea, or more than 75% urban (based on 1:250,000 OS maps).
- Official GB or regional estimates assume vegetative land in excluded squares is similar to included squares; bias is expected to be small, except in regions with high sea or urban proportions.

## Estimation methods
- Estimates by land class are produced using ratio estimates, weighted by the vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap due to concerns about skewness in some features.

## Implications for GIS work
- When summarising data, account for stratification and weighting by land class area.
- Be cautious about region-level inferences in areas with many excluded squares or unique land classifications.
- Location confidentiality means GIS work should rely on aggregated or anonymised data rather than exact square placements when mapping.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.