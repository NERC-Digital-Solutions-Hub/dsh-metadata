# Notes on the downloadable data

- Data confidentiality and precision
  - The precise locations of CS survey squares are kept confidential by UKCEH to preserve representativeness.
  - External users cannot identify square locations to a precision better than 100 square km.
  - Consequently, users cannot determine whether any survey squares fall within defined areas below this threshold.

- Sampling design and levels
  - CS Field Survey data come from a sample of 1 km squares in GB.
  - Each selected square is mapped and measured at two levels: the whole square and within-square features.
  - Measurements include a mix of binary and continuous variables (e.g., areas, lengths).

- Representativeness and stratification
  - The sample is not a random subset of all GB squares; it is stratified by land classification.
  - Land classifications differ by country: England (21 classes), Wales (8), Scotland (16).
  - Analyses that do not account for stratification may yield biased estimates of variation; estimates are produced using stratified-weighted approaches based on vegetative land area within each class.

- Exclusions and implications
  - Squares excluded from field survey: areas where OS-mapped area is >90% sea or >75% urban.
  - Official GB estimates assume excluded squares have similar vegetative composition to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

- Estimation and uncertainty
  - Land class estimates are derived using ratio-estimation techniques, weighted by the vegetative land area in each class.
  - Since 1998, standard errors and confidence intervals are estimated with bootstrap methods due to potential skewness in some features.

- References
  - Barr, C.J. et al. 1993. Countryside Survey 1990 Main Report.
  - Cochran, W.G. 1963. Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. 1993. An Introduction to the Bootstrap.

- Data stewardship implications for Data Stewards
  - Document and communicate the confidentiality constraints and the 100 square km precision threshold.
  - Provide metadata on sampling design (two levels, stratification by country-specific land classifications) and exclusion criteria.
  - Include guidance on how to account for stratification and weighting in analyses to avoid biased inferences.
  - Clearly describe the estimation methods (ratio estimates, bootstrap uncertainty) and their implications for reported results.
  - Maintain traceability of land-class definitions and how they have evolved across England/Wales/Scotland.