# Notes on the downloadable data

## Confidentiality and data access
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
- External users cannot identify square locations with precision better than 100 square km.

## Sampling design and data structure
- CS field data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels: the whole square and within-square features.
- Measurements are varied (binary, continuous, areas, lengths).
- The sample is stratified by the ITE Land Classification, with country-specific classifications: England (21 classes), Wales (8), Scotland (16); overall 45 classes historically.
- The squares surveyed are not a random subset; estimates must account for stratification.
- Not all GB squares were surveyed; squares more than 90% sea or more than 75% urban were excluded.
- Official GB estimates use ratio estimation by land class, weighting by vegetative land area in each class.

## Representativeness and implications
- Analyses ignoring stratification and weighting may yield non-representative estimates and incorrect variation.
- Excluded squares (high sea/urban content) are assumed to be similar in vegetative land composition to sampled squares; bias is considered small except in regions with high proportions of sea or urban squares.

## Estimation methods and recommendations for use
- Use ratio estimates by land class, then combine across classes using vegetative land area as weights.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani).

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.