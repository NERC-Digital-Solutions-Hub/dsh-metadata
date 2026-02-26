# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users are limited to a precision of 100 square kilometers; you cannot identify whether any survey square falls within defined areas below this threshold.

## Sampling design and structure

- CS field survey data come from a sample of 1 km squares across GB. Each selected square is mapped and measured at both the square level and within-square level (e.g., quadrats for vegetation, soils, etc.). Measurements include binary and continuous variables.
- There are two levels of sampling: whole squares and within-square features, with different measurements characterizing each level.

## Non-random, stratified sampling

- The CS sample is not a random subset of all GB squares. It is stratified by the ITE Land Classification, with country-specific classifications (England 21 classes, Wales 8, Scotland 16). The classifications have evolved (32 → 42 in 1998, then 45 in 2007) to accommodate separate country reporting.
- Estimates derived from CS data must account for stratification; failing to do so yields non-representative estimates and incorrect variation estimates.

## Coverage limitations and extrapolation

- Not all GB squares were surveyed: any square >90% sea or >75% urban, by 1:250,000 OS map area, was excluded. Official GB or regional estimates assume excluded squares have similar vegetative land composition to sampled squares. This assumption may introduce bias, especially in regions with high sea/urban proportions, though overall bias is expected to be small.

## Estimation methods and uncertainty

- Land-class estimates are produced as ratio estimates (Cochran, 1963) using the vegetative land area in each sample square as weights.
- From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some estimations.

## Practical implications for analysts

- When using CS data, apply the stratification and weighting by vegetative land area to obtain representative estimates.
- Be aware that extrapolations to GB or regional scales rely on the similarity of excluded squares, which may not always hold.
- Use bootstrap-based standard errors and confidence intervals to assess uncertainty, especially for skewed features.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.