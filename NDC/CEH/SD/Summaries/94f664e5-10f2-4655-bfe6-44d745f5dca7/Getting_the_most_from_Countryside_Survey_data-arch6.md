# Notes on the downloadable data

- Confidentiality and geolocation
  - Precise locations of Countryside Survey (CS) squares are kept confidential by CEH.
  - External users cannot identify square locations with precision finer than 100 square km.
  - This limits ability to determine whether squares fall within defined areas below that threshold.

- Sampling design and data structure
  - CS field survey data come from a sample of 1 km squares in Great Britain.
  - Two sampling levels: the square as a unit and within-square measurements (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include a mix of binary and continuous variables.

- Stratified sampling and classification
  - Squares are not a random subset; the sample is stratified by ITE Land Classification.
  - Country-specific classifications: England (21 classes), Wales (8), Scotland (16), totaling 45 classes across the three countries.
  - Analyses must account for stratification; ignoring it yields biased estimates of variation.

- Exclusions and representativeness
  - Squares with more than 90% sea area or more than 75% urban area (per 1:250,000 OS maps) were excluded from field survey.
  - Official estimates for GB or regions assume excluded areas have similar vegetative land composition to sampled squares.
  - Potential bias could arise if a region contains a high proportion of sea or urban squares; otherwise the bias is expected to be small.

- Estimation approach
  - Estimates are produced as ratio estimates by land class, weighting by the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani).

- Practical implications for data users
  - When analyzing CS data, incorporate stratification by land class and use area-based weights.
  - Treat the data as representative only of the included squares (not all GB squares); be cautious with GB-wide extrapolations.
  - Use bootstrap-derived uncertainty measures for more robust inferences.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.