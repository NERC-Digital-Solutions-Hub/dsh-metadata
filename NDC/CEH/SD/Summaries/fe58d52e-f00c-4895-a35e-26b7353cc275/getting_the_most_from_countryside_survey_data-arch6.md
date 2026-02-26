# Notes on the downloadable data

- Confidentiality of locations: Precise locations of Countryside Survey squares are kept confidential by UKCEH; external users cannot identify square locations to any precision finer than 100 square km, making it impossible to determine whether squares fall within defined areas below this threshold.

- Sampling design and levels: Countryside Survey (CS) field data come from a sample of 1-km squares in GB; measurements are taken at two levels—whole square and within-square—covering a range of data types from binary to continuous.

- Non-random, stratified sampling: The CS sample is not a random subset of all GB 1-km squares. It is stratified by the ITE Land Classification, with country-specific classifications (England 21 classes, Wales 8, Scotland 16; total 45 classes). Estimates that ignore stratification may be non-representative and have inaccurate variation.

- Exclusions and representativeness: Not all potential squares were surveyed; squares with more than 90% sea area or more than 75% urban area were excluded. Official GB estimates assume that vegetative land in excluded squares is similar to sampled squares; bias is generally negligible except in regions with high sea/urban proportions.

- Estimation methods: Estimates by land class are produced using ratio estimates that account for vegetative land area in each sample square. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.

- Practical implications for analysis:
  - Weight analyses by vegetative land area within each land class.
  - Incorporate stratification by country/class when estimating variability.
  - Use bootstrap-based standard errors and confidence intervals.
  - Be cautious when generalizing to GB-wide or regional scales, especially in areas with high sea or urban square prevalence.
  - Recognize the two-level sampling when designing models or interpreting features characterizing entire squares versus within-square details.

- References:
  - Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.