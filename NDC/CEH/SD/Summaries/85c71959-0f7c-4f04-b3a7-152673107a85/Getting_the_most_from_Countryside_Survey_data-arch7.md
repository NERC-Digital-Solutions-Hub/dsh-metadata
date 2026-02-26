# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field sample squares are kept confidential by CEH to preserve representativeness, with a precision limit of 100 square km for external users.
- It is not possible to identify whether survey squares fall within defined areas below this threshold.

## Sampling and data structure

- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and measured at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.).
- Measurements are of varied types (binary, continuous), taken at both levels to characterize the square and its internal features.

## Confidentiality and precision

- Location precision is intentionally limited; external users cannot pinpoint exact square locations beyond the 100 square km threshold.

## Sampling design and representativeness

- The CS sample squares are not a random subset of all GB squares; the sampling is stratified within designated strata.
- Stratification is defined by the ITE Land Classification. Classification details have evolved:
  - Original: 32 land classes
  - 1998: 42 classes (Scotland reporting) 
  - 2007: 45 classes (Wales reporting)
  - Consequently, each country has its own classification (England, Wales, Scotland with different class counts).
- Estimates that do not account for stratification may be unrepresentative and have inaccurate variation estimates.

## Exclusions and potential bias

- Squares excluded from field survey if their area (from 1:250,000 OS maps) is more than 90% sea or more than 75% urban.
- Official GB estimates are derived by ratio estimates within land classes, weighted by the vegetative land area in each class.
- In practice, GB or regional estimates assume similarity in vegetative land composition between included and excluded squares; bias is generally small, except where a region contains a high proportion of sea/urban squares.

## Estimation method and uncertainty

- Land class estimates use ratio estimates (Cochran, 1963), weighted by vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.

## Practical considerations for GIS work

- When creating map-based products or analyses:
  - Incorporate the stratified sampling design and related weights.
  - Use bootstrap-derived uncertainty measures where possible.
  - Be cautious about extrapolating results to areas with high proportions of excluded squares (sea/urban) or beyond the sampled squares.
  - Recognize country-specific land classification differences when comparing England, Wales, and Scotland.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.