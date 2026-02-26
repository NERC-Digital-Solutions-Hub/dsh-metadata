# Notes on the downloadable data

- The Countryside Survey (CS) field data come from a sample of 1-km squares in Great Britain, with measurements made at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.).
- To preserve representativeness, precise square locations are confidential. External users cannot identify square locations with precision better than 100 square kilometres.
- The CS sample is not a random subset of all GB 1-km squares. It is a stratified sample defined by the ITE Land Classification, and since 1990 the land classification has been adjusted for England, Wales, and Scotland (resulting in 21, 8, and 16 classes respectively).

- Exclusions and representativeness:
  - Squares with more than 90% sea or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field survey.
  - Official GB and regional estimates assume that vegetative land in excluded squares is similar to that in sampled squares. This is typically negligible in bias, except where a region has a high proportion of sea or urban squares.

- Estimation and weighting:
  - Estimates by land class are produced as ratio estimates, weighting by the area of vegetative land within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.

- Measurements and data structure:
  - Data include a mix of binary (yes/no) and continuous variables (e.g., areas, lengths) collected at both the square level and within-square level features.

- Key references:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.