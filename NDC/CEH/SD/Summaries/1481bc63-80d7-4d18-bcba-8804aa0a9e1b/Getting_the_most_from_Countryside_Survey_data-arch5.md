# Notes on the downloadable data

- Confidentiality and data privacy
  - The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH.
  - External users will not be able to identify square locations with precision finer than 100 square kilometers.
  - This constraint is in place to preserve representativeness and limit disclosure risk.

- CS sampling design and levels
  - Field survey data come from a sample of 1 km squares across GB.
  - Two levels of measurement: characteristics of whole squares and features within each square (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include a mix of binary and continuous variables (e.g., areas, lengths).

- Sampling framework and representativeness
  - Squares are not a random subset of all GB squares; the design is stratified within designated strata.
  - Stratification is based on the ITE Land Classification, which has evolved over time:
    - Original 32 classes
    - 1998 update for Scotland (42 classes)
    - 2007 update for Wales (45 classes)
  - Each country now uses its own classification, with England (21 classes), Wales (8), Scotland (16).
  - Because of stratification, estimates that ignore this design may be biased or non-representative.

- Exclusions and extrapolation
  - Squares with >90% sea area or >75% urban area (by 1:250,000 OS map) were excluded from field surveys.
  - Official estimates pertain to the included squares; extrapolation to all GB assumes similar vegetation composition in excluded squares.
  - This assumption is generally reasonable given the small total area of excluded squares, but regional biases can occur if a region has a high share of sea/urban squares.

- Estimation and uncertainty
  - Estimates by land class are produced using ratio estimation, weighting by vegetative land area within each land class.
  - Since 1998, bootstrap methods (Efron and Tibshirani) are used to estimate standard errors and confidence intervals due to skewness in certain features.

- Data stewardship implications (for governance, sharing, and use)
  - Metadata should clearly document:
    - Stratification structure, land classes, and any country-specific classifications
    - Exclusion criteria and the resulting representativeness limits
    - The weighting scheme (vegetative land area) and the use of ratio estimates
    - The bootstrap approach used for uncertainty estimates
    - Privacy constraints limiting precise square locations
  - Data users should account for stratification and potential extrapolation biases in analyses.
  - Ensure updates align with country-specific classifications and sampling design changes.
  - Consider maintaining provenance and versioning of datasets, including documentation of any derived products and the methods used to generate them.

- References
  - Barr, C.J., et al. Countryside Survey 1990 Main Report (1993)
  - Cochran, W.G. Sampling Techniques (2nd ed.) (1963)
  - Efron, B., Tibshirani, R.J. An introduction to the bootstrap (1993)