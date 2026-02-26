# Notes on the downloadable data

- Purpose and confidentiality
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users will not be provided with square locations more precise than 100 square km.

- What Countryside Survey field data include
  - Data come from a sample of 1-km squares in GB.
  - For each square, both square-level and within-square measurements are collected (e.g., vegetation, soils) using quadrats.
  - Measurements are varied in type, from binary to continuous.

- Sampling design and implications
  - CS squares are not a random subset; sampling is stratified within designated strata.
  - Stratification is defined by the ITE Land Classification, which has evolved over time (32 → 42 → 45 classes; separate country classifications: England 21, Wales 8, Scotland 16).
  - Estimates not accounting for stratification may be unrepresentative and have inaccurate variation.

- Exclusions and representativeness
  - Squares with more than 90% sea or more than 75% urban area were excluded from field surveys.
  - Official estimates are for the squares that meet criteria; GB estimates assume excluded vegetative land is similar to sampled squares, which is generally reasonable but could be problematic in highly sea- or urban-dominated regions.

- Estimation and uncertainty
  - Land-class estimates are produced as ratio estimates, weighted by the area of vegetative land within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness (Efron and Tibshirani).

- Practical considerations for data use
  - When analysing CS data, account for stratification and area-based weighting.
  - Be aware that the sampling design affects representativeness and uncertainty; use bootstrap-based CIs where applicable.
  - The confidentiality constraint limits precise location-based analyses beyond 100 square km.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.