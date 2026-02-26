# Notes on the downloadable data

- Privacy and precision: CEH holds precise locations of Countryside Survey (CS) survey squares to preserve representativeness; external users cannot identify square locations to better than 100 square km. This constrains whether a square falls within defined areas.

- Data and sampling structure: CS field data come from a sample of 1 km squares in Great Britain. Each selected square is mapped and measured at two levels: the whole square and within-square features. Measurements include binary and continuous variables, with some data collected via detailed quadrats and vegetation/soil measurements.

- Non-random, stratified design: The square sample is not random but stratified by the ITE Land Classification. Countries have separate classifications (England, Wales, Scotland) with 21, 8, and 16 classes respectively (classification has evolved from 32 to 45 classes due to country-specific reporting needs).

- Implications for representativeness: Estimates based on CS data must account for stratification; failing to do so can yield biased estimates of variation.

- Excluded squares and coverage: Squares with more than 90% sea or more than 75% urban area (by 1:250,000 OS maps) were excluded from field surveys. Official GB estimates assume vegetative land composition in excluded squares is similar to sampled squares; biases are typically negligible unless a region contains a large proportion of sea or urban squares.

- Estimation and uncertainty: Estimates are produced using ratio estimation for each land class, weighted by the vegetative land area of the class. Since some features are skewed, standard errors and confidence intervals have been estimated using bootstrap methods since 1998.

- Practical GIS considerations: When using CS data in mapping and analysis:
  - incorporate stratification and weights
  - account for the representativeness limits due to exclusions
  - use bootstrap-derived uncertainty where applicable
  - be mindful that data reflect only squares meeting survey criteria

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) Bootstrap.