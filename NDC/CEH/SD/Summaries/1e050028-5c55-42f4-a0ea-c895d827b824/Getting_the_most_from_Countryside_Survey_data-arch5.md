# Notes on the downloadable data

- Confidentiality of locations: Precise locations of Countryside Survey (CS) field squares are held confidential by CEH; external users cannot identify whether squares fall within defined areas with precision better than 100 square km to preserve representativeness.

- Sampling framework: CS field survey data come from a sample of 1 km squares in Great Britain, with measurements taken at two levels—per square and within-square—covering binary and continuous variables (e.g., vegetation, soils, etc.).

- Non-random, stratified design: The sample is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16). Estimates not accounting for stratification may be non-representative and have incorrect variation.

- Excluded squares: Squares where area is >90% sea or >75% urban (per 1:250,000 OS maps) are not surveyed. Official GB estimates apply only to the included squares; extrapolation to GB assumes excluded vegetative land is similar to sampled areas, which is generally a small bias unless a region has substantial sea/urban coverage.

- Estimation and weighting: Official estimates are derived by ratio estimation for each land class, weighting by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness.

- Implications for data users and governance: Metadata should document the stratified sampling design, exclusion criteria, and weighting approach; analyses should account for stratification and sampling design to avoid biased inferences; bootstrap-based uncertainty estimates should be preserved for reproducibility.

- References and methodological basis:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap

- Practical note for data stewardship: Clearly communicate the confidentiality constraint, the two-level sampling design, country-specific land classifications, exclusion criteria, and the bootstrap approach to uncertainty to users; ensure data release metadata reflects these aspects to support valid analyses and responsible data sharing.