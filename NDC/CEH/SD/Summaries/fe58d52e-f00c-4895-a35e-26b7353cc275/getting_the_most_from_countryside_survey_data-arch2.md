# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) squares are kept confidential by UKCEH to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision finer than 100 square km.
- CS field data come from a sample of 1-km squares across Great Britain (GB). Each selected square is mapped and detailed measurements are collected for features such as vegetation and soils, with two levels of sampling: measurements for the square as a whole and measurements within the square (e.g., quadrats).
- Measurements vary in type, from binary (yes/no) to continuous (areas, lengths).

- Sampling design and representativeness
  - The CS sample squares are not a random subset of all GB 1-km squares; the sample is stratified within designated strata defined by the ITE Land Classification.
  - Land Classification classifications have evolved: 32 classes originally; expanded to 42 in 1998 for Scotland; further revised to 45 classes in 2007 for Wales. In practice, each country has its own set of classes (England: 21, Wales: 8, Scotland: 16).
  - Estimates that do not account for stratification may be non-representative and have inaccurate variation estimates.
  - Not all GB squares were surveyed. Squares with area more than 90% sea or more than 75% urban, as determined from 1:250,000 scale OS maps, were excluded. Estimates for GB or regional scales are then derived by assuming similarity in vegetative land composition between excluded and surveyed squares—an assumption that is generally reasonable because the excluded area is small, though problems may arise if a region has a high proportion of sea or urban squares.

- Estimation and statistical methods
  - Official GB land class estimates are calculated using ratio estimates that weight the area of vegetative land within each sample square.
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.

- Practical references
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.