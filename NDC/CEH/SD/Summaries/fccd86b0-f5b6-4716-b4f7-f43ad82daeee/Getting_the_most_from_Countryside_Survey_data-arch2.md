# Notes on the downloadable data

- Purpose and scope
  - Describes how Countryside Survey (CS) data are collected, processed, and presented for monitoring environmental health.
  - Highlights data representativeness, sampling design, and estimation methods to support informed analysis and policy scrutiny.

- Location privacy and precision
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users cannot identify squares to better than 100 square km, limiting spatial pinpointing within defined areas.

- Sampling design (two levels)
  - Field data come from a sample of 1 km squares across GB.
  - Two levels of measurement: across each square (characterising the square) and within-square (detailed within-square features via quadrats).
  - Measurements include binary and continuous variables.
  - Not a random sample; it is stratified by ITE Land Classification, with country-specific refinements:
    - England: 21 land classes
    - Wales: 8 land classes
    - Scotland: 16 land classes
  - The classification system has evolved (32 → 42 → 45 classes due to Scotland/Wales reporting requirements).

- Representativeness and limitations
  - Estimates ignoring stratification may be non-representative and misstate variation.
  - Not all GB squares were surveyed; squares that are >90% sea or >75% urban were excluded.
  - Official GB/region estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is considered negligible unless a region has high sea/urban coverage.

- Estimation methods
  - Estimates by land class are ratio estimates that account for the vegetative land area within each sample square.
  - Land-class estimates are combined using weights equal to the vegetative land area of each land class overall.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.

- Data quality and outputs
  - Data are collected, mapped, and subjected to quality assurance and cleaning.
  - Outputs are presented in clear formats (reports, maps, charts) and datasets are stored/uploaded to appropriate portals.

- Practical considerations for analysts
  - Always account for stratification by land class and country-specific classifications when analyzing CS data.
  - Use the provided weights (vegetative land area) and ratio-estimation framework for land-class estimates.
  - Interpret standard errors/confidence intervals derived from bootstrap methods; be mindful of potential biases from excluded squares and non-random sampling design.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.