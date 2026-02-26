# Notes on the downloadable data

- Purpose and scope: Countryside Survey (CS) field data consist of measurements from a sample of 1 km squares in Great Britain, with both whole-square and within-square measurements (various data types from binary to continuous).

- Data confidentiality: exact locations of CS survey squares are kept confidential by CEH; external users cannot identify squares with precision finer than 100 square km, limiting geographic pinpointing.

- Sampling design and representativeness:
  - Sampling is not random; it is stratified by ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16).
  - The design includes two levels of measurement and relies on ratio estimates weighted by vegetative land area in each land class.
  - Some squares were excluded from field survey (area > 90% sea or > 75% urban). Estimates for GB or regions assume excluded areas are similar in vegetative composition to sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.

- Estimation and uncertainty:
  - Official estimates are produced using ratio estimates (Cochran, 1963) with area-based weights.
  - Since 1998, standard errors and confidence intervals are estimated with bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.

- Data quality, metadata, and governance:
  - Ensuring data quality involves careful metadata handling, data cleaning, transformation, and transparent presentation of findings (reports, charts, dashboards).
  - Access to underlying data and metadata can be a barrier; data providers may need to be contacted to verify metadata or obtain datasets.
  - Data sharing and governance considerations are important, given the confidentiality and transformation requirements.

- Implications for analysis and use:
  - Analyses must account for stratified sampling and weighting by vegetative land area.
  - Be cautious about extrapolating to excluded areas (sea/urban-dominated squares) and to GB as a whole without considering the underlying stratification and exclusions.
  - Use bootstrap-derived uncertainty estimates to reflect potential skewness in land-class features. 

- References:
  - Barr et al. 1993; Cochran 1963; Efron & Tibshirani 1993.