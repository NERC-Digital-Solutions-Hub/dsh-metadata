# Notes on the downloadable data

- Confidentiality and location privacy
  - Precise locations of Countryside Survey (CS) field survey squares are kept in confidence by CEH.
  - External users cannot identify squares with precision better than 100 square km.
  - As a result, users cannot determine whether specific survey squares fall within defined areas below this threshold.

- Data structure and sampling levels
  - CS field survey data come from a sample of 1 km squares in Great Britain.
  - Two sampling levels: whole squares (square-level) and within-square measurements.
  - Measurements are of mixed types (binary to continuous), with some characteristics described at the square level and others within squares.

- Sampling design and stratification
  - Squares are not a random subset; the design is stratified by land classification.
  - Land classification (country-specific) has evolved:
    - Originally 32 classes; expanded to 42 in 1998 for Scotland reporting.
    - Further revision to 45 classes in 2007 for Wales reporting.
  - England: 21 classes; Wales: 8; Scotland: 16.
  - Estimates that ignore stratification may be unrepresentative and have incorrect variation estimates.

- Representativeness and extrapolation
  - Not all GB squares were surveyed; exclusions were based on map-derived area criteria:
    - Excluded if ≥90% sea or ≥75% urban.
  - Official GB estimates assume vegetative land in excluded squares is similar to sampled ones; bias is expected to be small unless a region is dominated by sea or urban squares.

- Analysis method and uncertainty
  - Estimation uses ratio estimates by land class, weighted by the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani).

- Implications for data governance and reuse
  - Users must account for stratification and non-random sampling when analyzing CS data.
  - Documentation should reflect the sampling design, classifications, exclusions, and bootstrap-based uncertainty.
  - Metadata should include details on confidentiality protections, area-based precision limits, and the country-specific land-class framework.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.