# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by UKCEH to preserve representativeness of the wider countryside. External users will not be able to identify square locations with precision better than 100 square km.

- CS field survey data design:
  - Based on a sample of 1 km squares in Great Britain (GB).
  - Each selected square is mapped and measured at two levels: the square as a whole and features within the square (e.g., quadrats for vegetation, soils, etc.).
  - Measurements span binary and continuous variables.

- Sampling design and representativeness:
  - The sample is not a random subset of GB squares; it is stratified by the ITE Land Classification.
  - Land Classification has been revised over time and now varies by country (England, Wales, Scotland) with 21, 8, and 16 classes respectively.
  - Estimates that do not account for stratification may be unrepresentative and have incorrect variance estimates.

- Exclusions and potential bias:
  - Squares with more than 90% sea area or more than 75% urban area (as measured from 1:250,000 OS maps) were excluded from field surveys.
  - Official GB or regional estimates assume vegetative land in excluded squares is similar to that in sampled squares. This assumption is generally reasonable due to the small total area affected, but can be problematic for regions with high proportions of sea or urban squares.

- Estimation techniques:
  - Because of skewness in some features, estimates are produced as ratio estimates (by land class) using the vegetative land area as weights within each class.
  - Weights are combined across land classes to produce GB-wide estimates based on the total vegetative land area.
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness concerns.

- Measurement and analysis implications:
  - The data involve multiple sampling levels and varied measurement types, requiring careful handling of within-square and between-square variation.
  - Analysts should incorporate the stratified design (land class and country) and the weighting scheme when deriving inferences.
  - Be mindful of the confidentiality constraints and the limitations they impose on precise geographic identification.

- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.