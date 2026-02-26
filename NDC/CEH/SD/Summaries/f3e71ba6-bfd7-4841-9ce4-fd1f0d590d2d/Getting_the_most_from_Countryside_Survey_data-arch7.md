# Notes on the downloadable data

- Location confidentiality: Precise locations of CS survey squares are kept confidential by CEH; external users cannot identify whether squares fall within defined areas with precision better than 100 square kilometers. This prevents mapping exact survey-square positions at fine scales.

- Data scope and structure: Countryside Survey (CS) Field Survey data come from a sample of 1 km squares across Great Britain. Each selected square is mapped and measured at two levels: the square level (characterising the whole square) and within-square (describing features inside the square). Measurements include a range of variable types, from binary to continuous.

- Sampling design: The square sample is not random but stratified. Strata are defined by the ITE Land Classification, which has evolved by country (England, Wales, Scotland) into 21, 8, and 16 classes respectively. Consequently, estimates not accounting for stratification may be unrepresentative or have biased variation estimates.

- Exclusions and representativeness: Some squares were not surveyed because their area at 1:250,000 scale was more than 90% sea or more than 75% urban. Official GB estimates assume vegetative land in excluded squares is similar to that in sampled squares; this generally introduces negligible bias, except in regions with high sea/urban square proportions.

- Estimation and uncertainty: Estimates are produced using ratio estimation within land classes, weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated via bootstrap methods to address skewness in some features.

- Data preparation and usage: Users should be aware of the need to account for stratification and weighting when analyzing CS data. Combining data from different resolutions may require careful cleaning and transformation.

- Implications for GIS work: Map-based products should reflect the 100 sq km locational precision, stratified sampling structure, and the Bootstrap-derived uncertainties. Users should avoid inferring precise locations or making region-wide claims without accounting for the sampling design and potential biases from excluded squares.

- References for methodology: Barr et al. (1993) on the CS 1990 Main Report; Cochran (1963) on sampling techniques; Efron and Tibshirani (1993) on the bootstrap.

## Sampling Considerations in the use of Countryside Survey Data

- Sampling levels: Two levels of data collection—square-level and within-square measurements—enable characterisation of both overall square attributes and within-square features.

- Stratification details: Land Classification strata differ by country (England, Wales, Scotland) and have evolved over time, affecting representativeness and weighting in estimates.

- Survey coverage caveats: Not all GB squares were surveyed; the assumptions about vegetative land in excluded squares underpin nationwide estimates and may influence regional analyses.

- Practical GIS note: When creating maps, apply the appropriate stratified weights and acknowledge the confidentiality constraint that prevents precise plotting beyond the 100 sq km threshold.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.