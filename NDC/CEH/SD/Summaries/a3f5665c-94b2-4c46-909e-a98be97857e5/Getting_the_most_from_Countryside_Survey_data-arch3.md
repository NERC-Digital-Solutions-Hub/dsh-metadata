# Notes on the downloadable data

- Purpose and confidentiality
  - Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain.
  - To preserve representativeness, precise square locations are kept confidential; external users cannot identify squares with precision better than 100 square km.

- Data collection and measurements
  - Each selected square is mapped and detailed measurements are taken at two levels: the whole square and features within the square.
  - Measurements include a mix of binary (yes/no) and continuous variables (areas, lengths, etc.).

- Sampling design
  - The CS sample squares are not a random subset; they are stratified within designated strata.
  - Strata are defined by the ITE Land Classification, with country-specific classifications:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - The Land Classification has been revised over time for country reporting (from 32 to 45 classes across changes in Scotland/Wales/England).

- Exclusions and representativeness
  - Squares with more than 90% sea area or more than 75% urban area were excluded from field survey.
  - Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; bias is expected to be negligible unless a region has a high proportion of sea or urban squares.

- Estimation and inference
  - Official GB estimates are produced using ratio estimates for each land class, weighted by the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated via bootstrap methods due to skewness in some features.

- Implications for users
  - Analyses must account for the stratified sampling design and weighting.
  - Exclusions and assumptions about similarity between included and excluded squares affect representativeness, particularly for regional extrapolations.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.