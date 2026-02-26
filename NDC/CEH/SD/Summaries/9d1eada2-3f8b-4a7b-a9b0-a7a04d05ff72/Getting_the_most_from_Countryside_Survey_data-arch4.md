# Notes on the downloadable data

- Purpose and confidentiality
  - The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify square locations with precision finer than 100 square km.

- Data scope and structure
  - CS field survey data come from a sample of 1 km squares in Great Britain.
  - Within each selected square, maps are created and detailed measurements are taken (e.g., quadrats for vegetation, soils, etc.).
  - There are two sampling levels: the square level (characterising the square) and within-square measurements (characterising features inside the square).
  - Measurements include a mix of binary and continuous variables (e.g., areas, lengths).

- Sampling design and representativeness
  - The CS squares are not a random subset; the sample is stratified by the ITE Land Classification.
  - Land Classification has evolved:
    - Original: 32 classes
    - 1998: expanded to 42 classes (Scotland reporting requires changes)
    - 2007: expanded to 45 classes (Wales reporting requires changes)
    - Each country has a separate set of classes (England: 21, Wales: 8, Scotland: 16).
  - Not all GB squares were surveyed; squares with >90% sea or >75% urban area (by 1:250,000 OS maps) were excluded.
  - Estimates for GB or regions rely on assumptions that vegetative land in excluded squares resembles that in sampled squares; bias is considered negligible unless a region has a high proportion of sea/urban squares.

- Analytical method and uncertainty
  - Official estimates are produced using ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area in each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness concerns.

- Implications for users and data management
  - Analyses must account for the stratified sampling design when interpreting estimates and their variation.
  - Data users should be aware of potential limitations due to exclusions and the need to use provided weights and bootstrap-derived uncertainty.
  - Metadata and data formats should reflect the stratification, class definitions by country, and sampling exclusions to ensure proper interpretation and reproducibility.

- References
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Cochran (1963): Sampling Techniques
  - Efron and Tibshirani (1993): An Introduction to the Bootstrap