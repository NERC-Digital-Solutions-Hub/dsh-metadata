# Notes on the downloadable data

- Data confidentiality: The exact locations of Countryside Survey (CS) survey squares are held in confidence by UKCEH. External users will not receive locations with precision better than 100 square kilometres, so you cannot determine whether specific squares fall within defined areas below this threshold.

- Sampling framework: CS involves field data from a sample of 1 km squares across Great Britain. Each selected square is mapped and measured at two levels: the square level (characterising the whole square) and within-square (detailed measurements of features inside the square). Measurements range from binary variables to continuous metrics (e.g., areas, lengths).

- Non-random, stratified design: Squares are not a random subset of all GB squares. The sample is stratified by Land Classification (ITE). Land Classification has evolved from 32 classes (original) to 42 (1998) and 45 (2007) to accommodate country reporting differences. England has 21 classes, Wales 8, Scotland 16. Analyses ignoring stratification may be unrepresentative and have biased variation estimates.

- Exclusions and representativeness: Some GB squares were excluded from field survey if their area was more than 90% sea or more than 75% urban (per 1:250,000 OS maps). Official GB estimates assume excluded squares have similar vegetative land composition to included squares. This assumption generally has negligible bias unless a region contains a large share of sea or urban land.

- Estimation and uncertainty: Estimates are produced as ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) to address potential skewness in features.

- Practical implications for GIS users: When using CS data, apply the stratification by Land Classification and square-area weights; be mindful of the confidentiality threshold (100 km2 precision) which limits precise geolocation analyses; account for the sampling design and potential biases due to excluded squares in regional analyses.

- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.