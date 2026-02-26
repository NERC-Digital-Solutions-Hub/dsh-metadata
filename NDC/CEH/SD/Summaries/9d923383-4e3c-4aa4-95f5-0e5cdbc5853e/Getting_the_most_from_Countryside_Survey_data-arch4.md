# Notes on the downloadable data

## Key points
- To preserve representativeness, precise CS survey square locations are confidential; external users cannot identify squares with precision better than 100 square km.
- Countryside Survey (CS) field survey data come from a sample of 1 km squares in GB, with measurements at two levels: whole square and within-square; data include both binary and continuous variables.
- Squares are not a random subset; the sample is stratified by the ITE Land Classification, with country-specific revisions (England 21 classes, Wales 8, Scotland 16). The classification has evolved from 32 to 42 (1998) and 45 (2007).
- Some squares are excluded from field survey: those >90% sea or >75% urban. Estimates for GB/regions assume excluded squares are similar to sampled ones, a bias likely negligible unless a region has many sea/urban squares.
- Official estimates are produced using ratio estimates by land class, weighted by the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap to address skewness in features being estimated.

## Sampling considerations
- The sampling design requires accounting for stratification when interpreting estimates; ignoring stratification can lead to non-representative results and incorrect variation.
- Extrapolations to whole GB or regions rely on the assumption that vegetative land composition in excluded squares mirrors that in sampled squares; bias is possible if this fails.
- Data users should apply appropriate weighting by land-class area and consider bootstrap-based uncertainty measures for robust inferences.

## Practical implications for data leaders
- Ensure metadata clearly documents the stratified sampling design, exclusions, and bootstrap methods for uncertainty.
- Communicate limitations around representativeness and potential biases when applying GB/regional estimates.
- Use proper weighting and consider region-specific applicability given changes in land-class classifications across countries.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.