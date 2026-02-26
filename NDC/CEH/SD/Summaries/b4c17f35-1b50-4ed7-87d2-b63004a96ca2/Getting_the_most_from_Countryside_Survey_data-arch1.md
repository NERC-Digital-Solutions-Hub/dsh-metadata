# Notes on the downloadable data

## Key points
- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with two levels of sampling: whole square characterisation and within-square feature measurements (e.g., quadrats for vegetation, soils).
- Measurements include a mix of binary and continuous variables; some characterise the square as a whole, others describe within-square features.
- Squares are not a random subset; the sample is stratified by the ITE Land Classification. Country-specific classifications exist (England 21 classes, Wales 8 classes, Scotland 16 classes) following revisions that added Scotland (1998) and Wales-only reporting (2007).
- Not all GB squares were surveyed. Squares more than 90% sea or more than 75% urban were excluded. The GB estimates assume vegetative land in excluded squares is similar to that in sampled squares; bias is generally small unless a region has a high sea/urban proportion.
- Official estimates are produced using ratio estimation by land class, weighting by the vegetative land area in each land class.

## Confidentiality and scope
- The precise locations of CS survey squares are confidential and cannot be revealed to external users with precision finer than 100 square kilometres.

## Sampling design and implications
- The sampling design implies non-random selection of squares; analyses must account for stratification by land class to obtain representative estimates and accurate variation.
- Estimates without stratification may be biased or have incorrect measures of variation.

## Statistical methods
- Standard errors and confidence intervals have been estimated using bootstrap methods since 1998 due to concerns about skewness in some features (Efron and Tibshirani).

## Data handling and provenance
- Key references:
  - Barr et al. 1993, Countryside Survey 1990 Main Report
  - Cochran 1963, Sampling Techniques
  - Efron and Tibshirani 1993, An Introduction to the Bootstrap

## Implications for analysts
- When using CS data, account for stratified sampling and country-specific land classifications.
- Be mindful of exclusions (sea/urban-heavy areas) and the assumption of similarity in vegetative land between included and excluded squares.
- Use ratio estimates by land class and bootstrap SEs/CIs to obtain robust inferences.
- Maintain data provenance and awareness of confidentiality restrictions when linking CS data to other datasets.