# Notes on the downloadable data

- Overview
  - The precise locations of Countryside Survey squares are kept confidential by UKCEH. External users are limited to a precision no better than 100 square km, so you cannot determine whether survey squares fall within areas defined at finer resolutions.

- Sampling design and representation
  - Countryside Survey field data come from a sample of 1-km squares in Great Britain, with measurements at both the square level and within-square features.
  - The sample is not a random subset; it is stratified by the ITE Land Classification. Countries use different classifications (England: 21 classes, Wales: 8, Scotland: 16).
  - Analyses that ignore stratification may yield unrepresentative estimates and incorrect variation.
  - Not all 1-km squares were surveyed: squares that are >90% sea or >75% urban were excluded. Estimates for GB or regions assume remaining vegetative land in excluded squares is similar to sampled squares; bias is considered small, but regional issues may occur if there is a high proportion of sea/urban squares.

- Estimation and uncertainty
  - Official land-class estimates are produced using ratio estimation (Cochran, 1963) with weights based on the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness concerns.

- Practical guidance for GIS work
  - When mapping or analyzing CS data, account for stratification by land class and the area-based weighting.
  - Be aware of data confidentiality and the 100 square km precision limit when interpreting location-specific results.
  - Use bootstrap-based uncertainty measures for results, and note potential regional biases if a region contains many sea or urban squares.
  - Understand that the data represent selected squares and within-square measurements, not a complete coverage of GB; extrapolation relies on assumed similarity of excluded areas.

- Data structure and measurements (high level)
  - Data comprise information from 1-km squares with two levels of measurements: square-level and within-square features (e.g., vegetation, soils). Measurements vary from binary to continuous.

- References
  - Barr et al. (1993); Cochran (1963); Efron and Tibshirani (1993).