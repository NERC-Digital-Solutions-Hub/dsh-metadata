# Notes on the downloadable data

- Overview
  - Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements taken at both the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Data are used to support environmental monitoring, reporting, and decision-making, requiring awareness of sampling design and data provenance.

- Sampling design and levels
  - Two levels of sampling: the whole square and within-square measurements.
  - Measurements include binary and continuous variables, varying in type and scale.
  - The sample is not a random subset of all GB squares; it is stratified within designated strata.

- Stratification and land classification
  - Stratification is defined by the ITE Land Classification, with country-specific classifications:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Since 1998, classifications have been adjusted for separate country reporting (32 → 42 classes in 1998; 45 classes after Wales reporting changes in 2007).

- Exclusions and representativeness
  - Squares where the map area is more than 90% sea or more than 75% urban were excluded from field survey.
  - Official estimates for GB or regions assume excluded vegetative land is similar in composition to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

- Handling of estimates and weights
  - Estimates for land classes are produced as ratio estimates (Cochran, 1963) and are weighted by the vegetative land area within each land class.
  - Given stratification, estimates that ignore strata can be biased or misrepresent variation.

- Uncertainty and standard errors
  - From 1998 onward, standard errors and confidence intervals are estimated using the bootstrap (Efron and Tibshirani, 1993) due to concerns about skewness in some features.

- Data confidentiality and accessibility
  - To preserve representativeness, precise CS survey square locations are kept confidential by UKCEH.
  - External users cannot identify survey squares with precision finer than 100 square kilometers, which limits exact geographic pinpointing within defined areas.

- Data quality, metadata, and transformation
  - Metadata may be incomplete or require effortful transformation to be usable; some data may need cleaning or reformatting before analysis.
  - Ensuring data quality, openness, and appropriate data management standards is important at the source, with clear documentation for users.

- Practical guidance for monitoring and analysis
  - Account for stratification (land class) and use appropriate weights tied to vegetative land area when aggregating estimates.
  - Use bootstrap-based uncertainty estimates to reflect sampling variability and potential feature skewness.
  - Be mindful of the non-random sampling design when interpreting results and making inferences for the whole GB.
  - When communicating findings, clearly reflect the sampling design, exclusions, and uncertainty.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.