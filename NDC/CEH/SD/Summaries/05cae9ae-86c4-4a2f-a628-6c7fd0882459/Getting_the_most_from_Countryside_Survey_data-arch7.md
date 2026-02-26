# Notes on the downloadable data

- Confidentiality and precision
  - Precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
  - External users are limited to a precision of 100 square km; users cannot determine whether squares fall within defined areas below this threshold.

- Sampling design and data structure
  - CS field survey data come from a sample of 1 km squares across GB.
  - Each selected square is mapped and measured at two levels: whole square and within-square features.
  - Data types range from binary (yes/no) to continuous (areas, lengths), with measurements taken at both levels.
  - The sampling is not random; it is stratified by the ITE Land Classification.
  - Land classification history:
    - Original classification: 32 land classes.
    - 1998: Scotland reporting necessitated changes, increasing to 42 classes.
    - 2007: Wales reporting changes increased to 45 classes.
    - Result: country-specific classifications (England 21, Wales 8, Scotland 16).

- Representativeness and limitations
  - Estimates derived from CS data assume stratification is properly accounted for; estimates without stratification may be unrepresentative and have incorrect variation estimates.
  - Not all GB squares were surveyed:
    - Squares with >90% sea or >75% urban area (per 1:250,000 OS maps) were excluded.
    - Estimates for GB or regions assume vegetative land in excluded squares resembles sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.

- Estimation and weighting
  - Official estimates are produced using ratio estimates for each land class, weighted by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.

- Practical implications for GIS use
  - When mapping or aggregating CS data, account for stratification and use appropriate land-class weights.
  - Exercise caution when interpreting results for regions with substantial sea or urban areas or when applying estimates to small areas.
  - Be mindful of data confidentiality limits, which affect precision and location-based analyses.

- References
  - Barr, C.J., et al. Countryside Survey 1990 Main Report (1993).
  - Cochran, W.G. Sampling Techniques (2nd ed., 1963).
  - Efron, B. & Tibshirani, R.J. An Introduction to the Bootstrap (1993).