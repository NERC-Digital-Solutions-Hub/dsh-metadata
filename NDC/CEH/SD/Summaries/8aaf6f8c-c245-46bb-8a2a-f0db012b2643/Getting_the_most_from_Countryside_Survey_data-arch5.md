# Notes on the downloadable data

## Data confidentiality and precision
- The precise locations of Countryside Survey (CS) survey squares are confidential to preserve representativeness.
- External users cannot identify square locations with precision better than 100 square kilometers.

## Sampling design and data structure
- CS Field Survey data come from a sample of 1 km squares in Great Britain.
- There are two sampling levels: whole squares and within-square measurements (e.g., quadrats for vegetation, soils, etc.).
- Measurements include a mix of binary and continuous variables.
- The sample is not a random subset; it is stratified by the ITE Land Classification.
- Country-specific classifications: England (21 classes), Wales (8 classes), Scotland (16 classes).
- Some squares are excluded from field survey: squares more than 90% sea or more than 75% urban.
- Estimates are effectively representative only of included squares; extrapolation to the whole GB assumes excluded areas resemble included ones, which may introduce bias, especially where sea/urban areas are proportionally large.
- Estimation approach: ratio estimates by land class, weighted by the vegetative land area in each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.

## Data use, metadata and governance
- Documentation should clearly describe the sampling design, stratification, exclusions, and estimation methods to support correct analysis and reproducibility.
- Users must account for stratification and weighting when deriving GB- or region-level estimates.
- Sharing and usage should respect confidentiality and any data limitation notes; updates to datasets should maintain consistency with the sampling framework.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.