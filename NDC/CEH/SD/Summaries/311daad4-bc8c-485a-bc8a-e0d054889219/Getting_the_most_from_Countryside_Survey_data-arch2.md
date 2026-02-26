# Notes on the downloadable data

## Confidentiality of survey locations
- To preserve representativeness of the wider countryside, the precise locations of Countryside Survey (CS) field squares are held in confidence by CEH.
- External users will not be able to identify square locations with precision better than 100 square kilometres.

## Sampling framework and data collection
- CS field survey data come from a sample of 1 km squares in Great Britain; measurements are taken at two levels: the whole square and within-square features (e.g., quadrats for vegetation, soils, etc.), yielding binary and continuous variables.
- The sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification.
  - Country-specific classifications: England (21 classes), Wales (8 classes), Scotland (16 classes).
  - The land classification system has evolved (32 classes originally; restructured to 42 in 1998 for separate Scotland reporting; further revision leading to 45 classes with Wales reporting).
- Some squares were excluded from field survey:
  - Exclusion criterion: area of sea > 90% or urban area > 75% (based on 1:250,000 OS maps).
  - Estimates for GB (or regions) assume excluded squares have similar vegetative land composition to sampled squares; bias is typically negligible unless a region has a high proportion of sea or urban squares.

## Estimation methods and weighting
- Official GB land-class estimates are produced using ratio estimates (Cochran, 1963) for each land class.
- Weights are based on the area of vegetative land in each land class; estimates across classes are combined using these vegetative-land-area weights.

## Uncertainty and statistical treatment
- From 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness in some estimated features.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.