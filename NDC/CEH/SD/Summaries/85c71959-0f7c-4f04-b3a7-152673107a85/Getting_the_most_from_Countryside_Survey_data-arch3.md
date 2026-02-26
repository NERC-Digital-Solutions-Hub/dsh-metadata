# Notes on the downloadable data

- Purpose and confidentiality
  - To preserve representativeness of the wider countryside, the precise locations of Countryside Survey (CS) squares are kept confidential by CEH.
  - External users will not be able to identify survey squares with precision finer than 100 square km.

- Sampling framework and data scope
  - CS field survey data come from a sample of 1 km squares across GB, with measurements taken at two levels: per square and within-square (e.g., quadrats, vegetation, soils).
  - Measurements span binary and continuous variables, creating a mix of data types.

- Sampling design characteristics
  - The sampling is stratified rather than random, using the ITE Land Classification.
  - Country-specific classifications have evolved:
    - England: 21 land classes
    - Wales: 8 land classes
    - Scotland: 16 land classes
  - Historically, the classification changed from 32 classes (original) to 42 (1998) and 45 (2007) due to separate country reporting needs.

- Representativeness and exclusions
  - Not all GB squares were considered for field survey.
  - Exclusion criteria: squares with more than 90% sea area or more than 75% urban area.
  - Official estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

- Estimation and inference
  - Estimates are produced as ratio estimates by land class, weighting by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness of some features.

- Data access, metadata, and governance
  - Metadata quality and availability can be a practical barrier to reuse.
  - To use and verify data, users often need to engage with data originators to fill gaps or enhance metadata.
  - Public sharing of underlying data is a consideration in data governance and can impact data usage.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.