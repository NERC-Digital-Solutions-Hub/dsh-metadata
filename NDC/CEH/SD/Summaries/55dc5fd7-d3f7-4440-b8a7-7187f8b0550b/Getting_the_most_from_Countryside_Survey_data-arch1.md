# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH. External users cannot identify squares with precision finer than 100 square kilometres, limiting geographic pinpointing within defined areas.

- CS field survey data are based on a two-level sampling design:
  - Whole 1 km squares are selected and mapped.
  - Within each square, quadrats are laid out to collect additional vegetation, soils, and other measurements.
  - Measurements include both binary and continuous variables, yielding characterisation at the square level and within-square features.

- Sampling is not a simple random sample. It is stratified by the ITE Land Classification, with country-specific classifications:
  - England: 21 land classes
  - Wales: 8 land classes
  - Scotland: 16 land classes
  - The Land Classification system evolved from 32 to 42 to 45 classes over time due to reporting requirements (England/Scotland/Wales).

- Exclusions and representativeness:
  - Squares with more than 90% sea or more than 75% urban area were excluded from field surveying.
  - Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares. This is generally reasonable since the excluded land is small, but regional biases could appear if a region has a high proportion of sea/urban squares.

- Estimation method:
  - Estimates by land class are produced using ratio estimates, weighted by the vegetative land area within each land class.
  - Land-class estimates are combined using weights equal to the vegetative land area of each land class overall.
  - From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods to address skewness (Efron and Tibshirani, 1993).

- Practical implications for analysts:
  - When analysing CS data, account for stratification by Land Classification and the weighting by vegetative land area.
  - Be cautious of potential biases if a region contains a high proportion of excluded squares (sea/urban).
  - The bootstrap approach should be used for SEs and CIs due to skewed feature distributions.

- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.