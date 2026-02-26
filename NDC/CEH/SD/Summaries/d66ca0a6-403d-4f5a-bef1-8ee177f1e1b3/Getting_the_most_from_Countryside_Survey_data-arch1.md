# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at two levels: per square and within-square features (including quadrats, vegetation, soils, etc.).
- Measurements include binary and continuous variables; sampling design affects how analyses should be conducted.

## Location confidentiality
- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify square locations with precision better than 100 square kilometres, meaning you cannot determine whether squares fall within defined, smaller areas.

## Sampling design and representativeness
- The CS sample is stratified rather than random, using the ITE Land Classification.
- Land classes have evolved by country: England (21 classes), Wales (8), Scotland (16); overall classifications changed from 32 to 42 (1998) and to 45 (2007) due to country-specific reporting.
- Estimates derived from CS data without accounting for stratification may be biased or have incorrect measures of variation.

## Excluded squares and extrapolation
- Squares whose area is >90% sea or >75% urban are excluded from field surveys.
- Official GB estimates are produced by ratio estimates across land classes, weighted by the vegetative land area in each class.
- To extrapolate to the whole GB, it is assumed that vegetative land in excluded squares is similar to sampled squares; bias is generally small unless a region has a high proportion of sea or urban squares.

## Estimation and uncertainty
- Because of skewness, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) from 1998 onward.
- Area-weighted combination of land-class estimates is used to produce GB-level estimates.

## Data handling and references
- Key methodological references: Barr et al. (1993) for the 1990 Main Report; Cochran (1963) on sampling techniques; Efron & Tibshirani (1993) on bootstrap methods.