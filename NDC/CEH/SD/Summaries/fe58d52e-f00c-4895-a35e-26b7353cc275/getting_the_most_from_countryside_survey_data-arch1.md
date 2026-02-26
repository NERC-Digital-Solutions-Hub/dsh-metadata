# Notes on the downloadable data

- Confidentiality and precision
  - The exact locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users cannot identify whether survey squares fall within defined areas at any precision finer than 100 square km.

- Sampling design and structure
  - Field data come from a sample of 1-km squares across GB.
  - Each selected square is mapped and measured both at the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include binary and continuous variables, spanning several data types.

- Stratification and classifications
  - Squares are not a random subset; they are stratified within designated strata.
  - Stratification is defined by the ITE Land Classification, with country-specific adjustments:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - The land classification evolved over time (initially 32 classes; 1998 updated to 42; 2007 Welsh reporting led to 45 classes). Each country effectively has its own classification system for reporting.

- Exclusions and representativeness
  - Squares with more than 90% sea or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field survey.
  - The field survey data are representative only of the included squares.
  - GB estimates or regional estimates are typically extrapolated assuming the vegetative land composition in excluded squares is similar to sampled squares; bias is generally small unless a region has a high proportion of sea or urban squares.

- Estimation and inference
  - Estimates for land classes are produced using ratio estimation, weighting by the area of vegetative land in each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani).

- Practical considerations for analysts
  - Always account for stratification and weighting when analyzing CS data.
  - Be cautious with extrapolations to areas with many excluded squares (e.g., high sea/urban proportions).
  - Use bootstrap-derived standard errors to quantify uncertainty, particularly given potential skewness in features.

- References
  - Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.