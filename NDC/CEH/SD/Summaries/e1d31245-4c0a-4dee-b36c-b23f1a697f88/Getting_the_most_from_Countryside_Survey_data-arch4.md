# Notes on the downloadable data

## Overview
- Describes confidentiality protections, sampling design, data structure, and estimation methods for Countryside Survey (CS) field data used in GB.

## Data structure and sampling design
- Data come from a sample of 1 km squares in Great Britain; each square is mapped and measured at two levels: the square itself and features within the square.
- Measurements include a mix of binary and continuous variables (e.g., areas, lengths).
- The CS sample is not a random subset; it is stratified by the ITE Land Classification, with country-specific classifications (England 21 classes, Wales 8, Scotland 16).
- From 1998 onward, stratification is essential for estimating land-class statistics and their variation.

## Confidentiality and scope
- To preserve representativeness, precise locations of CS survey squares are kept confidential by CEH and are limited to 100 square km precision for external users.
- This limitation means users cannot determine whether specific survey squares fall within particular defined areas below the 100 sq km threshold.

## Exclusion criteria and representativeness
- Squares excluded from field survey if >90% sea or >75% urban at 1:250,000 OS map scale.
- Official estimates assume similarity between vegetative land in excluded squares and sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.

## Estimation and inference
- Estimates by land class are produced using ratio estimators that weight by vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani), addressing skewness concerns in some features.

## Implications for analysis and data management
- Analyses must account for stratification by land class to obtain representative estimates and correct measures of variation.
- Extrapolation to the whole GB requires careful consideration of the exclusion criteria and the similarity assumption for excluded areas.
- Data governance should document location privacy, sampling design, weighting scheme, and bootstrap-based uncertainty.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.