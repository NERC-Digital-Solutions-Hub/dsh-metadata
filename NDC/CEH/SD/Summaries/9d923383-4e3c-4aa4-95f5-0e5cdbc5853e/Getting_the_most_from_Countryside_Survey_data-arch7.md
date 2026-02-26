# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at both the square level and within-square features.
- Data include a variety of measurement types, from binary to continuous, across different vegetation and soil features.
- The document explains confidentiality, sampling design, and how estimates are produced to support GIS-based analyses.

## Data confidentiality and geographic precision
- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify square locations with precision finer than 100 square kilometres.
- Consequently, it is not possible to determine whether any survey squares fall within specific areas below this threshold.

## Sampling design and levels
- Each CS square is surveyed in detail, with two levels of information:
  - Whole-square level: general characteristics and classifications.
  - Within-square level: detailed measurements for selected features (e.g., vegetation, soils) using quadrats.
- Sampling design is not a random subset of GB squares; it is stratified by designated strata.

## Stratification and Land Classification
- Stratification is based on the ITE Land Classification.
- Land-class classifications by country now differ:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- The classification has changed over time:
  - Originally 32 classes
  - 1998 update: 42 classes (to accommodate Scotland reporting)
  - 2007 update: 45 classes (to accommodate Wales reporting)
- Analyses that do not account for stratification may yield biased estimates of variation.

## Excluded squares and coverage
- Squares with more than 90% sea or more than 75% urban area (per 1:250,000 OS maps) were excluded from field survey.
- Official GB estimates apply only to the squares that meet the above criteria.
- Extrapolations to GB or regions assume excluded squares have similar vegetative land composition to sampled squares.
- Bias from this extrapolation is generally negligible, except in regions with high sea or urban square proportions.

## Estimation and uncertainty
- Estimates are produced using ratio estimation techniques for each land class, weighting by the vegetative land area within each land class.
- Weights are based on the vegetative land area of each land class as a whole.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to concerns about skewness in some features.

## Implications for GIS use
- Recognize non-random, stratified sampling when interpreting spatial estimates and making comparisons across regions or classes.
- Apply the appropriate land-class weights and account for stratification to obtain representative spatial estimates.
- Be mindful of confidentiality limits when attempting to map or reproduce data at fine spatial scales; some precise-location information is not available.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.