# Notes on the downloadable data

- Confidentiality and location precision
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users cannot identify whether squares fall within defined areas below a 100 square km threshold.

- Data structure and sampling levels
  - Countryside Survey (CS) field data come from a sample of 1 km squares in GB.
  - Two sampling levels: whole square (characterising the square) and within-square (features inside the square).
  - Measurements include binary (yes/no) and continuous variables (areas, lengths, etc.).

- Sampling design and stratification
  - The sample is not a random subset of all GB squares; it is stratified.
  - Stratification is by Land Classification (ITE) with country-specific classifications:
    - Separate classifications for England, Wales, and Scotland (e.g., 21 classes in England, 8 in Wales, 16 in Scotland).
  - Land class definitions have evolved over time (32 → 42 → 45 classes) to support separate country reporting.

- Exclusions and representativeness
  - Squares with more than 90% sea or more than 75% urban area (per 1:250,000 OS maps) were excluded from field survey.
  - Official estimates assume that vegetative land in excluded squares is similar to sampled squares; bias is typically small unless a region has a high proportion of sea/urban squares.

- Estimation methods
  - Estimates are produced using ratio estimates for each land class, weighted by the vegetative land area of each class.
  - Weights are applied to combine land-class estimates into overall estimates.

- Uncertainty and standard errors
  - Standard errors and confidence intervals have been estimated using bootstrap methods since 1998, due to skewness in some features.

- Practical implications for analyses
  - Analyses must account for stratification and weighting by vegetative land area to avoid biased estimates.
  - When combining across countries, use country-specific land classifications.
  - Region-wide estimates can be biased if the region includes a high proportion of excluded or non-represented squares; handle with caution.

- Data usage notes
  - Outputs can be produced at various aggregation levels; consider using aggregated, self-contained outputs to preserve confidentiality and reflect the sampling design.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.