# Notes on the downloadable data

- Purpose and privacy
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey (CS) squares are held in confidence by UKCEH.
  - External users will not be provided location precision finer than 100 square km; cannot identify whether survey squares fall within defined areas below this threshold.

- Sampling design
  - CS Field Survey data come from a sample of 1 km squares in Great Britain.
  - Each square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils).
  - Measurements include both binary and continuous variables.
  - The sample is not a random subset; it is stratified by the ITE Land Classification.
  - Land Classification details:
    - Original 32 classes; expanded to 42 classes in 1998 for Scotland; 45 classes in 2007 for Wales.
    - Separate classifications exist for England (21 classes), Wales (8), Scotland (16).

- Representation and implications
  - Estimates derived from CS data must account for stratification; analyses that ignore stratification may be unrepresentative and have inaccurate variation estimates.

- Exclusions and potential bias
  - Squares where land area is more than 90% sea or more than 75% urban were excluded from field survey.
  - Official estimates assume vegetative land composition in excluded squares is similar to sampled squares; bias is generally negligible unless a region has a high proportion of sea or urban squares.

- Estimation and uncertainty
  - Because of the sampling design, ratio estimates are used for land-class estimates, weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals have been estimated using the bootstrap to address skewness in some features.

- References
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap