# Notes on the downloadable data

- Purpose and representativeness
  - Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain.
  - Data are designed to preserve representativeness of the wider countryside; precise square locations are kept confidential to external users (no greater precision than 100 square km).

- Confidentiality and location privacy
  - Public access is limited to maintain representativeness; exact square coordinates are not disclosed beyond the 100 sq km threshold.

- Sampling design and levels
  - Two levels of sampling: whole squares and within-square features.
  - Measurements are collected at both levels (e.g., square-level characterisations and within-square vegetation/soil measurements).
  - Data types range from binary variables to continuous measures (areas, lengths, etc.).

- Non-random, stratified sampling
  - CS squares are not a random subset of all GB squares.
  - The sample is stratified by land class, defined by the ITE Land Classification.
  - Country-specific revisions have led to different classifications: 21 classes in England, 8 in Wales, 16 in Scotland, with historical changes (32 → 42 → 45 classes).

- Exclusion criteria and implications
  - Squares with >90% sea area or >75% urban area (by 1:250,000 OS map area) were excluded from field survey.
  - Official GB estimates assume non-sampled vegetative land in excluded squares is similar to sampled squares; bias is generally small unless a region has a high proportion of sea/urban squares.

- Estimation methodology
  - Estimates are produced as ratio estimates (Cochran, 1963) for each land class, weighting by vegetative land area within squares.
  - Land-class estimates are combined using weights equal to the total vegetative land area for each land class.

- Uncertainty and standard errors
  - Due to skewness concerns, standard errors and confidence intervals have been estimated using bootstrap methods since 1998 (Efron and Tibshirani, 1993).

- Data quality, governance, and reuse
  - The approach involves ensuring metadata, data quality, and transparent reporting.
  - Data are typically used to derive findings presented in reports, charts, or dashboards; openness and data management standards are important.
  - When using the data, analysts should account for stratification, inclusion/exclusion criteria, and the weighting scheme to avoid biased inferences.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.