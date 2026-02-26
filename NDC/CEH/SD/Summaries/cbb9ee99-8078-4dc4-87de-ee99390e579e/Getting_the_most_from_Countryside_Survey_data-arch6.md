# Notes on the downloadable data

## Overview
- Documents Countryside Survey (CS) field survey data: a GB-wide sample of 1 km squares with both square-level and within-square measurements, including vegetation, soils, etc.
- Data types range from binary (yes/no) to continuous (areas, lengths); measurements are taken at two levels to characterize squares and features within squares.

## Sampling design and data structure
- Not a simple random sample; the CS uses a stratified design with sub-samples within designated strata.
- Strata are defined by the ITE Land Classification, with country-specific classifications:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Land Classification classifications have evolved:
  - Original: 32 classes
  - 1998: Scotland-specific reporting changed to 42 classes
  - 2007: Wales reporting led to 45 classes in total
- Two levels of sampling:
  - Whole square level
  - Within-square level (e.g., quadrats for vegetation, soils)
- Some squares are excluded from field survey based on map-derived area criteria (see below).

## Location confidentiality and scope
- Precise locations of survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify any survey squares with precision better than 100 square km.
- Consequently, it is not possible to determine whether specific squares fall within defined, finer-scale areas.

## Excluded squares and representativeness
- Squares with more than 90% sea or more than 75% urban area are excluded from field surveys.
- Official GB estimates apply only to squares meeting the inclusion criteria; estimates for GB or regions assume excluded squares have similar vegetative composition to sampled squares.
- This assumption may introduce bias in regions with high proportions of sea or urban squares; the overall bias is expected to be small because the excluded land area is typically small.

## Estimation and uncertainty
- Land-class estimates are produced using ratio estimates (Cochran, 1963), with weights based on the vegetative land area within each land class.
- Estimates across land classes are combined using the overall vegetative land-area weights for the class total.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.

## Practical guidance for data use
- When analysing CS data, account for stratification by Land Classification and apply appropriate weights.
- Be mindful of the non-random sampling design and the exclusion of certain squares when interpreting region or GB-wide estimates.
- Use bootstrap-based uncertainty measures as provided, or replicate with bootstrap procedures if conducting custom analyses.
- Recognize location confidentiality limitations when creating geospatial outputs; precise square-level mapping beyond 100 km² resolution is not possible.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.