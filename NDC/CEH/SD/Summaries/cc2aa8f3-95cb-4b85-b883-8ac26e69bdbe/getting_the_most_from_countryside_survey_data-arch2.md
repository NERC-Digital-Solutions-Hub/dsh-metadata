# Notes on the downloadable data

## Context and purpose
- To preserve representativeness of the wider countryside, precise locations of Countryside Survey (CS) squares are kept confidential by UKCEH.
- External users cannot identify whether squares fall within defined areas below a threshold of 100 square km accuracy.
- CS field survey data come from a sample of 1 km squares in Great Britain, with measurements at both the square level and within-square features (binary and continuous variables).

## Sampling design and representativeness
- The sample is not a random subset of all GB squares; it is stratified within designated strata.
- Strata are defined by the ITE Land Classification. Country-specific updates have led to different classifications: England (21 classes), Wales (8), Scotland (16). The classification evolved from 32 to 45 classes to accommodate separate country reporting.
- Estimates that do not account for stratification may be unrepresentative and have biased variation estimates.
- Not all GB squares were surveyed. Squares with more than 90% sea area or more than 75% urban area were excluded from field survey.
- Official GB, regional, or country estimates assume vegetative land in excluded squares is similar to sampled squares; this assumption may introduce bias if regional composition differs markedly, though the un-surveyed land area is small.

## Estimation methods and uncertainty
- Estimates by land class are produced as ratio estimates (Cochran, 1963), incorporating the area of vegetative land in each sample square.
- Land class estimates are combined using weights equal to the vegetative land area of each land class overall.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness in some features.

## Practical implications for analysts
- When using CS data, apply the stratified design and appropriate weighting to obtain representative estimates.
- Be mindful of the exclusion of certain squares (sea/urban dominance) and the assumption that excluded land is similar to sampled land.
- Use bootstrap-based uncertainty measures for standard errors and confidence intervals, as recommended.
- Reference materials include Barr et al. (1993) for the CS 1990 main report, Cochran (1963) for sampling techniques, and Efron & Tibshirani (1993) for the bootstrap approach.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.