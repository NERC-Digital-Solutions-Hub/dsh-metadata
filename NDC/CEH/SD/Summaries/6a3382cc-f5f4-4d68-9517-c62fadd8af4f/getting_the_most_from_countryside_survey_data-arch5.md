# Notes on the downloadable data

- Purpose and confidentiality
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users cannot identify survey squares with precision finer than 100 square kilometres.

- Sampling design of Countryside Survey (CS)
  - Field data come from a sample of 1-km squares across Great Britain (GB).
  - Within each selected square, measurements are taken at two levels: the square level and within-square features.
  - Data are not a random subset; the sample is stratified by ITE Land Classification (land classes) with sub-sampling within strata.
  - Land Classification evolution: 32 → 42 → 45 classes over time, with separate classifications for England, Wales, and Scotland.
  - Estimates that ignore stratification may be non-representative and have biased variation estimates.

- Exclusions and representativeness
  - Squares with area >90% sea or >75% urban were excluded from field surveys.
  - Field data are strictly representative of the included squares; extrapolations to the whole GB assume excluded vegetative land resembles included squares.
  - Bias risk is generally small unless a region has a high proportion of sea or urban squares.

- Estimation and uncertainty
  - Estimates are produced as ratio estimates within land classes, weighted by the vegetative land area of each class.
  - From 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.
  - Country-specific classifications require careful handling when aggregating across UK regions.

- Data provenance and references
  - Key references: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) The Bootstrap.

- For Data Stewards: governance and metadata implications
  - Maintain metadata on stratification (land class definitions, country-specific classifications) and sampling within-square vs. square-level measurements.
  - Document confidentiality constraints and the 100 sq km precision limit for square locations.
  - Include guidance on appropriate analysis that accounts for stratification and weighting, and on using bootstrap SEs/CIs.
  - Note limitations due to exclusions (sea/urban) and potential regional biases when disseminating national or regional estimates.