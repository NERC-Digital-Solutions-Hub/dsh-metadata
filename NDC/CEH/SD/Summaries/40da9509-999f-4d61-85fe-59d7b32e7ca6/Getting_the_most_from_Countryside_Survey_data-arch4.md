# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision better than 100 square km.
- Consequently, it is not possible to determine if specific survey squares lie inside defined areas below this threshold.

## Sampling design and data structure

- CS field survey data come from a sample of 1 km squares across Great Britain (GB). Each selected square is mapped, and detailed measurements are taken of features within the square, including vegetation and soils via quadrats.
- There are two sampling levels: (1) whole squares, and (2) within-square features. Measurements include a mix of binary and continuous variables (e.g., areas, lengths).
- The sample squares are not a random subset of all GB squares; instead, they are stratified within designated strata defined by the ITE Land Classification.
- Land Classification has evolved: originally 32 classes; expanded to 42 in 1998 for Scotland reporting; further revised to 45 classes in 2007 for Wales reporting. Each country now has its own subclassification (England: 21, Wales: 8, Scotland: 16).

## Representativeness and limitations

- Estimates based on CS data without accounting for stratification may be non-representative and have inaccurate variation estimates.
- Not all GB squares were surveyed: squares with more than 90% sea or more than 75% urban area (per 1:250,000 OS maps) were excluded. Official GB estimates assume non-sampled vegetative land in excluded squares is similar to sampled squares; this assumption is generally acceptable because the excluded area is small, but it could be problematic if a region contains a high proportion of sea or urban squares.

## Estimation methods and uncertainty

- Estimates by land class are produced using ratio estimates and weighted by the vegetative land area of each land class.
- From 1998 onward, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani), addressing skewness in some features.

## Data governance and access considerations

- The data's confidentiality and sampling design have direct implications for data analysis, including:
  - Need to use stratified analysis approaches and apply appropriate weights.
  - Caution when extrapolating beyond surveyed and similar-excluded squares.
  - Preference for bootstrap-based uncertainty measures when communicating precision.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.