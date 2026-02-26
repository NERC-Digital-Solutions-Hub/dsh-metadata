# Notes on the downloadable data

- Overview
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users cannot identify whether survey squares fall within defined areas with precision better than 100 square km.

- Sampling design and data structure
  - Countryside Survey field data come from a sample of 1-km squares in Great Britain.
  - Each selected square is mapped and measurements are taken both at the square level and within each square (e.g., multiple quadrats for vegetation, soils, etc.).
  - Data types range from binary indicators to continuous measures (areas, lengths).

- Non-random, stratified sampling
  - The sample is not a random subset of all 1-km squares; it is stratified within designated strata.
  - Stratification is defined by the ITE Land Classification.
  - Land classification has evolved: originally 32 classes; 1998 revision for Scotland reporting increased to 42 classes; 2007 Wales reporting led to 45 classes. England, Wales, and Scotland use country-specific classifications (21, 8, and 16 classes, respectively).
  - Because estimates are produced with stratification in mind, failing to account for stratification can yield non-representative estimates and incorrect variation.

- Inclusion/exclusion and potential biases
  - Squares excluded from field survey if their area is more than 90% sea or more than 75% urban (per 1:250,000 OS maps).
  - Official GB estimates are for the squares meeting inclusion criteria; it is assumed vegetative land in excluded squares is similar to that in sampled squares.
  - This assumption generally introduces negligible bias unless a region has a high proportion of sea or urban areas.

- Estimation and inference
  - Estimation uses ratio estimation techniques for land class, weighting by the area of vegetative land in each class.
  - From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods to address skewness (Efron & Tibshirani).

- Practical implications for analysts
  - Always incorporate stratification and area-based weights when analyzing Countryside Survey data.
  - Be cautious when extrapolating results to areas not well represented by the sample (e.g., high sea/urban proportions or non-sampled regions).
  - Use bootstrap-derived uncertainty measures for robust inference due to skewness in some features.

- References
  - Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.