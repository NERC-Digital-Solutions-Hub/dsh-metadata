# Notes on the downloadable data

## Key points
- Countryside Survey (CS) field data come from a sample of 1 km squares across GB, with measurements at two levels: the square level and within-square features.
- Data types include both binary and continuous variables (e.g., areas, lengths, vegetation and soil measurements).
- The sample is not random; it is stratified by the ITE Land Classification, with country-specific refinements (England: 21 classes, Wales: 8, Scotland: 16; 32 original classes evolved to 42 in 1998 for Scotland, 45 in 2007 for Wales).

## Data confidentiality and access
- The precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify square locations with precision finer than 100 square kilometres.

## Sampling design and levels
- Two sampling levels:
  - Whole 1 km square: general characterization.
  - Within-square: detailed measurements (e.g., quadrats for vegetation, soils).
- The CS sample squares are not a random subset of all GB squares; the stratified design requires proper weighting and stratification handling in analyses.
- Some squares are excluded from field surveys if more than 90% sea or more than 75% urban, based on 1:250000 OS map area.
- Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares, which may introduce bias mainly in regions with high sea/urban coverage.

## Implications for analysis
- Analyses must account for stratification by land class; failing to do so can yield unrepresentative estimates and incorrect variation.
- When using CS data for GB or regional estimates, consider the weighting by vegetative land area within each land class.
- Be aware of potential biases in regions with substantial excluded land (sea/urban).

## Estimation and uncertainty
- Ratios are used to estimate land-class-level metrics, then combined using area-based weights.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness in some features.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.