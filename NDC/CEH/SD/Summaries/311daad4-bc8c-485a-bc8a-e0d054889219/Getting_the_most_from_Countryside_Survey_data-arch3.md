# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users will not be provided with location precision better than 100 square km.
- This confidentiality means users cannot determine whether survey squares fall within defined areas below the threshold.

## Sampling design and data structure
- CS Field Survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels: the whole square and features within the square.
- Measurements are varied (binary and continuous) and include detailed vegetation, soils, etc.
- The sample is not random; it is stratified by the ITE Land Classification. Classifications have evolved:
  - Originally 32 land classes.
  - 1998: Scotland reporting requirements expanded to 42 classes.
  - 2007: Wales reporting requirements expanded to 45 classes.
  - Each country effectively has its own classification: England (21), Wales (8), Scotland (16).
- Not all GB squares were considered for field survey; excluded if the area on 1:250,000 OS maps was more than 90% sea or more than 75% urban.
- Official GB estimates assume vegetative land in excluded squares is similar in composition to sampled squares; bias is likely negligible except in regions with high sea/urban proportions.

## Estimation and uncertainty
- Estimates by land class are calculated as ratio estimates (Cochran, 1963) using the area of vegetative land in each sample square.
- Land class estimates are combined using weights equal to the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness concerns.

## Implications for monitoring and analysis
- Analyses must account for stratification by land class to avoid biased estimates.
- The non-random, stratified design means results may not be representative if the design is ignored.
- Excluded squares and confidentiality constraints should be considered in any spatial or regional extrapolations.
- When using CS data, be mindful of potential data transformation needs to make measurements usable.
- Transparent data governance and data sharing practices are important, given the public-sharing expectations and metadata considerations.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.