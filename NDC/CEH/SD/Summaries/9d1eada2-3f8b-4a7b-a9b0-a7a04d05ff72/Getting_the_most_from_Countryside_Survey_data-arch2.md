# Notes on the downloadable data

- Precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify squares to a precision better than 100 square km.
- Consequently, users cannot determine whether any survey squares fall within defined areas below this precision threshold.

## Sampling design and data structure

- CS field survey data come from a sample of 1 km squares across Great Britain (GB). Each square is mapped and detailed measurements are taken at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Measurements include both binary (yes/no) and continuous variables (areas, lengths, etc.).

## Representativeness and extrapolation considerations

- The sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification, with country-specific adaptations.
- Land Classification history:
  - Originally 32 classes.
  - 1998: Scotland reporting required → 42 classes.
  - 2007: Wales reporting required → 45 classes.
  - Result: England has 21 classes, Wales 8, Scotland 16; effectively country-specific classifications.
- Some GB squares were excluded from field survey:
  - Excluded if more than 90% sea area or more than 75% urban area (per 1:250,000 OS maps).
  - Thus, official GB or regional estimates reflect only the included squares; extrapolation assumes vegetative land in excluded squares is similar to included squares, which is usually reasonable but can be problematic if a region has a high sea/urban proportion.
- Because of the sampling design, estimates must account for stratification and weighting; naïve analyses that ignore these aspects may be biased.

## Estimation methods and uncertainty

- Estimate construction:
  - Uses ratio estimates (Cochran, 1963) for each land class, weighting by the vegetative land area within each class.
  - Land class estimates are then combined using weights equal to the vegetative land area of each class across GB or regional extents.
- Uncertainty measures:
  - Since some features can be skewed, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) since 1998.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.