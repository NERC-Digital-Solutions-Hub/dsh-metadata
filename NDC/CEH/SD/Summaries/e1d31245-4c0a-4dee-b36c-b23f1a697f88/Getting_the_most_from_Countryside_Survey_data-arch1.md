# Notes on the downloadable data

- Confidentiality and geographic precision
  - Precise CS survey square locations are kept confidential by CEH.
  - External users cannot identify whether squares fall within defined areas to better precision than 100 square km.

- Data structure and levels of sampling
  - Countryside Survey (CS) field data come from a sample of 1 km squares across GB.
  - Each square is mapped; measurements are taken at two levels: the square as a whole and features within the square (e.g., quadrats for vegetation, soils).
  - Measurements include a range of variable types from binary to continuous.

- Sampling design and representativeness
  - The sample is not a random subset of all GB squares; it is stratified by designated strata.
  - Strata are defined by the ITE Land Classification, which has evolved:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - The land classification has changed over time (32 → 42 → 45 classes) to accommodate country reporting needs.
  - Estimates must account for stratification; analyses that ignore stratification may be unrepresentative or misstate variation.

- Exclusions and implications for coverage
  - Squares with more than 90% sea or more than 75% urban area (per 1:250,000 OS maps) were excluded from field surveys.
  - Official GB estimates are based on the surveyed squares; extrapolations assume excluded squares have similar vegetative land composition as sampled squares.
  - This assumption may introduce bias only if a region has a high proportion of sea or urban squares.

- Estimation method and uncertainty
  - Estimation by land class uses ratio estimates (Cochran, 1963) with weights based on the vegetative land area of each land class.
  - From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness concerns.

- References
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Cochran (1963): Sampling Techniques
  - Efron and Tibshirani (1993): An Introduction to the Bootstrap