# Notes on the downloadable data

- Location confidentiality: The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify squares with precision better than 100 square km.

- Data structure and sampling levels:
  - CS field survey uses a sample of 1 km squares across Great Britain.
  - Measurements are taken at two levels: characteristics of the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.).
  - Data include a mix of binary and continuous variables.

- Sampling design and representativeness:
  - The sample is stratified, not a random subset, using the ITE Land Classification.
  - Land classification has evolved from 32 to 45 classes, with separate classifications for England, Wales, and Scotland (England: 21, Wales: 8, Scotland: 16).
  - Estimates without accounting for stratification may be unrepresentative; proper analysis requires incorporating the stratified design.

- Exclusions and potential bias:
  - Squares with more than 90% sea or more than 75% urban area (per 1:250,000 OS maps) were excluded from field survey.
  - Official GB estimates are based on the included squares; regional GB estimates assume excluded areas have similar vegetative land composition, which may introduce bias only in regions with substantial sea/urban coverage.

- Estimation methods:
  - Land-class estimates are produced using ratio estimates, weighted by the vegetative land area within each land class.
  - From 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness.

- Implications for analysts:
  - Interpretations must consider the stratified sampling, weighting, and exclusions.
  - For data sharing and integration, acknowledge confidentiality and the need to use the prescribed weighting and bootstrap-based uncertainty estimates.

- References (methodological context):
  - Barr et al. 1993; Cochran 1963; Efron & Tibshirani 1993.