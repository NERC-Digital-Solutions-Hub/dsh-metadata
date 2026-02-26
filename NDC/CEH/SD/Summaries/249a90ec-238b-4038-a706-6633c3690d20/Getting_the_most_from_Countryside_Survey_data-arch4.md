# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) squares are confidential to preserve representativeness; external users cannot identify survey squares with precision finer than 100 square km. This limits fine-grained geospatial analyses.

- CS Field Survey data come from a sample of 1 km squares across Great Britain. Each selected square is mapped and measured at two levels: the square as a whole and features within the square. Measurements range from binary to continuous variables.

- The sampling is not a random subset of all GB squares. It is a stratified sample based on the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16). There are two levels of sampling (whole square and within-square) and measurements are taken at both levels.

- Squares were not all surveyed: squares with more than 90% sea or more than 75% urban area were excluded. The field data thus represent only the eligible squares; extrapolation to GB or regions assumes similar vegetative land composition in excluded squares. This assumption generally yields small biases unless a region has a high proportion of sea/urban squares.

- Estimates from CS data are calculated as ratio estimates by land class, weighted by the vegetative land area of each class. Since stratification is important, analyses that ignore stratification may be biased or have incorrect variance estimates.

- Uncertainty measures have used bootstrap methods since 1998 to address skewness in some features (references: Efron & Tibshirani, 1993).

- References for methodology and data context include Barr et al. (1993) for the 1990 Main Report, Cochran (1963) on sampling techniques, and Efron & Tibshirani (1993) on bootstrap methods.

- Practical implications for data users and data leaders: manage expectations about geographic precision and sampling design; ensure metadata clearly documents stratification, country-specific land classifications, exclusions, and the estimation approach; provide aggregated outputs that respect confidentiality; communicate limitations when interpreting regional or GB-wide estimates.