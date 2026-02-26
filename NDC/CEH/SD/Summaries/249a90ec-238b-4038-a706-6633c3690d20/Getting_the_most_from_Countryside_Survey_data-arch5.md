# Notes on the downloadable data

## Overview and governance context
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness.
- External users will not be able to identify survey squares with precision finer than 100 square km.
- Data stewards should document and communicate location privacy constraints, provenance, and representativeness when sharing or reusing the data.

## Data content and sampling design
- CS field survey data are from a sample of 1 km squares across GB, with measurements at both the square level and within-square features (e.g., quadrats for vegetation, soils).
- Measurements include a mix of binary and continuous variables.
- Sampling is not a simple random subset; it is stratified by the ITE Land Classification.
- Land Classification classifications are country-specific and have evolved:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
  - Historical changes: 32 → 42 classes (1998) → 45 classes (post-Wales reporting)
- Some GB squares were excluded from field surveys (areas >90% sea or >75% urban) with extrapolation assumptions for vegetative land in excluded squares.
- Official estimates are produced using ratio estimates by land class, weighted by vegetative land area in each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness.

## Data quality, limitations, and implications
- Estimates assume stratified sampling and area-based weighting; analyses that ignore stratification may be biased.
- Exclusion criteria introduce potential bias in regions with high sea/urban square proportions, though overall impact is generally small.
- Users must account for sampling design, weights, and bootstrap SEs to obtain valid inferences.
- Metadata should clearly describe:
  - Sampling strata and classification mappings
  - Exclusion criteria and rationale
  - Weighting scheme and bootstrap procedures
  - Any country-specific classification nuances

## Confidentiality, access, and reuse considerations
- Location privacy constraints limit precise square identification; this affects spatial analyses requiring exact geolocations.
- Data sharing policies should reflect the confidentiality practices and the 100 square km precision threshold.

## Guidance for data users and data stewards
- When reusing CS data, apply appropriate survey weights and account for stratification and bootstrap-derived uncertainty.
- Align analyses with the country-specific Land Classification definitions and ensure cross-country comparability is handled carefully.
- Provide thorough provenance, including references to sampling design and estimation methods, in metadata and user documentation.

## Practical references
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.