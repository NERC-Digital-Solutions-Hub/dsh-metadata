# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users are limited to identifying square locations no more precise than 100 square km; users cannot determine if squares fall within defined areas below this threshold.

## Sampling considerations in the use of Countryside Survey Data

- CS field survey data come from a sample of 1 km squares across Great Britain. Each selected square is mapped, with detailed measurements taken at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.), producing both binary and continuous variables.
- The sample is not a random subset of all GB squares; it is stratified, with sub-samples drawn within designated strata defined by the ITE Land Classification. Country-specific classifications exist: 21 land classes in England, 8 in Wales, and 16 in Scotland, resulting in an overall 45 classes when combined.
- Some squares were excluded from field survey: those where land area was more than 90% sea or more than 75% urban (per 1:250,000 OS maps). Official estimates assume vegetative land in excluded squares is similar to sampled squares; bias is considered negligible unless a region has a high proportion of sea/urban squares.
- Because of the sampling design, estimates for GB or regions are based on ratio estimates (Cochran, 1963) by land class, weighted by the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals for estimates have been computed using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.
- Practical implications for users: analyses must account for stratification and weighting; avoid treating the CS sample as a simple random sample; consider using bootstrap-based uncertainty where appropriate.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B., & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.