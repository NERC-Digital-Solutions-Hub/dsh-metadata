# Notes on the downloadable data

- Purpose of data confidentiality
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey squares are kept confidential by UKCEH and external users cannot identify squares to a precision finer than 100 square kilometers.

- Countryside Survey (CS) sampling design
  - Field data come from a sample of 1-km squares in Great Britain (GB).
  - Each selected square is mapped and detailed measurements are taken both at the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Measurements vary from binary to continuous variables, and there are two levels of sampling: whole square and within-square details.
  - The square sample is not a random subset of all 1-km GB squares; it is stratified within designated strata defined by the ITE Land Classification.
  - Land Classification evolution by country:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - The classification has changed over time (32 → 42 → 45 classes) due to country-specific reporting needs.

- Implications for analysis and representativeness
  - Estimates derived from CS data without accounting for stratification may be unrepresentative and have biased variation estimates.
  - The sampling design excludes certain squares a priori based on area composition.

- Exclusions and their impact on representativeness
  - Squares with more than 90% sea area or more than 75% urban area were excluded from the field survey.
  - Official GB estimates assume that vegetative land in excluded squares resembles that in sampled squares; biases are expected to be small unless a region has a high proportion of sea/urban squares.

- Data processing and estimation methods
  - Estimates are produced by ratio estimation within land classes, using the area of vegetative land in each sample square as the weighting factor.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness (Efron and Tibshirani).

- Key references
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.

- Notes on data context and governance
  - Location privacy and stratified sampling design are essential considerations for using CS data.
  - Data interpretation should account for non-random sampling, country-specific land classifications, and the bootstrap-based uncertainty estimates. 
  - The documentation references underlying mapping scales (e.g., 1:250,000 OS maps) used in area calculations for squares.