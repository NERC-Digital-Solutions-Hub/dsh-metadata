# Notes on the downloadable data

- Confidentiality of survey locations: The precise locations of Countryside Survey (CS) field survey squares are held in confidence by CEH to preserve representativeness. External users cannot identify squares with better precision than 100 square km, so it is not possible to determine whether any survey squares fall within defined areas below this threshold.

- CS sampling design and scope:
  - Data come from a sample of 1 km squares across Great Britain (GB). Each selected square is mapped and measured at both the square level and within-square features (e.g., quadrats for vegetation and soils).
  - Measurements span binary and continuous variables across two levels: whole square and within-square.

- Non-random, stratified sampling:
  - Squares are not a random subset; sampling is stratified by country-specific Land Classification (ITE). The classification has evolved from 32 to 42 to 45 classes due to separate country reporting, resulting in 21 classes in England, 8 in Wales, and 16 in Scotland.
  - Estimates derived without accounting for stratification may be unrepresentative and misestimate variation.

- Coverage and exclusions:
  - Not all GB squares were surveyed. Squares with area more than 90% sea or more than 75% urban (as measured on 1:250,000 OS maps) were excluded.
  - In practice, GB-wide estimates assume vegetative land in excluded squares is similar to sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.

- Estimation method and weighting:
  - Official estimates are produced using ratio estimation (per land class) that accounts for the vegetative land area within each sample square.
  - Land class estimates are combined using weights equal to the vegetative land area of each land class overall.

- Uncertainty and inference:
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features (Efron and Tibshirani).

- Practical implications for analysts:
  - Incorporate the stratified sampling design and land-class weights when analyzing CS data.
  - Use bootstrap-based standard errors and confidence intervals for uncertainty assessment.
  - Be cautious about extrapolating from sampled squares to the whole GB, especially in regions with substantial sea or urban areas.
  - Recognize limitations imposed by location confidentiality when mapping or performing highly spatially resolved analyses.

- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.