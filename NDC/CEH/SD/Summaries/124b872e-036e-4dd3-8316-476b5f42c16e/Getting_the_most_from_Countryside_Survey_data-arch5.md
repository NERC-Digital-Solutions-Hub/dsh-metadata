# Notes on the downloadable data

- Data confidentiality: precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH; external users are not given precision finer than 100 square kilometers, preventing identification of whether squares fall within defined areas below this threshold.

- Sampling design: CS field survey data come from a sample of 1 km squares across Great Britain; measurements are taken at two levels—across whole squares and within-square features; data include binary and continuous variables (e.g., areas, lengths).

- Non-random, stratified sampling: the sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification, with country-specific revisions (32 → 42 → 45 classes; England 21, Wales 8, Scotland 16). Estimates must account for this stratification to avoid misrepresentation and incorrect variation estimates.

- Excluded squares and representativeness: squares with more than 90% sea area or more than 75% urban area were excluded from field surveys; official GB/regional estimates assume vegetative land in excluded squares is similar to sampled squares, an assumption that may introduce bias, especially in regions with high sea/urban proportions.

- Estimation and weighting: official estimates are produced using ratio estimation by land class, weighted by the vegetative land area within each land class; this integrates the area contribution of each class to GB or regional totals.

- Uncertainty and methods: standard errors and confidence intervals for estimates have been estimated using bootstrapping since 1998, addressing skewness in some features (Efron and Tibshirani bootstrap methodology).

- Documentation and provenance: references include Barr et al. (1993) for the 1990 Main Report, and foundational texts on sampling (Cochran, 1963) and bootstrap methods (Efron and Tibshirani, 1993), underscoring the methodological basis for data handling and uncertainty quantification.

- Data governance implications for stewards: 
  - Maintain confidentiality controls (locations limited to 100 km2 precision) and document the rationale.
  - Ensure metadata clearly communicates stratification, sampling design, inclusion/exclusion criteria, and weighting schemes to users.
  - Highlight representativeness limitations due to non-random sampling and country-specific classifications.
  - Track updates to land classifications and ensure analyses incorporate stratification and weighting correctly.
  - Provide information on uncertainty (bootstrapped standard errors) to support robust analyses and decision-making.