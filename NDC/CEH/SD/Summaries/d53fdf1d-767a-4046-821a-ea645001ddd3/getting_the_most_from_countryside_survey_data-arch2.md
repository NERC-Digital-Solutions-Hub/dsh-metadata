# Notes on the downloadable data

- Confidentiality and representativeness
  - Precise locations of Countryside Survey squares are kept confidential by UKCEH to preserve representativeness of the wider countryside.
  - External users cannot identify survey squares with precision finer than 100 square km.
  - Consequently, it is not possible to determine whether any survey squares fall within defined areas below this threshold.

- Sampling design and data structure
  - Countryside Survey field data come from a sample of 1-km squares in GB, with measurements taken at two levels: whole squares and within-square features.
  - Measurements include binary and continuous variables (e.g., vegetation, soils) derived from surveys and quadrats.
  - The sample is not a random subset; it is stratified within the ITE Land Classification. Country-specific classifications exist: 21 land classes in England, 8 in Wales, and 16 in Scotland.
  - Estimates must account for stratification; ignoring it can lead to non-representative results and incorrect variation estimates.

- Exclusion criteria and representativeness
  - Squares with more than 90% sea area or more than 75% urban area were excluded from field survey.
  - Official GB estimates assume excluded squares are similar in vegetative land composition to sampled squares; while this is not perfect, the excluded land area is small, minimizing bias except in regions with high sea/urban proportions.

- Estimation and uncertainty
  - Land-class estimates are obtained via ratio estimates that weight by the vegetative land area within each square.
  - Land-class estimates are combined using weights equal to the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to concerns about skewness in some features.

- References
  - Barr et al. (1993) Countryside Survey 1990 Main Report.
  - Cochran (1963) Sampling Techniques.
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap.