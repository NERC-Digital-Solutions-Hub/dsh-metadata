# Notes on the downloadable data

- Overview
  - The precise locations of Countryside Survey (CS) field survey squares are held confidential by CEH to preserve representativeness. External users cannot identify square locations to a precision better than 100 square km.

- Sampling design
  - CS field survey data come from a sample of 1 km squares across GB, with measurements taken at two levels: within-square and square-level, using varied data types (binary to continuous).
  - The sample is stratified, not random, with strata defined by the ITE Land Classification. Country-specific classifications are used: England (21 classes), Wales (8), Scotland (16); classifications have been revised over time (32 → 42 → 45 classes) to accommodate separate country reporting.
  - Not all GB squares are surveyed: squares more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) are excluded. Estimates for GB assume excluded squares are similar in vegetative land composition to sampled squares; this may introduce bias only in areas with high sea/urban coverage.

- Estimation and uncertainty
  - Official GB estimates are produced using ratio estimates for each land class, weighting by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals have been estimated via bootstrap methods (Efron & Tibshirani) due to skewness of some features.

- Implications for monitoring and analysis
  - The sampling design and exclusions affect representativeness and must be accounted for in analyses (e.g., through stratification weights and awareness of potential biases when regions contain more sea/urban area).

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.