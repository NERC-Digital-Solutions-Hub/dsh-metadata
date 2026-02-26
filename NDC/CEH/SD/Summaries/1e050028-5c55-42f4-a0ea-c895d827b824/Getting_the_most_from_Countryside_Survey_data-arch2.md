# Notes on the downloadable data

- Purpose and confidentiality
  - CEH holds precise locations of Countryside Survey (CS) field survey squares to preserve representativeness; external users receive locations no more precise than 100 square km.
  - This prevents identification of whether survey squares fall within defined areas below the 100 km² threshold.

- Data structure and content
  - CS field survey data come from a sample of 1 km squares in Great Britain.
  - Each selected square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include a mix of binary and continuous variables.

- Sampling design
  - The squares are not a random subset; the sample is stratified by ITE Land Classification.
  - Land Classification evolution by country:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - The classification changed over time (32 → 42 → 45 classes) to accommodate separate country reporting.

- Coverage and representativeness
  - Not all GB squares were considered for field survey.
  - Excluded squares: more than 90% sea or more than 75% urban (as per 1:250,000 OS maps).
  - Estimates for GB or regions assume vegetative land in excluded squares is similar to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

- Estimation methods
  - Official estimates use ratio estimation (Cochran, 1963) for each land class, incorporating the area of vegetative land in each sample square.
  - Land-class estimates are combined using weights based on the vegetative land area of each land class.

- Uncertainty and standard errors
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.

- Practical implications for analysts
  - Analyses must account for stratification and weighting to avoid biased inferences.
  - Simple random-sample assumptions are inappropriate; regional and GB-level estimates rely on proper weighting and inclusion of land-class structure.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.