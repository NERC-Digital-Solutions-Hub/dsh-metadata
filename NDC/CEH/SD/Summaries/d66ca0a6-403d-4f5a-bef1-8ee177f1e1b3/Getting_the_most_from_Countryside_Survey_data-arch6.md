# Notes on the downloadable data

- Purpose: Provide guidance on how Countryside Survey (CS) field survey data should be used and interpreted, including sampling design, representativeness, and estimation methods.

- Geographic confidentiality:
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users can only identify square locations to a resolution no finer than 100 square km.
  - This prevents identifying whether specific survey squares fall within defined areas below this threshold.

- Sampling design and data structure:
  - CS data come from a sample of 1 km squares across Great Britain (GB).
  - There are two levels of sampling:
    - Whole square: mapped and characterised.
    - Within-square: detailed measurements (e.g., quadrats for vegetation, soils).
  - Measurements vary from binary to continuous (areas, lengths).

- Non-random, stratified sampling:
  - The sample is not a random subset of all GB squares.
  - It is stratified by the ITE Land Classification, with country-specific adaptations.
  - Country classifications have evolved:
    - England: 21 land classes
    - Wales: 8 land classes
    - Scotland: 16 land classes
  - Estimates that do not account for stratification may be biased or have incorrect variation estimates.

- Exclusions and representativeness:
  - Squares with area > 90% sea or > 75% urban (per 1:250,000 OS maps) were excluded from the field survey.
  - Official GB estimates assume excluded vegetative land is similar in composition to sampled squares; while not exact, the bias is likely small unless a region has a high proportion of sea/urban squares.

- Estimation approach:
  - Estimates are produced using ratio estimation (Cochran, 1963) for each land class, weighted by the vegetative land area in each class.
  - Land class estimates are combined using the area of vegetative land in the class as weights.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.

- Practical implications for analysis and use:
  - When analysing CS data, incorporate stratification by land class to obtain unbiased estimates and correct uncertainty.
  - Be cautious with extrapolations to GB or regions if they include many excluded (sea/urban) squares.
  - Use the bootstrap-based confidence intervals for robust uncertainty assessment.
  - Be mindful that precise geographic identification is limited; analyses should rely on land-class and vegetative-area weights rather than exact square locations. 

- References:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap