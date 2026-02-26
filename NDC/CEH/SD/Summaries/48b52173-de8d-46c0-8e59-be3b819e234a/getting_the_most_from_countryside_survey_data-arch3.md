# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) survey squares are kept confidential by UKCEH to preserve representativeness of the wider countryside; external users cannot identify square locations to better than 100 square km, limiting whether a square falls within defined areas.

- CS Field Survey design:
  - Data are collected from a sample of 1 km squares across Great Britain.
  - Each selected square is mapped and contains within-square measurements (e.g., quadrats for vegetation, soils, etc.), in addition to whole-square characterisations.
  - Measurements include a mix of binary and continuous variables.

- Sampling structure and representativeness:
  - The CS sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification.
  - Land Classification has evolved: originally 32 classes, expanded to 42 in 1998 for Scotland-focused reporting, and to 45 later with Wales-focused reporting (England: 21 classes, Wales: 8, Scotland: 16).
  - Estimates that ignore stratification may be unrepresentative and misstate variation.

- Exclusions and their implications:
  - Squares with more than 90% sea area or more than 75% urban area were excluded from field survey.
  - Official GB/region estimates assume excluded squares have vegetative land composition similar to sampled squares; this assumption may introduce bias mainly where a region has a high proportion of sea or urban squares.

- Estimation and uncertainty:
  - Official land-class estimates are produced using ratio estimates, weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods to address potential skewness.

- Data quality, metadata, and governance:
  - The sampling design and weighting require careful handling of metadata to ensure appropriate use and comparability.
  - Sharing underlying data and ensuring transparency of metadata are important considerations, with confidentiality constraints noted.

- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.

- Implications for monitoring frameworks:
  - Clear documentation of sampling design, stratification, and exclusion criteria is essential for understanding representativeness and uncertainty.
  - Use of area-weighted ratio estimates and bootstrap-derived uncertainty supports transparent reporting of environmental health indicators.
  - Confidentiality constraints should be balanced with data sharing and metadata practices to enable robust policy evaluation and decision-making.