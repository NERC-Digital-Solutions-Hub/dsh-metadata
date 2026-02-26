# Notes on the downloadable data

- Data confidentiality and spatial precision
  - Precise locations of Countryside Survey (CS) survey squares are kept confidential by UKCEH.
  - External users cannot identify square locations with precision better than 100 square kilometres.
  - This constraint limits geographic identification of survey squares within defined areas.

- Sampling design and data structure
  - CS field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Each selected square is mapped and measured at two levels: the square level and within-square features.
  - Measurements include a mix of binary and continuous variables (e.g., quadrat-based vegetation, soils, etc.).

- Non-random, stratified sampling
  - The sampled squares are not a random subset of all GB squares; the design is stratified.
  - Stratification is based on the ITE Land Classification, with country-specific classifications:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Analyses that ignore stratification may yield non-representative estimates and misestimated variation.

- Exclusions and representativeness
  - Squares excluded from field survey if their area is more than 90% sea or more than 75% urban (per 1:250,000 OS maps).
  - Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; this may introduce bias, particularly in regions with high sea/urban coverage (though the affected area is typically small).

- Estimation approach
  - Estimates by land class are produced using ratio estimation, weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani).

- Data provenance and references
  - Methodological references include:
    - Barr et al. (1993) Countryside Survey 1990 Main Report
    - Cochran (1963) Sampling Techniques
    - Efron & Tibshirani (1993) An Introduction to the Bootstrap

- Implications for monitoring and data use
  - Analysts must account for stratified design and weighting to obtain valid inferences.
  - The confidentiality of precise locations necessitates careful handling of spatial analyses and potential aggregation.
  - Metadata quality and provenance are important for evaluating suitability and reliability of outputs.
  - There may be barriers to data sharing due to the requirement to publicly disclose underlying data; governance and data management practices are critical.