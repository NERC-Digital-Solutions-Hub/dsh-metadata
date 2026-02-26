# Notes on the downloadable data

- Confidentiality and precision: The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify square locations with precision finer than 100 square km. Consequently, you cannot determine whether survey squares fall within defined areas below this threshold.

- What CS Field Survey data contains: Data come from a sample of 1 km squares in Great Britain, with measurements at two levels (the whole square and features within the square). Measurements range from binary to continuous variables and cover vegetation, soils, and related features.

- Sampling design and representativeness: The sample squares are not a random subset; they are stratified within designated strata defined by the ITE Land Classification. Country-specific classifications exist (England 21 classes, Wales 8, Scotland 16; classifications evolved from 32 to 42 to 45 classes). Estimates not accounting for stratification may be non-representative, with inaccurate variation estimates.

- Excluded squares: Squares that are more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) were excluded from field survey. Official GB or regional estimates assume excluded squares have vegetation similar to sampled squares; bias is likely only where a region has a high proportion of sea/urban squares.

- Estimation and uncertainty: Official estimates are produced by ratio estimates for each land class, weighted by the vegetative land area in each sample square. Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to skewness concerns.

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.

- GIS implications for use:
  - Respect confidentiality by avoiding reliance on precise point locations; prefer aggregated or generalized map representations.
  - Use land-class level, area-weighted estimates and incorporate stratification in any analysis or visualization.
  - Include bootstrap-derived uncertainty (standard errors and confidence intervals) in map-driven decision support.
  - Be aware of potential biases due to excluded squares, especially in regions with substantial sea or urban areas.