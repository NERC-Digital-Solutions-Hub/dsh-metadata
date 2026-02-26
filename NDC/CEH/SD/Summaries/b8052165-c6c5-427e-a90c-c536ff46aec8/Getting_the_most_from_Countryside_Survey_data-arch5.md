# Notes on the downloadable data

- Purpose of confidentiality
  - To preserve representativeness of the wider countryside, exact locations of Countryside Survey (CS) squares are kept confidential by CEH.
  - External users cannot identify whether any survey squares fall within defined areas with precision greater than 100 square km.

- Sampling design and levels
  - CS field data come from a sample of 1 km squares across GB.
  - Two sampling levels:
    - Whole square: general characteristics.
    - Within-square: detailed measurements (e.g., quadrats for vegetation, soils, etc.).
  - Measurements occur at both levels; some describe the square as a unit, others describe features within the square.
  - The CS sample is not a random subset of GB squares; it is stratified by land classification.

- Land classification and stratification
  - Stratification is based on the ITE Land Classification.
  - Classification history:
    - Original: 32 land classes.
    - 1998: revised to 42 classes (Scotland-specific reporting).
    - 2007: further revision for Wales; resulting in 45 classes total.
  - England, Wales, and Scotland have country-specific classifications (England 21, Wales 8, Scotland 16).
  - Analyses that ignore stratification may be non-representative and misstate variation.

- Exclusions and representativeness
  - Squares with more than 90% sea or more than 75% urban area were excluded from field surveys.
  - Official GB estimates assume excluded squares are similar in vegetative land composition to sampled squares.
  - This assumption is generally acceptable since the excluded area is small; region-level bias is more likely where there is a high proportion of sea or urban squares.

- Estimation and uncertainty
  - Estimates are produced as ratio estimates for each land class, accounting for the vegetative land area in each sample square.
  - Land-class estimates are combined using weights based on the vegetative land area of each land class.
  - Since some features are skewed, standard errors and confidence intervals since 1998 are estimated using bootstrap methods (Efron & Tibshirani, 1993).

- Data governance and usage considerations for stewards
  - Acknowledge the stratified sampling design when analyzing CS data; pooling across land classes without weights may misstate totals or variability.
  - Be aware of confidentiality constraints that limit precise geographic pinpointing; this affects spatial analyses at fine scales.
  - Ensure metadata documents reflect the sampling framework, inclusion/exclusion criteria, and bootstrap-based uncertainty measures.
  - Reference provenance and methodological notes (e.g., classification history and estimation approach) to support reproducibility and proper interpretation.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.