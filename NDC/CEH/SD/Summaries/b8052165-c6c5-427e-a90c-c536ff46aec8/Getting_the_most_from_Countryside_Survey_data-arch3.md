# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a stratified sample of 1 km squares in Great Britain, with measurements at two levels: whole squares and within-square features.
- Measurements vary in type, from binary to continuous.

## Confidentiality and location precision
- To preserve representativeness of the broader countryside, precise locations of CS survey squares are kept confidential by CEH.
- External users cannot identify whether squares fall within defined areas with precision finer than 100 square kilometers.

## Sampling design
- The sample is not random; it is stratified by the ITE Land Classification.
- Country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16) due to separate country reporting.
- Estimates that ignore stratification may be unrepresentative and misrepresent variation.

## Exclusions and representativeness
- Squares with more than 90% sea or more than 75% urban area were excluded from field survey.
- Official GB estimates are based on the surveyed subset; extrapolation to GB assumes vegetative land in excluded squares is similar to sampled squares, which may introduce bias if a region has a high proportion of sea/urban squares.
- Bias due to exclusion is considered likely negligible unless a region contains a large share of sea or urban land.

## Estimation and uncertainty
- Estimates are produced using ratio estimation for each land class, weighted by the vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods to address skewness.

## Data usage considerations for monitoring frameworks
- Analyses must account for the stratified sampling design and the exclusions when interpreting results.
- Metadata quality and the need to handle confidential location information can affect data use and reproducibility.
- Bootstrap-based uncertainty estimates should be used for inference.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.