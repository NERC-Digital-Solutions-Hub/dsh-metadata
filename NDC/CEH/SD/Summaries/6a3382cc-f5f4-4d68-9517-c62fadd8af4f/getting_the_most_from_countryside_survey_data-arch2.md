# Notes on the downloadable data

- Confidentiality of locations: UKCEH holds precise Countryside Survey (CS) square locations; external users cannot identify square locations with greater precision than 100 square km.
- Sampling design and data structure:
  - CS field survey data come from a sample of 1-km squares across GB.
  - For each selected square, both whole-square measurements and within-square measurements are taken (e.g., quadrats for vegetation, soils, etc.).
  - Measurements vary in type, from binary to continuous (areas, lengths).
  - The sample is not random; it is stratified by the ITE Land Classification, with country-specific refinements (England: 21 classes, Wales: 8, Scotland: 16; overall evolution from 32 to 45 classes over time).
- Representativeness and exclusions:
  - Analyses must account for stratification; estimates not adjusted for stratification may be unrepresentative and have incorrect variation estimates.
  - Not all 1-km squares were surveyed; squares with >90% sea or >75% urban area were excluded from field survey.
  - Official GB estimates apply only to the surveyed squares; to estimate GB-wide patterns, it is assumed excluded squares have vegetative land similar to sampled squares (bias is generally small unless a region has unusually high sea/urban cover).
- Estimation method and uncertainty:
  - GB land-class estimates are produced using ratio estimates that weight by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron and Tibshirani, 1993) due to skewness in some features.
- References:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron and Tibshirani (1993). An Introduction to the Bootstrap.