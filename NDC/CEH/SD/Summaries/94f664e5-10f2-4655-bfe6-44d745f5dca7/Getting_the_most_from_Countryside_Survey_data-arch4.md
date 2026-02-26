# Notes on the downloadable data

## Overview
- Addresses confidentiality of Countryside Survey (CS) field data: precise survey square locations are kept confidential by CEH and not disclosed to external users with precision finer than 100 square km.
- Implications: users cannot determine whether specific squares fall within defined areas below the 100 sq km threshold.

## Data structure and content
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels:
  - Whole-square level (characterises the square)
  - Within-square level (describes features inside the square)
- Measurements are diverse, including binary and continuous variables (e.g., areas, lengths, vegetation, soils).

## Sampling design and representativeness
- The CS sample squares are not a random subset of all GB squares; it is a stratified sample with sub-samples within designated strata.
- Strata are defined by the ITE Land Classification, which has evolved over time:
  - Originally 32 classes; updated to 42 in 1998 for Scotland reporting
  - Further revision to 45 classes in 2007 for Wales reporting
  - Each country effectively has its own classification (England: 21, Wales: 8, Scotland: 16)
- Some GB squares were excluded from field surveys:
  - Excluded if area > 90% sea or > 75% urban (based on 1:250,000 OS maps)
- Official estimates are produced by ratio estimates (Cochran, 1963) for each land class, weighting by vegetative land area in each class.
- Excluded squares are assumed to have vegetative land composition similar to sampled squares, which generally minimizes bias unless a region has a high share of sea or urban squares.

## Estimation and uncertainty
- Standard errors and confidence intervals for some features have been estimated using bootstrap methods (since 1998) due to concerns about skewness.

## Data access and privacy implications for data governance
- Location confidentiality constrains precision-based analyses and applications requiring exact square geolocations.
- Any data products must account for stratification and weighting to avoid biased inferences.

## Practical guidance for data users and data leaders
- When using CS data, incorporate:
  - Stratification by country-specific land classifications
  - Weighting by vegetative land area per land class
  - Potential limitations due to exclusions of certain squares
  - Bootstrap-based uncertainty estimates for robust inference
- Ensure metadata clearly documents sampling design, classifications, exclusions, and estimation procedures to support correct interpretation and reuse.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.