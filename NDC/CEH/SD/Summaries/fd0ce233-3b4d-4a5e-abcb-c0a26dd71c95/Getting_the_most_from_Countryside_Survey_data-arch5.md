# Notes on the downloadable data

- Confidentiality of locations
  - Exact locations of Countryside Survey (CS) survey squares are held in confidence by CEH.
  - External users will not be provided with precision finer than 100 square kilometres; users cannot identify whether squares fall within defined areas below this threshold.

- Sampling design and data structure
  - CS field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Two levels of sampling: the square level (mapping and measurements) and within-square level (quadrats for vegetation, soils, etc.).
  - Measurements include a mix of binary and continuous variables (e.g., areas, lengths).

- Non-random, stratified sampling
  - Squares are not a random subset; sampling is stratified by land classification (ITE Land Classification).
  - Classification history and country-specific adaptations:
    - Original 32 classes; expanded to 42 in 1998 for Scotland reporting needs; further revised to 45 classes in 2007 for Wales reporting.
    - England, Wales, and Scotland have separate classifications (England: 21 classes, Wales: 8, Scotland: 16).
  - Analyses that do not account for stratification may yield biased estimates of variation.

- Exclusions and representativeness
  - Squares with area more than 90% sea or more than 75% urban were excluded from field survey.
  - Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; bias is generally negligible, unless a region has a high proportion of sea/urban squares.

- Estimation methods and weights
  - Estimates by land class are calculated using ratio estimates, incorporating vegetative land area within each class.
  - Land class estimates are combined using weights equal to the vegetative land area of each class.

- Uncertainty and inference
  - From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in features.

- Data governance and metadata implications for Data Stewards
  - Ensure metadata documents acknowledge:
    - Confidentiality constraints on square locations.
    - The two-level sampling design and its impact on analyses.
    - Stratification by country-specific land classifications and the associated weights.
    - Exclusion criteria and their effect on representativeness.
    - The use of ratio estimates and bootstrap-based uncertainty estimates.
  - Guidance for users on proper handling of weights, stratification, and extrapolation beyond sampled squares.

- References for methodological context
  - Barr et al. (1993) Countryside Survey 1990 Main Report.
  - Cochran (1963) Sampling Techniques.
  - Efron and Tibshirani (1993) An Introduction to the Bootstrap.