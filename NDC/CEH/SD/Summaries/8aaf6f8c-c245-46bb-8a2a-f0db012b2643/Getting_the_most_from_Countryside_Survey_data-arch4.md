# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify squares with precision finer than 100 square km.
- CS Field Survey data are collected from a sample of 1 km squares in Great Britain, with measurements at both the square level and within-square features (binary and continuous variables).

- Sampling design and representativeness:
  - The sample is not random; it is stratified within designated strata defined by the ITE Land Classification.
  - Land Classification details have evolved by country: England (21 classes), Wales (8 classes), Scotland (16 classes); changes reflect country-specific reporting requirements.
  - Estimates without accounting for stratification may be non-representative and have incorrect variation estimates.

- Excluded squares and scope:
  - Squares with area more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) were excluded from field surveys.
  - Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; bias is expected to be small unless a region has a high proportion of sea or urban squares.

- Estimation method:
  - Estimates are produced as ratio estimates for each land class, weighted by the area of vegetative land in each class.
  - Land-class estimates are combined using weights corresponding to the vegetative land area of each class.
  - Since some features are skewed, standard errors and confidence intervals have been estimated using bootstrap methods since 1998.

- Uncertainty and references:
  - Bootstrap approach for uncertainty: Efron and Tibshirani (1993).
  - Key references: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) Bootstrap.

- Practical implications for data users:
  - Analyses must account for the stratified sampling design and applied weights when making inferences about GB or regional areas.
  - Be aware of the limited precision location data and the exclusions that affect representativeness.
  - Use bootstrap-derived uncertainty measures for robust inference.