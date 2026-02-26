# Notes on the downloadable data and Sampling Considerations in the use of Countryside Survey Data

- Privacy and representativeness
  - Precise locations of Countryside Survey (CS) field squares are confidential and only identifiable to a precision of 100 square km. This preserves the representativeness of the wider countryside but prevents external users from identifying whether squares fall within defined areas below this threshold.

- Structure of CS data
  - Data come from a sample of 1 km squares in Great Britain, with measurements at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.).
  - Measurements are diverse (binary to continuous) and require careful handling to reflect the hierarchical (two-level) sampling design.

- Sampling design and stratification
  - The CS sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification.
  - Land classification has evolved by country: originally 32 classes; Scotland added adjustments in 1998 for separate reporting (42 classes); Wales adjustments in 2007 (45 classes total), resulting in country-specific classifications (England 21, Wales 8, Scotland 16).
  - Estimates must account for this stratification to avoid biased results.

- Exclusions and representativeness
  - Squares with more than 90% sea or more than 75% urban area were excluded from field surveys.
  - Official GB estimates assume remaining vegetative land in excluded squares is similar to sampled squares; bias is generally negligible unless a region has high proportions of sea/urban squares.

- Estimation and uncertainty
  - Estimates by land class are produced using ratio estimation, weighted by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals have been estimated with the bootstrap method (to address skewness in some features).

- Data availability and governance implications for monitoring teams
  - Public sharing of underlying datasets may be constrained by confidentiality and governance requirements.
  - Metadata quality can be variable; transformations may be required to render data usable.
  - Analysts should be mindful of data provenance, required transformations, and governance considerations when integrating CS data into monitoring frameworks.

- Practical guidance for authors of monitoring frameworks
  - When using CS data, incorporate the stratified design and country-specific land classifications into analyses.
  - Use ratio estimation with appropriate area weights and bootstrap-based uncertainty measures.
  - Acknowledge and adjust for any exclusions (sea/urban) and their potential regional biases.
  - Plan for data access and metadata needs, and be prepared for privacy-related constraints on precise location information.

- References
  - Barr, C.J., et al. 1993. Countryside Survey 1990 Main Report.
  - Cochran, W.G. 1963. Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. 1993. An Introduction to the Bootstrap.