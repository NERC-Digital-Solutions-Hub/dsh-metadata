# Notes on the downloadable data

- Confidentiality and precision
  - The exact locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users cannot identify survey squares with precision finer than 100 square kilometres.
  - Consequently, it is not possible to determine whether defined areas contain any survey squares at a finer scale than 100 sq km.

- Data structure and content
  - Countryside Survey (CS) field data come from a sample of 1-km squares across Great Britain (GB).
  - Each selected square is mapped and measured at two levels: the square level and within-square features.
  - Measurements span binary and continuous variables (e.g., vegetation, soils, quadrat data).

- Sampling design and representativeness
  - The CS sample is not a random subset of all GB 1-km squares; it is stratified by Land Classification (ITE).
  - The Land Classification has evolved by country (England, Wales, Scotland) with varying class counts (e.g., 21 in England, 8 in Wales, 16 in Scotland).
  - Estimates that do not account for stratification may be non-representative and have biased variation estimates.
  - Not all GB squares were surveyed; squares with more than 90% sea or more than 75% urban area were excluded from field survey.
  - Excluded squares are assumed similar in vegetative land composition to sampled squares for GB-scale estimates, though this assumption may introduce bias in regions with high sea/urban square coverage.

- Estimation methods and uncertainty
  - Official GB and regional estimates are produced using ratio estimates that weight by vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to concerns about feature skewness.
  - Weights are applied when combining land-class estimates to produce GB-wide results.

- Implications for GIS work
  - When analyzing CS data, incorporate stratification by land class and area weights to obtain unbiased estimates.
  - Be cautious when extrapolating from sampled squares to larger areas; the masking of precise locations (100 sq km resolution) limits fine-scale hotspot analysis.
  - Use bootstrap-derived standard errors and confidence intervals to assess uncertainty in mapped estimates.

- References
  - Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.