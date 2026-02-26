# Notes on the downloadable data

- Representativeness and confidentiality
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey (CS) field survey squares are confidential and not identifiable to external users with precision finer than 100 square km.
  - Users cannot determine whether any survey squares fall within defined areas below this threshold.

- Sampling design and data structure
  - CS Field Survey data come from a sample of 1 km squares in Great Britain (GB). Each selected square is mapped and detailed measurements are taken at two levels: the whole square and within-square (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include varied types, from binary to continuous variables (areas, lengths).

  - The sample is not a random subset; it is stratified by the ITE Land Classification. Country-specific classifications have evolved: originally 32 classes, expanded to 42 in 1998 for Scotland reporting, and to 45 in 2007 for Wales reporting. England has 21 classes, Wales 8, Scotland 16.
  - Estimates that do not account for stratification may be unrepresentative and have inaccurate variation estimates.

- Exclusions and representativeness caveats
  - Not all GB squares were considered for field survey. Squares whose area (from 1:250,000 OS maps) was more than 90% sea or more than 75% urban were excluded.
  - Official GB estimates are based on the surveyed squares but assume vegetative land in excluded squares is similar to sampled squares. This assumption may introduce bias only if a region has a high proportion of sea or urban squares.

- Estimation methods and uncertainty
  - Estimates are produced using ratio estimation (Cochran, 1963) for each land class, weighted by the vegetative land area in each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993).

- Practical implications for users
  - Analyses should account for stratification and the sampling design; avoid treating data as a simple random sample.
  - Bootstrap methods are recommended for uncertainty estimation, reflecting the sampling framework.

- References
  - Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.