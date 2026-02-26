# Notes on the downloadable data

- Confidentiality of locations:
  - Precise locations of Countryside Survey (CS) survey squares are kept confidential by UKCEH.
  - External users cannot identify survey squares to precision finer than 100 square km, so you cannot determine if squares fall within defined areas below this threshold.

- Sampling design and data structure:
  - CS Field Survey data come from a sample of 1 km squares in Great Britain.
  - Each square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include a mix of binary and continuous variables (areas, lengths, etc.).

- Stratified sampling and land classification:
  - The sample is not a random subset but stratified by the ITE Land Classification.
  - Land Classification history:
    - Originally 32 classes.
    - 1998: expanded to 42 classes (Scotland reporting requirements).
    - 2007: expanded to 45 classes (Wales reporting requirements).
  - Each country uses its own classification (England 21 classes, Wales 8, Scotland 16).

- Representativeness and exclusions:
  - Some squares were excluded from field survey: if an area exceeds 90% sea or 75% urban (based on 1:250,000 OS maps).
  - Official estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; this bias is generally small, unless a region has a high proportion of sea or urban land.

- Estimation methodology:
  - Estimates are produced using ratio estimation (Cochran 1963) for each land class, weighting by the vegetative land area in each sample square.
  - Land-class estimates are combined using weights based on the vegetative land area of each land class.
  - Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani 1993) to address skewness in feature estimates.

- References:
  - Barr et al. (1993): Countryside Survey 1990 Main Report.
  - Cochran (1963): Sampling Techniques.
  - Efron & Tibshirani (1993): Bootstrap.

- Practical implications for data use:
  - When analyzing CS data, account for stratification by land class and apply area-based weights.
  - Use bootstrap-derived confidence intervals for inference.
  - Be mindful of the limited precision location data when linking to other geographies; assess potential biases from excluded squares, especially in areas with substantial sea or urban land.