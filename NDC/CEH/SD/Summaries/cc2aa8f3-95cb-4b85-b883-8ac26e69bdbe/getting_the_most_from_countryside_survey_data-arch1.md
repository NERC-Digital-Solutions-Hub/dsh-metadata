# Notes on the downloadable data

- Data confidentiality: The precise locations of Countryside Survey (CS) survey squares are kept confidential by UKCEH; external users cannot identify squares with precision better than 100 square km, preventing determination of whether squares fall within defined areas.

- Sampling design and data structure:
  - CS Field Survey data come from a sample of 1 km squares across GB.
  - Each selected square is mapped, with measurements made at two levels: the square level and within-square (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include binary and continuous variables (e.g., areas, lengths).

- Non-random, stratified sampling:
  - The sample is not a random subset of GB squares; it is stratified by the ITE Land Classification.
  - Country-specific classifications exist: 21 land classes in England, 8 in Wales, and 16 in Scotland, totaling 45 land classes across the UK.
  - Estimates that do not account for stratification may be unrepresentative and have inaccurate variation estimates.

- Exclusions and representativeness:
  - Squares with more than 90% sea or more than 75% urban area were excluded from field survey.
  - Official GB or regional estimates assume excluded squares have vegetative land composition similar to sampled squares; bias is considered small unless a region has many sea/urban squares.

- Estimation method:
  - Estimates are produced using ratio estimation (Cochran 1963) for each land class.
  - Weights are based on the area of vegetative land within each land class.

- Uncertainty and inference:
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani 1993) to address skewness in some features.

- References:
  - Barr et al. (1993) Countryside Survey 1990 Main Report.
  - Cochran (1963) Sampling Techniques.
  - Efron and Tibshirani (1993) An Introduction to the Bootstrap.