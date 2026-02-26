# Notes on the downloadable data

- Location confidentiality: precise locations of Countryside Survey (CS) squares are withheld by UKCEH; external users cannot identify whether squares fall within defined areas with precision finer than 100 square km.

- Data structure and sampling levels: CS field data come from a sample of 1-km squares across Great Britain; each square is mapped and measured at two levels—whole square characteristics and within-square features (e.g., quadrats for vegetation, soils).

- Non-random, stratified sampling: CS squares are not a random subset; sampling is stratified by the ITE Land Classification. Country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16). Analyses that ignore stratification may be unrepresentative and underestimate variation.

- Exclusions and representativeness: squares with more than 90% sea area or more than 75% urban area were excluded from field surveys. Estimates for GB or regions assume excluded vegetative land resembles sampled squares; this bias is generally small but can be problematic in regions with high sea/urban coverage.

- Weighting and estimation: official estimates are produced as ratio estimates for each land class, weighted by the vegetative land area within each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness.

- Practical implications for GIS work: when mapping CS data, account for the stratified design, weighting by vegetative land area, and the confidentiality constraint (no precise square-level positions). Use region- or land-class-specific estimates and consider bootstrap-derived uncertainty in visualizations and analyses.

- References: 
  - Barr, C.J., et al. Countryside Survey 1990 Main Report (1993)
  - Cochran, W.G. Sampling Techniques (2nd ed., 1963)
  - Efron, B. & Tibshirani, R.J. An Introduction to the Bootstrap (1993)