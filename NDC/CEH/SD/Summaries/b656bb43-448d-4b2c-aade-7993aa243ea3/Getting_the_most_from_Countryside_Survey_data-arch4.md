# Sampling Considerations in the use of Countryside Survey Data

- Overview
  - Countryside Survey (CS) field data come from a sample of 1 km square units across Great Britain, with measurements at both the square level and within-square sub-samples (e.g., quadrats for vegetation and soils).
  - Data types range from binary to continuous measurements (e.g., areas, lengths).

- Confidentiality and data access
  - The precise locations of survey squares are kept confidential by CEH to preserve representativeness.
  - External users cannot identify survey squares with precision finer than 100 square kilometers.

- Sampling design and representativeness
  - The CS sample squares are not a random subset; they are stratified by the ITE Land Classification.
  - The Land Classification has evolved over time: originally 32 classes, then 42 (1998 Scotland reporting), then 45 (2007 Wales reporting). Each country effectively has its own classification (England: 21, Wales: 8, Scotland: 16).
  - Estimates must account for stratification; ignoring it can yield non-representative estimates and mischaracterize variation.
  - Not all squares were considered for field survey: squares more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) were excluded. Official GB estimates assume excluded land is similar in vegetative composition to sampled squares; this is generally a small bias, except in regions with high sea/urban proportions.

- Estimation methodology
  - Official estimates use ratio estimates for each land class, weighted by the vegetative land area of that class.
  - Since 1998, standard errors and confidence intervals are estimated with bootstrap methods to address skewness in some features.

- Practical implications for data leaders
  - Document and preserve metadata on sampling design, stratification, and weighting to enable correct analysis and reproducibility.
  - Be transparent about confidentiality limits and their impact on spatial analyses and area-based inferences.
  - Ensure data products reflect stratification and the use of bootstrapped uncertainty estimates.
  - When analyzing regional or country-specific subsets, apply the appropriate land-class classifications and sampling weights; be cautious of potential biases if excluding regions with high sea/urban areas.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.