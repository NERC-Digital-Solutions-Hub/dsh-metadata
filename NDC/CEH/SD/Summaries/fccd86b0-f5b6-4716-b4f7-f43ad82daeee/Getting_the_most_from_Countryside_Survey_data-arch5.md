# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data are collected from a sample of 1 km squares across Great Britain, with two levels of measurement: the square and features within the square.
- To preserve representativeness, precise square locations are kept confidential; external users cannot identify squares with precision finer than 100 square kilometers.
- Estimates are produced using stratified sampling and specialized weighting and estimation methods due to the non-random, country-specific sampling design.

## Data confidentiality and access
- Exact coordinates of survey squares are restricted; location precision is limited to 100 square kilometers to protect representativeness.
- This confidentiality means users cannot determine whether specific squares fall within defined areas below the 100 km² threshold.

## Sampling design
- Two levels of sampling: the entire 1 km square and measurements within each square (e.g., quadrats for vegetation, soils, etc.).
- The sampling is non-random but stratified by land classification (ITE Land Classification), with country-specific revisions:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Land classification classification evolved from 32 classes (original) to 42 (1998) to 45 (2007) to accommodate country reporting.
- Not all GB squares were considered for field survey; exclusion criteria include squares >90% sea or >75% urban by area on 1:250,000 OS maps.
- In practice, GB-wide estimates assume excluded areas are similar in vegetative composition to sampled squares; bias is considered small except in regions with high sea/urban proportions.

## Representativeness and limitations
- Estimates for GB or regions depend on ratio estimations by land class and the area of vegetative land per class.
- Stratification and exclusions mean that simple, unstratified analyses may be biased; analyses should account for stratified design and weighting.

## Estimation methods and uncertainty
- Estimates of land class are derived via ratio estimation (Cochran, 1963) using the vegetative land area as weights.
- Standard errors and confidence intervals are computed using bootstrap methods due to skewness concerns (since 1998).

## Practical implications for data users
- Datasets include both presence/absence (binary) and continuous measures (e.g., areas, lengths).
- Users must account for the stratified design and potential biases from excluded squares when making inferences about GB or regional scales.
- When reusing data, apply the appropriate weights and consider bootstrap-derived uncertainty measures to reflect the sampling design.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.