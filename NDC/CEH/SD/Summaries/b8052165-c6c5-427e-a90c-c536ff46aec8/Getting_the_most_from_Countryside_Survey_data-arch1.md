# Notes on the downloadable data

- Confidentiality of locations: The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH. External users cannot identify squares with greater precision than 100 square km.
- Implication: You cannot determine whether a survey square falls within defined areas below this threshold.

## Sampling design and data structure

- Data collection: CS field survey uses a sample of 1 km squares across GB. Within each selected square, measurements are taken at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.).
- Data types: Measurements include binary (yes/no) and continuous variables (areas, lengths, etc.).

## Non-random, stratified sampling

- The sample is not a random subset of all GB squares; it is stratified by land classification.
- Land Classification structure:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- History of classifications: 32 classes originally; expanded to 42 in 1998 for Scotland; further changes to 45 classes for Wales. Each country effectively has its own classification.

## Representativeness and exclusions

- Representativeness caveat: Official estimates for GB or regions assume vegetative land in excluded squares (based on OS maps) is similar to sampled squares. Excluded squares are those >90% sea or >75% urban.
- Bias risk: Likely small unless a region has a high proportion of sea or urban squares; otherwise, estimates are considered broadly representative.

## Estimation method and uncertainty

- Estimation approach: Estimates by land class are derived using ratio estimation, weighted by the vegetative land area within each land class.
- Combining estimates: Land class estimates are combined using the area of vegetative land as weights.
- Uncertainty assessment: Since features can be skewed, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) from 1998 onward.

## Practical references

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.

## Considerations for analysts

- When analyzing CS data, incorporate stratification by country-specific land classes and appropriate weights by vegetative land area.
- Use bootstrap-generated standard errors and confidence intervals for skewed features.
- Account for the geographic confidentiality constraint and the implications of excluding highly sea/urban squares on regional estimates.
- Be aware that direct analyses that ignore stratification and exclusion rules may yield biased or non-representative results.