# Notes on the downloadable data

- Data confidentiality and access
  - To preserve representativeness, precise locations of CS survey squares are kept confidential by UKCEH.
  - External users will not be provided with location precision finer than 100 square kilometres.
  - Consequently, users cannot determine whether survey squares fall within defined areas below this threshold.

- Sampling design and data levels
  - Countryside Survey field data come from a sample of 1 km squares across Great Britain.
  - Two levels of sampling and measurement:
    - Whole square level (square is mapped and characterized)
    - Within-square level (detailed measurements for features inside the square, e.g., quadrats for vegetation, soils)
  - Measurements are varied (binary to continuous).
  - The sample is not a random subset; it is stratified by designated strata.
  - Strata are defined by the ITE Land Classification, with country-specific adaptations:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - The land classification has evolved over time (32 classes originally; 1998 modification for Scotland; 2007 modification for Wales), resulting in country-specific classifications.

- Exclusions and representativeness
  - Squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field survey.
  - Official GB estimates assume vegetative land in excluded squares is similar to that in sampled squares, an assumption that generally biases little unless a region has a high proportion of sea/urban squares.

- Estimation methods and statistical treatment
  - Estimates are produced as ratio estimates for each land class, weighted by the vegetative land area within each class.
  - Because of stratification, estimates must account for the area weights of land classes to be representative.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.

- Data governance, provenance, and usage notes for stewards
  - Metadata should document the sampling design, stratification scheme, exclusions, and weighting procedures.
  - Track and communicate changes in land classification across years to maintain comparability.
  - When sharing or reusing data, clearly state limitations arising from the non-random sampling design and potential biases due to excluded squares.
  - Include methodological references to enable reproducibility (Cochran 1963; Efron & Tibshirani 1993; Barr et al. 1993).

- References
  - Barr, C.J. et al. Countryside Survey 1990 Main Report (1993)
  - Cochran, W.G. Sampling techniques (2nd ed.) (1963)
  - Efron, B. & Tibshirani, R.J. An introduction to the bootstrap (1993)