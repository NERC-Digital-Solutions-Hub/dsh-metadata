# Notes on the downloadable data

- Privacy and data precision
  - Precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
  - External users cannot identify square locations with precision better than 100 square km.
  - This prevents identifying whether survey squares fall within defined areas below this threshold.

- Sampling design and data structure
  - CS Field Survey data come from a sample of 1 km squares across Great Britain.
  - Each selected square is mapped and measured at two levels: the whole square and within-square features.
  - Measurements include binary and continuous variables (e.g., areas, lengths).

- Stratification and classification
  - The sample is not a random subset; it is stratified within designated strata defined by the ITE Land Classification.
  - Land Classification has evolved: originally 32 classes, then 42 (1998, Scotland reporting), then 45 (2007, Wales reporting).
  - Current country-specific classifications: England 21 classes, Wales 8, Scotland 16.

- Representativeness and sampling implications
  - Estimates derived without accounting for stratification may be unrepresentative and have biased variation estimates.
  - Official GB estimates are produced using ratio estimates by land class, weighted by vegetative land area in each class.

- Exclusions and coverage
  - Squares with more than 90% sea or more than 75% urban area were excluded from field survey (as of 1990 reference).
  - Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; this may introduce bias if regional sea/urban proportions are high.

- Estimation and uncertainty
  - After 1998, standard errors and confidence intervals are estimated using the bootstrap method (Efron and Tibshirani, 1993) due to concerns about skewness.

- References
  - Barr et al. (1993) Countryside Survey 1990 Main Report.
  - Cochran (1963) Sampling Techniques.
  - Efron and Tibshirani (1993) An Introduction to the Bootstrap.