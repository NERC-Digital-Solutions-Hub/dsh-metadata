# Notes on the downloadable data

- Location confidentiality: The precise locations of Countryside Survey (CS) field squares are withheld to preserve representativeness; external users cannot identify square locations with precision better than 100 square km.
- Data coverage and structure: CS field survey data sample 1 km squares across GB; each square is mapped and measurements are taken at two levels—across the whole square and within-square features (e.g., quadrats for vegetation and soils); measurements include binary and continuous variables.
- Representativeness and stratification: The squares are not a random subset but a stratified sample defined by the ITE Land Classification. Country-specific classifications exist (England, Wales, Scotland) and have evolved from 32 to 42 to 45 classes over time. Estimates not accounting for stratification may be non-representative; variation estimates depend on the stratified design.
- Exclusions and potential bias: Squares with more than 90% sea or more than 75% urban area were excluded from field survey. Official GB estimates assume excluded areas are similar to included areas; bias is typically negligible unless a region has a high proportion of sea/urban land.
- Estimation approach: Official estimates are produced using ratio estimators by land class, weighted by vegetative land area in each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features.
- Documentation and references: Key methodological references include Barr et al. (1993) for the CS 1990 Main Report, Cochran (1963) on sampling techniques, and Efron & Tibshirani (1993) on the bootstrap.

## Sampling Considerations in the use of Countryside Survey Data

- Sampling design and data levels: CS data come from a two-level sampling framework (whole 1 km squares and within-square measurements) with mapping and detailed measurements across selected squares.
- Land Classification and country differences: The Land Classification used for stratification has changed across time and by country (England, Wales, Scotland) leading to country-specific classifications; analyses should incorporate stratification to avoid biased inferences.
- Representativeness and regional bias: Exclusion criteria and non-random sampling mean estimates are most valid when analyses respect the stratified design; extrapolations to larger regions should be treated cautiously if regional composition deviates from the sampled squares.
- Estimation and uncertainty: Ratio-estimator based estimates by land class with weights by vegetative land; bootstrap-based standard errors and confidence intervals are used due to skewness concerns.
- Foundational references: Barr et al. (1993); Cochran (1963); Efron & Tibshirani (1993).