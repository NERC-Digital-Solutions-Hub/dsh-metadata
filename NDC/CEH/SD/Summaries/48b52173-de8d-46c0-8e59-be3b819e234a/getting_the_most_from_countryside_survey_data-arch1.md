# Notes on the downloadable data

- Confidential locations: The precise locations of Countryside Survey (CS) squares are kept confidential by UKCEH to preserve representativeness. External users cannot identify whether squares fall within defined areas below 100 square km.

- Field survey design: CS field data come from a sample of 1 km squares in Great Britain. Each square is mapped and measured at two levels—square-level and within-square measurements—covering a range of binary and continuous variables (e.g., vegetation, soils).

- Sampling design: The CS sample squares are not a random subset of all GB squares; it is a stratified sample defined by the ITE Land Classification. Country-specific classifications exist (England 21 classes, Wales 8, Scotland 16). Classifications have evolved (32 → 42 → 45 classes) due to separate country reporting. Analyses must account for stratification to avoid biased estimates and incorrect variation estimates.

- Exclusions and representativeness: Squares with more than 90% sea area or more than 75% urban area were excluded from field survey. Official estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is typically negligible unless a region has a high proportion of sea or urban land.

- Estimation method: Official estimates are produced using ratio estimates by land class, weighting by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated via bootstrap due to skewness in some features.

- Practical implications for analysts: When using CS data, respect the stratified design and weighting by vegetative land area; be mindful of location confidentiality and the implications of excluding certain squares; the bootstrap approach should be used for uncertainty estimation.

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.