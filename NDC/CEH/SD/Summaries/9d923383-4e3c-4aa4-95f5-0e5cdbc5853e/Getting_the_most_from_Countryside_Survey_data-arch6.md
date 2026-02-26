# Notes on the downloadable data

- Purpose and scope
  - Describes Countryside Survey (CS) Field Survey data: information from a sample of 1 km squares across Great Britain, with measurements at both the whole-square level and within-square features (e.g., vegetation, soils).
  - Data types range from binary to continuous, collected to characterize squares and sub-features.

- Confidentiality and data access
  - Precise locations of survey squares are kept confidential by CEH.
  - External users cannot identify whether squares fall within defined areas with precision better than 100 square km.

- Sampling design and representativeness
  - The CS sample is not a random subset of all GB squares; it is stratified by land classification (ITE) with country-specific classifications (England, Wales, Scotland).
  - Land classification history: originally 32 classes; revised to 42 (1998, Scotland reporting), then 45 (2007, Wales reporting). Each country effectively has its own classification (England: 21, Wales: 8, Scotland: 16).
  - Not all GB squares were surveyed: squares with area >90% sea or >75% urban were excluded from field survey.
  - Official estimates are based on ratio estimates by land class, weighting by vegetative land area within each land class. Excluded squares are assumed to be similar in vegetation to sampled squares; this assumption introduces potential bias mainly in areas with many sea/urban squares.

- Analysis considerations and methods
  - Analyses must account for the two-stage sampling (whole square and within-square measurements) and stratification by land class.
  - Estimation approach uses ratio estimates for each land class, then combines them using vegetative land area as weights.
  - Because some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (since 1998).

- Practical implications and caveats
  - Estimates for the entire GB or large regions may be biased if the exclusion criteria (sea/urban areas) are a larger share of the region.
  - Users should be mindful of stratification when interpreting variation and representation; unadjusted analyses may misstate uncertainty or representation.

- References for methodology
  - Barr et al. (1993) Countryside Survey 1990 Main Report.
  - Cochran (1963) Sampling Techniques.
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap.