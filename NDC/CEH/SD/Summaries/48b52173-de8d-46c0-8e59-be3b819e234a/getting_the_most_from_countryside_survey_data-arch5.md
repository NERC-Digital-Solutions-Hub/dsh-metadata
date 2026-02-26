# Notes on the downloadable data

- To preserve representativeness of the wider countryside, the precise locations of Countryside Survey (CS) survey squares are held in confidence by UKCEH.
- The locations of squares will not be identified to external users with greater precision than 100 square km, so users cannot determine whether any survey squares fall within defined areas below this threshold.

## Sampling Considerations in the use of Countryside Survey Data

- Field data come from a sample of 1 km squares across Great Britain, with two levels of sampling: the whole square and within-square measurements (e.g., quadrats for vegetation, soils, etc.). Measurements include a range of variable types from binary to continuous.
- The sampling is stratified rather than purely random. Strata are defined by the ITE Land Classification. Classification has evolved from 32 to 42 to 45 classes due to country-specific reporting needs, resulting in England (21 classes), Wales (8), and Scotland (16) being treated separately.
- Estimates that do not account for stratification may be biased. Analyses should reflect the stratified design to obtain valid estimates of variation.
- Some squares were excluded from field survey: those with more than 90% sea or more than 75% urban area at 1:250,000 scale. Consequently, CS field data represent only the included squares; extrapolation to all GB assumes vegetative land in excluded squares is similar to sampled squares, a assumption generally unlikely to be problematic because the excluded area is small, but problematic in regions with high sea/urban proportions.
- Official GB estimates are produced using ratio estimates for each land class, weighted by the vegetative land area within each class. Since 1998, bootstrap methods (Efron & Tibshirani) are used to estimate standard errors and confidence intervals due to concerns about skewness.
- References for sampling design and methods:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap