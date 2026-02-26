# Notes on the downloadable data

- Confidentiality of locations: precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH; external users only receive data with location precision no better than 100 square km. This prevents identification of whether squares fall within defined areas.

- Sampling design and data structure:
  - Field data come from a sample of 1 km squares in Great Britain, with measurements at two levels: whole squares and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Data types include binary and continuous variables.
  - The sampling is stratified by ITE Land Classification rather than a simple random subset; country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16) with historical changes (32 → 42 → 45 classes) due to separate country reporting.
  - Not all squares were considered for field survey; squares more than 90% sea or more than 75% urban (per 1:250,000 OS maps) were excluded. Estimates for GB or regions assume excluded squares are similar in vegetation to sampled squares; region-specific biases may occur if a region contains many sea/urban squares.

- Estimation and uncertainty:
  - Official estimates are produced using ratio estimates for each land class, weighted by the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals have been estimated with bootstrap methods (to address skewness).

- Implications for data stewardship and user use:
  - Analyses should account for stratified sampling design and weighting; unstratified estimates may be biased.
  - Representativeness is limited to the included squares; caution is needed when interpreting regional or GB-wide results, especially where excluded areas are substantial.
  - Metadata should thoroughly document the sampling design, inclusion/exclusion criteria, stratification, estimation methods, and uncertainty (including bootstrap-based SEs).
  - Data handling practices must maintain confidentiality of precise locations; guidance on appropriate aggregation or location obfuscation should be provided, along with any data sharing or embargo restrictions.

- References:
  - Barr et al. (1993), Cochran (1963), Efron & Tibshirani (1993).