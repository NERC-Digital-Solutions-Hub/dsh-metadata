# Notes on the downloadable data

- Purpose and confidentiality
  - Precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
  - External users cannot identify square locations with precision finer than 100 square km.
  - This constraint preserves representativeness but limits fine-grained geographic pinpointing.

- Data scope and structure
  - CS field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Each square is mapped and measured at two levels: the whole square and features within the square.
  - Measurements vary from binary (yes/no) to continuous (areas, lengths).

- Sampling design
  - The square sample is not random; it is stratified by the ITE Land Classification.
  - Land Class classifications have evolved:
    - Originally 32 classes
    - 1998: 42 classes (Scotland reporting requirements)
    - 2007: 45 classes (Wales reporting)
  - Each country uses its own classification (England 21, Wales 8, Scotland 16).
  - Analyses that ignore stratification may be non-representative and have biased variation estimates.

- Exclusions and extrapolation
  - Squares with >90% sea area or >75% urban area were excluded from field surveys.
  - Official GB estimates assume excluded vegetative land is similar to sampled squares; bias is generally small unless a region has a high proportion of sea/urban squares.

- Estimation and uncertainty
  - Estimates are calculated as ratio estimates by land class, weighted by the vegetative land area within each class.
  - Weights are applied to combine land-class estimates across GB.
  - Since 1998, standard errors and confidence intervals are estimated via bootstrap due to skewness concerns.

- Implications for users and analysis
  - Must account for stratification, weighting, and the restricted location precision when analyzing and interpreting results.
  - Extrapolations to unsampled or excluded areas should be treated with caution.
  - Documentation should include land-class definitions, area weights, and bootstrap-based uncertainty measures.

- References
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap