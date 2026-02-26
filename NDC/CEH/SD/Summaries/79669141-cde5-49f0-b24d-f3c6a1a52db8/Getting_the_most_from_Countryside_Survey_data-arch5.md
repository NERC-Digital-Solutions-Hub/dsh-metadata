# Notes on the downloadable data

## Summary for Data Stewards
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot obtain precision better than 100 square km.
- CS data structure:
  - Field survey data come from a sample of 1 km squares across GB.
  - Measurements are taken at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils).
  - Data types range from binary to continuous.
- Sampling design and representativeness:
  - The set of sampled squares is not a random subset; it is stratified by the ITE Land Classification.
  - Land Classification classifications have evolved: 32 classes originally, then 42 (1998) for Scotland, and 45 (2007) to accommodate Wales reporting; England, Wales, and Scotland have country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16).
  - Estimates not accounting for stratification may be biased; official estimates are produced using ratio estimates by land class and area-weighted combinations.
- Exclusions and coverage:
  - Squares excluded from field survey if more than 90% sea area or more than 75% urban area (per 1:250,000 OS maps).
  - In practice, GB-wide estimates assume excluded squares have similar vegetative composition to sampled squares; potential bias is small except in regions with high sea/urban proportions.
- Inference and uncertainty:
  - Because of skewness in some features, standard errors and confidence intervals are estimated via bootstrap methods since 1998 (Efron and Tibshirani).
- Data handling and documentation:
  - Data are intended to be downloadable with accompanying metadata describing sampling design, stratification, exclusions, weighting, and bootstrap methodology.
  - Users should be guided by the documented limitations when performing region-wide or cross-country analyses.
- References for methodology:
  - Barr et al. (1993) Countryside Survey 1990 Main Report.
  - Cochran (1963) Sampling Techniques.
  - Efron and Tibshirani (1993) An Introduction to the Bootstrap.