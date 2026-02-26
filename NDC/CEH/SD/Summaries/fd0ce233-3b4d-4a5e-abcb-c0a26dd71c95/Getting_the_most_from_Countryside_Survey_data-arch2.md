# Notes on the downloadable data

## Confidentiality and precision of locations
- Precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify whether survey squares fall within defined areas with precision finer than 100 square km.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels: per-square characterisation and within-square features (e.g., quadrats for vegetation, soils).
- Measurements include a mix of binary and continuous variables (e.g., areas, lengths).
- The sampling is not a random subset; it is stratified by land classification (ITE Land Classification).

## Land classification and regional differences
- Land classification details have evolved:
  - Originally 32 classes.
  - 1998: expanded to 42 classes for Scotland reporting.
  - 2007: expanded to 45 classes for Wales reporting.
- Each country now uses a country-specific classification (England: 21 classes, Wales: 8, Scotland: 16).

## Representativeness and limitations
- Estimates derived from CS data that ignore stratification may be biased and not representative.
- In practice, GB estimates rely on weighting by vegetative land area within each land class.
- Some GB squares were excluded from field surveys due to land cover:
  - More than 90% sea
  - More than 75% urban
- Exclusion is small in area; estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares. This assumption may be problematic for regions with substantial sea/urban areas.

## Estimation methods and uncertainty
- Estimates are produced using ratio estimates (Cochran, 1963) for each land class, with weights equal to the vegetative land area of the class.
- From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.

## Practical implications for analysis
- When analyzing CS data, account for the stratified sampling design by land class.
- Use ratio-estimation with appropriate area-based weights for each land class.
- Exercise caution with regions that have a high proportion of sea or urban squares.
- Apply bootstrap-based uncertainty measures to obtain confidence intervals, especially for skewed features.

## References
- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.