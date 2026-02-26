# Notes on the downloadable data

- The precise locations of Countryside Survey squares are held confidential by UKCEH to preserve representativeness; external users cannot identify square locations with precision finer than 100 square km.

- Sampling design
  - Field survey data come from a sample of 1-km squares across Great Britain.
  - Each selected square is mapped, with detailed measurements within the square (two levels of sampling: whole square and within-square).
  - Measurements include binary and continuous variables (e.g., vegetation, soils).
  - Squares are not a random subset; sampling is stratified within Land Classes defined by the ITE classification.
  - Land Class classifications have evolved:
    - Original 32 classes
    - 1998: 42 classes (Scotland reporting requirement)
    - 2007: 45 classes (Wales reporting requirement)
  - Each country has its own classification (England: 21 classes, Wales: 8, Scotland: 16).

- Representativeness and coverage
  - Estimates may be biased if analyses ignore stratification; official estimates use ratio estimation by land class and weight by vegetative land area within each class.
  - Not all 1-km squares were surveyed; squares with more than 90% sea or more than 75% urban land were excluded.
  - Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; this is generally reasonable due to the small total area excluded, but regional bias can occur if a region contains a large proportion of sea/urban squares.

- Estimation and inference
  - Ratio estimates (Cochran, 1963) are used to derive land-class estimates, weighted by vegetative land area.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.

- Practical implications for data management and use
  - Document and preserve the sampling design, stratification, and weight structures to support correct analysis and interpretation.
  - When combining data across years or regions, align land-class definitions and account for country-specific classifications.
  - Be aware of the limitations related to excluded squares and potential regional biases; adjust analyses accordingly.
  - Maintain clear metadata on data provenance, sampling criteria, and estimation procedures to support reproducibility.

- References
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap