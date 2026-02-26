# Notes on the downloadable data

## Privacy and data access
- Precise locations of Countryside Survey (CS) squares are confidential to protect representativeness.
- External users cannot identify survey squares to a precision finer than 100 square kilometres.

## Sampling design and data structure
- CS field data come from a sample of 1 km squares across Great Britain.
- Two sampling levels: whole square characteristics and within-square features (e.g., quadrats for vegetation, soils).
- Measurements vary from binary to continuous (areas, lengths).
- The sample is stratified by ITE Land Classification; country versions differ:
  - England: 21 land classes
  - Wales: 8 land classes
  - Scotland: 16 land classes
- The classification has evolved: 32 classes originally, then 42 (1998), then 45 (2007) with country-specific reporting.

## Representation and potential bias
- Estimates must account for stratification; ignoring it yields non-representative estimates and wrong variation.
- Not all GB squares were surveyed; excluded if >90% sea or >75% urban (per 1:250,000 OS maps).
- Official GB estimates assume excluded squares are similar in vegetative land to included squares; bias is generally small, except in regions with many sea/urban squares.

## Estimation methods
- Land-class estimates use ratio estimators (Cochran, 1963) weighting by vegetative land area in each sample square.
- Estimates for land classes are combined using weights equal to their total vegetative land area.
- From 1998, standard errors and confidence intervals are estimated via bootstrap (Efron & Tibshirani, 1993) due to skewness concerns.

## Practical guidance for data use
- Incorporate stratification and appropriate weights when analyzing CS data.
- When combining data across countries, align with country-specific land classifications.
- Use bootstrap-based SEs to assess uncertainty, particularly for skewed features.
- Be aware that extrapolation to unsurveyed or heavily sea/urban regions relies on assumed similarity; assess regional applicability. 

## References
- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Cochran (1963). Sampling Techniques.
- Efron & Tibshirani (1993). An Introduction to the Bootstrap.