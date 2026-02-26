# Notes on the downloadable data

## Document scope and data confidentiality
- Describes how Countryside Survey (CS) field data are prepared, including representativeness considerations and data handling for GIS use.
- Exact locations of CS survey squares are kept confidential by CEH and cannot be identified to external users with precision better than 100 square kilometres.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares in Great Britain.
- Each selected square is mapped and measured at two levels: the whole square and within-square features (e.g., quadrats for vegetation, soils).
- Measurements are varied types, from binary (yes/no) to continuous (areas, lengths).
- Sampling is not a random subset; it is stratified by the ITE Land Classification.
- Country-specific land classifications differ: England has 21 classes, Wales 8, Scotland 16.

## Exclusions and representativeness
- Squares are excluded if their area is more than 90% sea or more than 75% urban (based on 1:250,000 OS maps).
- Official estimates for GB and regions assume that vegetative land in excluded squares is similar to sampled squares; bias is deemed negligible except in regions with a high proportion of sea or urban squares.

## Estimation and uncertainty
- Estimates by land class are produced using ratio estimates that weight by the area of vegetative land in each class.
- Land-class estimates are combined using weights equal to the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness.

## Practical implications for GIS
- Do not assume precise point-level accuracy; data are represented at the level of aggregated squares with a confidentiality constraint.
- When mapping or aggregating, apply the stratified ratio-estimation weights based on vegetative land area.
- Be aware of potential regional bias due to excluded squares (sea/urban areas) and the non-random sampling design.
- Use bootstrap-derived uncertainty measures (standard errors, confidence intervals) when assessing variability in estimates.
- Ensure analyses align with the country-specific land classifications for comparability.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.