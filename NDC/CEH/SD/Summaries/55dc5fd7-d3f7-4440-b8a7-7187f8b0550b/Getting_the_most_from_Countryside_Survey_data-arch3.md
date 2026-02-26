# Notes on the downloadable data

- Precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify square locations with precision better than 100 square km.

- CS Field Survey design:
  - Based on a sample of 1 km squares across GB.
  - Measurements are taken at two levels: whole square (characterising the square) and within-square (describing features inside the square).
  - Variables range from binary to continuous (e.g., areas, lengths).

- Sampling design and representativeness:
  - The CS sample squares are not a random subset of all GB squares; they are stratified within designated strata.
  - Strata are defined by the ITE Land Classification, with country-specific revisions:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Because of historical changes, classifications evolved from 32 → 42 → 45 land classes to accommodate separate country reporting.

- Exclusions and representativeness:
  - Squares with more than 90% sea or more than 75% urban area (as measured on 1:250,000 OS maps) were excluded from field surveys.
  - Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; this is likely a small bias except in regions with high sea/urban square proportions.

- Estimation and uncertainty:
  - Official GB land class estimates are produced as ratio estimates, weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to skewness in some features.

- References:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap

# Sampling Considerations in the use of Countryside Survey Data

- Dual-level sampling and data structure:
  - Sampling occurs at the square level and within-square level; measurements are collected at both levels and include a mix of binary and continuous variables.

- Implications for analysis:
  - The stratified sampling design must be accounted for in analyses; ignoring stratification can lead to non-representative estimates and incorrect variation.
  - Analyses should use the Land Classification strata, with awareness that classifications differ slightly by country.

- Country-specific classifications:
  - Historical changes in Land Classification necessitate careful handling when comparing across England, Wales, and Scotland.
  - Separate country classifications (England 21, Wales 8, Scotland 16) affect cross-country comparability and aggregation.

- Representativeness and potential bias:
  - GB/region estimates rely on the assumption that vegetative land in excluded squares resembles that in sampled squares; potential bias is a concern mainly in regions with high sea/urban square proportions.

- Uncertainty estimation:
  - Bootstrap methods have been used since 1998 to estimate standard errors due to skewness in some features.

- Practical takeaway for monitoring frameworks:
  - When using CS data, implement stratified analyses aligned with Land Classification, apply appropriate weights by vegetative land area, and use bootstrap-based uncertainty assessments.
  - Be cautious with region-wide or cross-country comparisons due to differing country classifications and exclusion criteria.