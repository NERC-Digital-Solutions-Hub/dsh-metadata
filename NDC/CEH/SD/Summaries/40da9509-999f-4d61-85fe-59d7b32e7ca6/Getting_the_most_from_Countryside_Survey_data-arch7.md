# Notes on the downloadable data

- Location precision and confidentiality
  - Precise locations of Countryside Survey (CS) field squares are kept confidential by CEH.
  - External users cannot identify whether a survey square falls within defined areas with precision better than 100 square kilometres.
  - Therefore, users cannot determine square-level inclusion within certain areas below this threshold.

- Sampling design and data structure
  - CS field data come from a sample of 1 km squares across Great Britain (GB).
  - Two sampling levels: whole squares and within-square measurements (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include a range of types from binary to continuous (areas, lengths, etc.).

- Representativeness and non-random sampling
  - The sample is not a random subset of GB squares; it is stratified by ITE Land Classification.
  - Country-specific classifications exist (England: 21 classes; Wales: 8; Scotland: 16; total changed from 32 → 45 classes over time).
  - Analyses that ignore stratification may yield non-representative estimates and incorrect variance.

- Excluded squares and implications for coverage
  - Squares with more than 90% sea or more than 75% urban area were excluded from field survey.
  - Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares.
  - Potential bias is likely small unless a region has a high proportion of sea/urban squares.

- Estimation methods
  - Estimates are produced using ratio estimation for each land class, weighted by the vegetative land area of that class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods.

- References for methodological background
  - Barr et al. 1993 (Countryside Survey 1990 Main Report)
  - Cochran 1963 (Sampling Techniques)
  - Efron & Tibshirani 1993 (Bootstrap)