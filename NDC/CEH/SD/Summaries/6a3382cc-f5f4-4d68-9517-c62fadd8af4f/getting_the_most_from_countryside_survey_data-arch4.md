# Notes on the downloadable data

- Confidentiality of locations: precise positions of Countryside Survey squares are kept confidential by UKCEH; external users cannot identify squares with precision finer than 100 square km, limiting spatial identification for targeted areas.

- Sampling design and data structure: Countryside Survey field data come from a sample of 1-km squares in GB; two sampling levels exist (whole square and within-square) with measurements ranging from binary to continuous types; some features describe the square, others features within the square.

- Non-random, stratified sampling: the sampling is stratified by ITE Land Classification, with country-specific revisions over time (32 → 42 → 45 classes; England, Wales, Scotland have different class counts). Analyses must account for stratification to avoid non-representative estimates and incorrect variation.

- Excluded squares and representativeness: squares deemed more than 90% sea or more than 75% urban were excluded from field survey; official estimates assume excluded vegetative land is similar to sampled squares, which is usually reasonable because the excluded area is small, but regional problems may arise if a region has a high proportion of sea/urban squares.

- Estimation and uncertainty: official GB estimates are computed as ratio estimates by land class, weighted by the vegetative land area in each class. Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to skewness (Efron and Tibshirani, 1993).

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron and Tibshirani (1993) An Introduction to the Bootstrap.