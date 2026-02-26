# Notes on the downloadable data

- Purpose: Outline how Countryside Survey (CS) data are collected, processed, and estimated, with attention to representativeness, data access, and analysis implications for users.

## Key data governance and access points
- To preserve representativeness, precise locations of CS survey squares are kept confidential. External users cannot identify squares to better than 100 square km, limiting precise geographic tracing in analyses.

## Sampling design and data structure
- CS field data are collected from a sample of 1 km squares across Great Britain (GB).
- Two levels of sampling and measurement:
  - Whole-square level: general square characteristics.
  - Within-square level: detailed measurements (e.g., quadrats for vegetation, soils).
- Data types range from binary to continuous measurements.
- The sample is not a random subset of GB squares; it is stratified, with sub-samples drawn within designated strata.

## Stratification and land classification
- Strata are defined by the ITE Land Classification, which has evolved:
  - Originally 32 classes; expanded to 42 in 1998 for Scotland; further revised to 45 classes in 2007 for Wales.
  - England has 21 classes, Wales 8, Scotland 16 (as separate country classifications).
- Estimates must account for stratification to be representative; ignoring stratification yields biased variation estimates.

## Exclusions and representativeness
- Some squares were excluded from field surveys:
  - Excluded if more than 90% sea or more than 75% urban (per 1:250,000 OS maps).
- Official GB estimates assume vegetative land in excluded squares is similar to sampled squares. This bias is generally negligible, except in regions with high sea or urban square proportions.

## Estimation and uncertainty
- Estimates are produced using ratio estimation (Cochran, 1963) for each land class and then combined using weights based on vegetative land area within each class.
- Standard errors and confidence intervals are estimated via bootstrap methods (from 1998 onward) due to skewness concerns in some features (Efron & Tibshirani, 1993).

## Measurement and data quality notes
- The CS dataset includes both square-level and within-square measurements, with a mix of binary and continuous variables.
- The origin and structure of the data imply careful attention to the sampling design when analysing features, making use of stratification and weighting essential.

## Implications for data strategy and use
- Data leaders should:
  - Ensure analyses account for stratified sampling and area-based weighting.
  - Be mindful of confidentiality constraints limiting precise geolocation, which may affect reproducibility or regional targeting.
  - Use bootstrap-based uncertainty measures for appropriate features.
  - Recognize potential biases due to exclusions (sea/urban-dominated squares) and consider regional context when interpreting GB-wide estimates.
- Consider collaboration and data-sharing practices that align with the compatibility and metadata needs of stratified, regionally classified datasets.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.