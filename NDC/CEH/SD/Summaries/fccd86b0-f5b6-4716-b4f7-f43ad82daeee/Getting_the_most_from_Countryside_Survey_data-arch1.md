# Notes on the downloadable data

- Confidentiality of survey locations
  - The precise locations of CS survey squares are held in confidence by CEH.
  - External users will not obtain locations with precision better than 100 square km, meaning you cannot identify whether specific survey squares fall within defined areas.

- Sampling design of Countryside Survey (CS)
  - Field data come from a sample of 1 km squares across GB.
  - Each selected square is mapped; measurements are taken at both the square level and within-square level (e.g., quadrats for vegetation, soils).
  - Data types range from binary to continuous (areas, lengths).

- Non-random, stratified sampling
  - The CS sample is not a random subset of all GB squares.
  - It is stratified by the ITE Land Classification.
  - Land classification systems vary by country (England: 21 classes, Wales: 8, Scotland: 16); historically 32, then 42 (1998) and 45 (2007) classes due to separate country reporting.
  - Analyses that ignore stratification may produce unrepresentative estimates and incorrect variation.

- Excluded squares and implications
  - Squares with more than 90% sea or more than 75% urban areas were excluded from field survey.
  - Official GB estimates assume excluded squares are similar in vegetative land composition to sampled squares; bias is generally negligible, except in regions with high sea/urban square proportions.

- Estimation and inference
  - Estimates by land class are produced using ratio estimation, weighted by the area of vegetative land within each land class.
  - Since 1998, standard errors and confidence intervals are estimated with bootstrap methods (Efron & Tibshirani, 1993) to address skewness in features.

- Practical implications for data users
  - Account for stratification and sampling weights in analyses.
  - Use bootstrap-derived standard errors and confidence intervals.
  - Respect location confidentiality and avoid attempting to locate exact squares.
  - When combining data across countries, apply country-specific land classifications and weights; be mindful of potential biases from excluded squares.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.