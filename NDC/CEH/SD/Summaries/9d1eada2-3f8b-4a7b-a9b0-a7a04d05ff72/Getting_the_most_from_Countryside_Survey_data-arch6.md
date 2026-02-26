# Notes on the downloadable data

- Confidentiality of locations
  - Precise locations of CS survey squares are held in confidence by CEH.
  - External users are not provided with precision better than 100 square km.
  - This prevents identification of whether survey squares fall within defined areas below the 100 sq km threshold.

- Sampling considerations in Countryside Survey Data
  - Field Survey data come from a sample of 1 km squares in Great Britain, with two sampling levels: whole squares and within-square measurements.
  - Measurements include a range from binary (yes/no) to continuous (areas, lengths), collected for selected features via quadrats.
  - Squares are not a random subset; sampling is stratified within designated strata using the ITE Land Classification.
  - Land Classification history and country-specific classifications:
    - Original 32 classes.
    - 1998 update to 42 classes for Scotland-specific reporting.
    - 2007 update to 45 classes for Wales-specific reporting.
    - Each country now has a separate classification (England: 21, Wales: 8, Scotland: 16).
  - Representativeness and variation:
    - Estimates derived from CS data must account for stratification; ignoring it can yield unrepresentative estimates and inaccurate variation.
  - Exclusions and representativeness:
    - Squares with area more than 90% sea or more than 75% urban (per 1:250000 OS maps) were excluded from field survey.
    - Official GB estimates assume excluded squares have similar vegetative land composition to sampled squares; this may introduce bias only in regions with high sea/urban proportions (likely negligible overall due to small affected area).
  - Estimation approach:
    - Uses ratio estimates (Cochran, 1963) by land class, weighted by the vegetative land area within each class.
  - Uncertainty estimation:
    - From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.