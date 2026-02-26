# Notes on the downloadable data

## Overview of data confidentiality and sampling scope
- Precise locations of Countryside Survey (CS) field survey squares are confidential and not identified to external users with precision better than 100 square km.
- This confidentiality means users cannot determine whether specific survey squares fall within defined areas below the threshold.

## Sampling framework and levels
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels: the whole square and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Measurements are of varied types, from binary to continuous.
- The sample is not random; it is stratified by land classification (ITE Land Classification). Country-specific classifications exist: England (21 classes), Wales (8 classes), Scotland (16 classes) due to reporting needs.
- Two-stage sampling implications: estimates must account for stratification to be representative and to correctly reflect variation.

## Representativeness and exclusions
- Estimates derived from CS data without accounting for stratification may be unrepresentative and misstate variation.
- Not all GB squares were considered for field survey. Squares that are more than 90% sea or more than 75% urban were excluded (details in the 1990 Main Report).
- Official GB or regional estimates assume vegetative land in excluded squares is similar in composition to sampled squares. This is usually a small bias, but can be problematic in regions with high sea or urban proportions.

## Estimation and uncertainty practices
- Estimates by land class are produced using ratio estimation, weighted by the vegetative land area in each land class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods to address skewness in some features.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.