# Notes on the downloadable data

- Purpose and scope
  - Describes Countryside Survey (CS) field data from GB and its sampling design, to support environmental monitoring, analysis, and policy evaluation.
  - Data are structured to enable estimates of vegetative land across GB, with a focus on representativeness and methodological rigor.

- Data confidentiality and accessibility
  - Precise locations of CS survey squares are confidential to preserve representativeness.
  - External users cannot identify survey squares with precision finer than 100 square km.

- Sampling design and levels
  - CS data come from a sample of 1 km squares across GB.
  - Two levels of sampling: the square itself and measurements within each square (e.g., quadrats for vegetation, soils, etc.).
  - Not a simple random subset; the sample is stratified by the ITE Land Classification.
  - Country-specific classifications have evolved:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Classifications have expanded over time (32 → 42 → 45 classes) to accommodate separate country reporting.

- Representativeness and exclusions
  - Estimates must account for stratification; ignoring it can yield biased estimates.
  - Some GB squares were excluded from field survey:
    - >90% sea
    - >75% urban
  - Official GB estimates assume excluded land is similar in vegetative composition to included squares; bias is expected to be small unless a region has a high share of sea or urban squares.

- Estimation methods
  - Land-class estimates are computed using ratio estimates, weighted by the area of vegetative land in each class.
  - Since some features are skewed, standard errors and confidence intervals (since 1998) are estimated using bootstrap methods.

- Data characteristics and usage
  - Measurements encompass a range of data types (binary, continuous) across two sampling levels.
  - Requires careful handling of stratification, weighting, and, where applicable, bootstrap SEs to draw valid inferences about vegetative land and related features.

- References and methodological notes
  - Barr, Bunce, Clarke et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.