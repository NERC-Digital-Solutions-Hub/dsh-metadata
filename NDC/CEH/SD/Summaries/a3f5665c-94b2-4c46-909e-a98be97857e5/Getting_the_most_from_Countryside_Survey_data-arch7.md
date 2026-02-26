# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision finer than 100 square km.
- Consequently, users cannot determine if any survey squares lie inside certain area boundaries below this 100 sq km threshold.

- CS field survey data come from a sample of 1 km squares in Great Britain (GB), with two levels of sampling:
  - Whole-square level
  - Within-square features (e.g., quadrats for vegetation, soils, etc.)
- Measurements vary in type from binary to continuous (areas, lengths), collected at both levels.

- The sampling design is not random; it is stratified by the ITE Land Classification. Country-specific classifications have evolved:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
  - Original 32 classes expanded to 42 (1998) and then 45 (2007) due to country reporting requirements
- Estimates based on the CS data must account for stratification; ignoring it yields non-representative estimates and biased variation.

- Not all GB squares were surveyed. Excluded squares are those with:
  - More than 90% sea area, or
  - More than 75% urban area (as measured at 1:250,000 OS map)
- Official estimates are representative only for included squares. In practice, GB-wide estimates assume vegetative land in excluded squares is similar to sampled squares; this bias is typically negligible except where a region has a high sea or urban proportion.

- Estimation approach:
  - Use ratio estimates (Cochran, 1963) for each land class, weighting by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness.

- References:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.