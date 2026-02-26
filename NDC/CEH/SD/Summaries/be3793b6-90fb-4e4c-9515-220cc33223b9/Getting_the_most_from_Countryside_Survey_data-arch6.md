# Notes on the downloadable data

## Overview
- Describes confidentiality, sampling design, and estimation methods for Countryside Survey (CS) field data used to derive estimates for GB vegetative land.

## Confidentiality and data precision
- Precise locations of CS survey squares are kept confidential by CEH.
- External users cannot identify square locations with precision finer than 100 square km.
- This prevents determining whether squares fall within defined areas below this threshold.

## Sampling design and data structure
- CS field survey data are from a sample of 1 km squares in GB.
- Two levels of sampling and measurement:
  - Overall square level: characterises the square.
  - Within-square level: measurements from quadrats and features within the square (e.g., vegetation, soils).
- Measurements vary in type (binary, continuous).
- The sample is not a random subset of all GB squares; it is stratified within designated strata.

## Stratification and land classification
- Stratification uses the ITE Land Classification.
- Land classification has evolved:
  - Originally 32 classes.
  - 1998 revision for Scotland reporting increased to 42 classes.
  - 2007 revision for Wales reporting increased to 45 classes.
- Each country (England, Wales, Scotland) has its own classification (England: 21, Wales: 8, Scotland: 16).
- Estimates must account for stratification; ignoring it may yield non-representative estimates and incorrect variation.

## Exclusions and representativeness
- Squares excluded from field survey if:
  - Area > 90% sea, or
  - > 75% urban (as measured on 1:250000 OS maps).
- Official estimates for GB (or regions) assume excluded vegetative land is similar in composition to sampled squares.
- This assumption introduces potential bias mainly if a region has a high proportion of sea or urban squares; otherwise bias is expected to be negligible.

## Estimation and uncertainty
- Official GB land-class estimates are produced using ratio estimates (Cochran 1963), weighted by the vegetative land area within each land class.
- Since some features can be highly skewed, standard errors and confidence intervals have been estimated using the bootstrap method (Efron and Tibshirani 1993) since 1998.

## Practical implications for data use
- When analyzing CS data, incorporate the stratified design and country-specific land classifications.
- Use the provided weighting by vegetative land area to obtain representative estimates.
- Be aware of potential biases from excluded squares, particularly in regions with substantial sea/urban areas.
- Use bootstrap-based uncertainty measures for robust confidence intervals.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.