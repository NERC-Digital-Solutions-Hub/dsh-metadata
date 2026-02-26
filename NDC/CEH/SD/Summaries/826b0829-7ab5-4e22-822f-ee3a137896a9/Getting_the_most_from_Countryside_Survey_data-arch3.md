# Notes on the downloadable data

- Purpose and scope
  - Describes how Countryside Survey (CS) field data are collected, sampled, and analyzed to support monitoring and policy evaluation.
  - Highlights implications for representativeness, metadata, and uncertainty in environmental health reporting.

- Data privacy and location visibility
  - Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
  - External users cannot identify square locations with precision better than 100 square kilometers.

- Sampling design and levels
  - CS field data come from a sample of 1 km squares across Great Britain (GB).
  - Two sampling levels: the square as a unit, and measurements within each square (e.g., quadrats for vegetation, soils, etc.).
  - Not a random sample; it is a stratified sample within designated strata.

- Stratification and land classification
  - Stratification is defined by the ITE Land Classification.
  - Land classification has changed over time:
    - Originally 32 land classes.
    - 1998: expanded to 42 classes to support separate Scotland reporting.
    - 2007: expanded to 45 classes due to Wales-focused reporting; each country now has a separate classification (England 21, Wales 8, Scotland 16).

- Representativeness and coverage
  - Estimates that ignore stratification may be biased and misrepresent variation.
  - Not all GB squares are surveyed: squares more than 90% sea or more than 75% urban are excluded.
  - In practice, GB-wide estimates assume excluded areas are similar in vegetative land composition to sampled squares; bias is considered negligible unless a region has a high sea/urban proportion.

- Estimation and weighting
  - Official estimates are produced as ratio estimates by land class, incorporating the area of vegetative land within each class.
  - Land class estimates are combined using weights based on vegetative land area for the class.

- Uncertainty and statistical methods
  - Since some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (since 1998).

- Practical implications for monitoring frameworks
  - When using CS data, account for stratification and weighting to obtain valid inferences.
  - Be mindful of privacy constraints limiting precise location data for reproducibility and linkage with other datasets.
  - Use bootstrap-based uncertainty measures to convey confidence in estimates, especially for skewed features.

- References
  - Barr, C.J. et al. 1993. Countryside Survey 1990 Main Report.
  - Cochran, W.G. 1963. Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. 1993. An Introduction to the Bootstrap.