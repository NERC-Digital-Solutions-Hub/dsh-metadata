# Notes on the downloadable data

## Data confidentiality and precision
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
- External users will not be able to identify square locations with precision better than 100 square kilometres.
- Consequently, users cannot determine whether squares fall within defined areas below this threshold.

## Sampling design and data structure
- CS field survey data are collected from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and detailed measurements are taken (e.g., quadrats for vegetation, soils, etc.).
- There are two sampling levels: measurements characterising the square as a whole and measurements within each square.
- Data types range from binary (yes/no) to continuous (areas, lengths).

## Stratification and classifications
- The sampling is not a random subset; it is stratified by the ITE Land Classification.
- Land classifications have evolved:
  - Originally 32 classes
  - 1998: expanded to 42 classes (Scotland reporting introduced)
  - 2007: further revision for Wales reporting, resulting in 45 classes
- Each country has its own classification (England: 21, Wales: 8, Scotland: 16).
- Estimates that do not account for stratification may be unrepresentative and misstate variation.

## Excluded squares and representativeness
- Squares excluded from field surveys: those with more than 90% sea area or more than 75% urban area (per Countryside Survey 1990 Main Report).
- Official GB/regional estimates assume vegetative land in excluded squares is similar to sampled squares.
- Bias is expected to be negligible generally, except where a region contains a high proportion of sea or urban squares.

## Estimation and uncertainty
- Official land-class estimates are produced using ratio estimation (Cochran, 1963), weighted by the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness in some features.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.