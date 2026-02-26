# Notes on the downloadable data

- Location privacy: precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH; external users cannot identify square locations with precision finer than 100 square km.
- Implication for mapping: users cannot determine whether specific survey squares fall within defined areas below this 100 km² threshold.

## Sampling Considerations in the use of Countryside Survey Data

- Two-level sampling: CS field survey data come from a sample of 1 km squares across GB, with measurements taken both at the square level and within-square (e.g., quadrats for vegetation, soils, etc.), covering a range of data types from binary to continuous.
- Non-random, stratified design: the sample is not a random subset; it is stratified by the ITE Land Classification. Country-specific classifications have evolved (32 → 42 in 1998 → 45 in 2007), resulting in England (21 classes), Wales (8 classes), Scotland (16 classes). Analyses that ignore stratification may yield biased or non-representative estimates.
- Excluded squares: squares with more than 90% sea area or more than 75% urban area (as measured from 1:250,000 OS maps) were not surveyed. Official GB/regional estimates assume similar vegetative composition in excluded squares as in sampled ones; this generally causes negligible bias unless a region contains a high proportion of sea or urban squares.
- Estimation approach: CS land-class estimates are produced using ratio estimators (Cochran, 1963) weighted by the vegetative land area within each land class. Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.
- Practical implications for GIS work:
  - When mapping CS-derived metrics, account for stratification and weighting by vegetative land area within land classes.
  - Be cautious with extrapolations to GB or regional scales due to the sampling design and exclusion criteria.
  - Use bootstrapped standard errors to convey uncertainty, especially for skewed features.
  - Recognize that data are representative only of squares that meet inclusion criteria; regions with high sea/urban proportions may require special interpretation.
- Data provenance references:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.