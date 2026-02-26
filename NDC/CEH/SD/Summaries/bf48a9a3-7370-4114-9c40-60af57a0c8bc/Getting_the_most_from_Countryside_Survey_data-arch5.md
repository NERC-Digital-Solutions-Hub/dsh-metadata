# Notes on the downloadable data

## Overview
- Describes how Countryside Survey (CS) field data are collected, stored, and analysed, including confidentiality constraints on precise locations and the statistical methods used to produce GB-wide estimates.

## Data confidentiality and location privacy
- Exact locations of CS survey squares are held by CEH and not disclosed externally beyond 100 square km precision.
- Users cannot identify whether any survey squares fall within defined areas smaller than this threshold.

## Sampling design and data structure
- CS field data come from a sample of 1 km square areas across Great Britain.
- Two levels of measurement: whole squares (square-wide) and within-square features.
- Data types range from binary to continuous (e.g., areas, lengths).

## Sampling framework and stratification
- The sample is not random; it is stratified by land classification (ITE Land Classification).
- Land classification history:
  - Originally 32 classes.
  - 1998: expanded to 42 classes to accommodate Scotland reporting.
  - 2007: expanded to 45 classes due to Wales reporting requirements.
- Each country effectively has its own classification: England (21), Wales (8), Scotland (16).

## Representativeness and weighting
- Estimates that ignore stratification may be biased; appropriate ratio-estimation and weighting are required.
- Land-class estimates are weighted by the vegetative land area of each class.

## Exclusions and representativeness
- Not all GB squares were surveyed: excludes squares that are >90% sea or >75% urban (based on 1:250,000 OS maps).
- Official GB estimates assume excluded squares have similar vegetative composition to included squares; this may introduce bias only if a region has a high proportion of sea/urban squares.

## Estimation methodology and uncertainty
- Estimates are produced using ratio estimation methods for each land class, with weights by vegetative area within classes.
- Since 1998, bootstrap methods (Efron & Tibshirani) are used to estimate standard errors and confidence intervals due to potential skewness in some features.

## Implications for data users and governance
- Metadata should document the stratified sampling design, country-specific classifications, and weighting schemes.
- Location confidentiality and the handling of excluded squares should be clearly described to inform analyses and reproducibility.
- Users should consider the non-random, stratified design and potential biases when interpreting regional or GB-wide estimates.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.