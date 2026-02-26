# Notes on the downloadable data

- Context and data scope
  - Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at both whole-square and within-square levels.
  - Measurements vary from binary to continuous variables and include vegetation, soils, and related features.

- Confidentiality and geolocation
  - Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
  - External users do not have precision better than 100 square kilometers, making it impossible to determine whether specific survey squares fall within defined areas below this threshold.

- Sampling design and representativeness
  - The CS sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification with country-specific adaptations (England: 21 classes, Wales: 8, Scotland: 16).
  - Exclusions: squares with area >90% sea or >75% urban (as measured on 1:250,000 OS maps) are not surveyed.
  - Estimates for GB or regional levels assume similarity between surveyed and excluded areas; bias is expected to be small unless a region has a high proportion of sea/urban squares.
  - Official estimates use ratio estimation by land class, weighted by vegetative land area per land class.
  - Since 1998, standard errors and confidence intervals are derived via bootstrap methods to address skewness.

- Implications for analysis and monitoring frameworks
  - Analyses must account for stratification and weighting to avoid misleading estimates of level and variation.
  - When regions are of interest, be mindful of the assumption that unsampled/excluded squares are representative of surveyed areas.
  - The mixed measurement levels (binary and continuous) require appropriate statistical treatment and clear communication of uncertainty (bootstrap SEs).

- Data handling and dissemination considerations
  - The sampling design and confidentiality constraints may affect reproducibility and fine-grained spatial analyses.
  - Transparency about data provenance, weighting, and estimation methods is important for monitoring outputs and governance.

- References
  - Barr, C.J., et al. 1993. Countryside Survey 1990 Main Report.
  - Cochran, W.G. 1963. Sampling Techniques (2nd ed.).
  - Efron, B. and Tibshirani, R.J. 1993. An Introduction to the Bootstrap.