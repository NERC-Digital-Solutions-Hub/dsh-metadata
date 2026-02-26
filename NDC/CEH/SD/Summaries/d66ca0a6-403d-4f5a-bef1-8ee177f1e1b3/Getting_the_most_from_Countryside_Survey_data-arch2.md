# Notes on the downloadable data

- Overview
  - Documents the handling, limitations, and statistical considerations for Countryside Survey (CS) Field Survey data used to monitor GB countryside conditions.
  - Aims to preserve representativeness while restricting precise location information.

- Confidentiality and Access
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users will not receive location precision better than 100 square kilometres; cannot determine whether squares fall within defined areas below this threshold.

- Sampling Design
  - Data come from a sample of 1 km squares in GB, with measurements at two levels: whole square and within-square features.
  - Measurements include a mix of binary and continuous variables.
  - The sample is not random; it is stratified by Land Classification (ITE).
  - Land Classification changes over time:
    - Original: 32 classes
    - 1998: Scotland-specific reporting led to 42 classes
    - 2007: Wales-specific reporting led to 45 classes
    - England: 21 classes; Wales: 8 classes; Scotland: 16 classes
  - Excluded squares: those >90% sea or >75% urban were omitted from field surveys.
    - Official estimates assume vegetative land in excluded squares is similar to sampled squares; biases are expected to be small except in regions with high sea/urban proportions.

- Estimation and Uncertainty
  - Estimates by land class are calculated as ratio estimates, weighted by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are derived using bootstrap methods due to skewness in some features (Efron and Tibshirani, 1993).

- Implications for Analysis and Monitoring
  - Analyses must account for stratified sampling and weights to obtain representative estimates.
  - Extrapolation to excluded squares can introduce bias, particularly in regions with substantial sea or urban areas.
  - Location confidentiality limits fine-grained mapping; analyses should rely on standardized outputs and aggregated data where necessary.
  - To maximize data value, combine CS data with other relevant datasets, and ensure underlying data accessibility and standardised presentation (reports, maps, charts).
  - Ensure data quality: verification, cleaning, transformation, and storage in appropriate data portals, aligning with standardised methodologies for environmental health assessment.

- References
  - Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.