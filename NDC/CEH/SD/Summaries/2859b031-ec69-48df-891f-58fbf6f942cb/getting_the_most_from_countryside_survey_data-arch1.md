# Notes on the downloadable data

- Overview
  - Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at two levels: the square as a whole and features within the square.
  - Data include a range of variable types from binary to continuous (e.g., area, length).

- Data privacy
  - Precise locations of CS survey squares are confidential and not disclosed to external users at precision finer than 100 square km, preventing identification of squares within defined areas.

- Sampling design
  - The CS sample is not a random subset; it is stratified by land classification (ITE Land Classification).
  - Country-specific classifications have evolved: originally 32 classes; 42 classes in 1998 for Scotland; 45 classes in 2007 with Wales reporting added. England has 21 classes, Wales 8, Scotland 16.
  - Analyses that ignore stratification may yield non-representative estimates or incorrect variation.

- Exclusions and representativeness
  - Squares where 1:250,000-scale OS-map area is more than 90% sea or more than 75% urban were excluded from field survey.
  - Official GB estimates are derived assuming vegetative land in excluded squares is similar to sampled squares; this bias is typically small, unless a region has a high proportion of sea or urban squares.

- Estimation and uncertainty
  - Official land-class estimates are produced using ratio estimation (Cochran, 1963) for each land class, weighting by the vegetative land area of that class.
  - Since 1998, bootstrap methods (Efron & Tibshirani, 1993) are used to estimate standard errors and confidence intervals due to concerns about skewness in some features.

- References
  - Barr et al. (1993); Cochran (1963); Efron & Tibshirani (1993).