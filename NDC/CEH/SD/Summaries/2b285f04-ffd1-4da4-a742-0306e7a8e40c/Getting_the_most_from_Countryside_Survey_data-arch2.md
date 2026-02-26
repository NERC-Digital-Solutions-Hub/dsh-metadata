# Notes on the downloadable data

## Purpose and confidentiality
- To preserve representativeness of the wider countryside, precise locations of Countryside Survey (CS) squares are kept confidential by CEH.
- External users cannot identify whether survey squares fall within defined areas below 100 square km precision.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and detailed measurements are taken at two levels: the whole square and within-square features.
- Measurements vary in type (binary, continuous, etc.) and include vegetation, soils, etc.
- The sample is not random; it is stratified by the ITE Land Classification with country-specific classifications:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness concerns.

## Exclusion criteria
- Not all GB squares are considered for field survey.
- Excluded squares: more than 90% sea or more than 75% urban (as defined from 1:250,000 OS maps).
- Official GB estimates assume excluded squares are similar in vegetative land composition to sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.

## Estimation approach and weights
- Estimates are produced as ratio estimates (per Cochran, 1963) for each land class, incorporating the area of vegetative land in each sample square.
- Land class estimates are combined using weights equal to the vegetative land area of each land class as a whole.

## Uncertainty and analysis implications
- Stratification must be accounted for in analyses to avoid unrepresentative estimates.
- Standard errors and confidence intervals are derived via bootstrap methods (since 1998), addressing potential skewness in the data.

## Practical guidance for analysts
- When using CS data, ensure analyses reflect the stratified sampling design and weighting by vegetative land area.
- Be mindful of potential biases from excluded squares, particularly for regions with high sea or urban coverage.
- Rely on bootstrap-based uncertainty measures for standard errors and confidence intervals.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.