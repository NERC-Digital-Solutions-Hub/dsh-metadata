# Notes on the downloadable data

- Confidentiality and precision
  - UKCEH keeps the precise locations of CS survey squares confidential.
  - External users will not be given location precision finer than 100 square km.
  - You cannot identify whether any survey squares fall within defined areas below this threshold.

- Sampling framework
  - Countryside Survey (CS) field data come from a sample of 1 km squares in Great Britain.
  - Each selected square is mapped and detailed measurements are taken at two levels: the whole square and within-square features.
  - Measurements include binary variables and continuous measures (areas, lengths, etc.).

- Stratification and classification
  - The sample is not random; it is stratified by the ITE Land Classification.
  - Land Classification has evolved: originally 32 classes; 1998 expanded due to Scotland reporting to 42; 2007 revised for Wales reporting to 45 total classes.
  - Each country now has its own set of classes: England (21), Wales (8), Scotland (16).

- Representativeness and implications
  - Estimates derived without accounting for stratification may be unrepresentative and misstate variation.
  - Official GB or regional estimates assume vegetative land in excluded squares is similar to that in sampled squares.
  - Excluded squares are those with area >90% sea or >75% urban (per 1:250,000 OS maps); such exclusions may bias regional estimates only if a region has a high proportion of sea/urban squares.

- Estimation and uncertainty
  - Official estimates are produced using ratio estimates (Cochran 1963) for each land class, weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani 1993).

- Practical references
  - Barr et al. 1993. Countryside Survey 1990 Main Report.
  - Cochran 1963. Sampling Techniques.
  - Efron & Tibshirani 1993. An Introduction to the Bootstrap.