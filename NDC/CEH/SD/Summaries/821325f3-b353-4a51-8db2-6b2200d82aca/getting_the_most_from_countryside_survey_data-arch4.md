# Notes on the downloadable data

- Location confidentiality: precise Countryside Survey square locations are kept by UKCEH and not disclosed beyond 100 square km precision to external users.
- Implication for use: users cannot determine whether survey squares fall within defined areas smaller than the 100 sq km threshold.

## Sampling Considerations in the use of Countryside Survey Data

- Data structure: CS field data come from a sample of 1-km squares in Great Britain, with two sampling levels—whole squares and within-square measurements (binary and continuous variables).
- Non-random, stratified design: The sample is not a random subset; it is stratified by land classification (ITE Land Classification), with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16; totals adjusted over time to 32, 42, and 45 classes respectively across editions). Incorrectly ignoring stratification can lead to non-representative estimates and misestimated variation.
- Exclusions and representativeness: Squares with more than 90% sea or more than 75% urban area were excluded from survey. Estimates are considered representative only for GB squares meeting criteria; across GB, it is assumed excluded areas are similar to sampled areas for vegetative land (bias is generally small unless a region has a high proportion of sea/urban squares).
- Estimation approach: Official estimates are produced as ratio estimates by land class, weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are derived via bootstrap methods.
- References for methodology: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.