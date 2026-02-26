# Notes on the downloadable data

- Purpose and confidentiality
  - To preserve representativeness of the wider countryside, the precise locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users will not have location precision finer than 100 square km, so it's not possible to identify whether specific survey squares fall within defined areas below that threshold.

- Sampling design and data structure
  - Field data come from a sample of 1-km squares across Great Britain (GB).
  - Each selected square is mapped and detailed measurements are taken within the square (e.g., quadrats for vegetation, soils, etc.).
  - Two levels of sampling: whole square and within-square measurements.
  - Not a random subset; the sample is stratified within Land Classification strata defined by ITE.
  - Land Classification class counts have changed over time:
    - Originally 32 classes; expanded to 42 in 1998 for country reporting; 45 classes after 2007 for Wales reporting.
    - England: 21 classes, Wales: 8 classes, Scotland: 16 classes (country-specific classifications).
  - Exclusions: Squares with area more than 90% sea or more than 75% urban were excluded from survey.
  - Practical implication: field survey data are representative only of the included squares; extrapolations to GB or regions assume vegetative land in excluded squares is similar to sampled squares (bias is generally small but may be problematic in regions with high sea/urban composition).

- Estimation and analysis
  - Estimates are produced using ratio estimation for each land class, weighting by the vegetative land area within each square.
  - To obtain uncertainty measures, standard errors and confidence intervals are computed using bootstrap methods (since 1998) due to skewness in some features.

- Implications for data users and governance (Data Steward perspective)
  - When using the data, account for stratification by Land Classification and the area-based weighting.
  - Recognize representativeness limitations due to exclusions and the non-random sampling design.
  - Use bootstrap-based uncertainty measures for robust inference.
  - Documentation and methods are anchored in established references; ensure transparency in analyses and reporting.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.