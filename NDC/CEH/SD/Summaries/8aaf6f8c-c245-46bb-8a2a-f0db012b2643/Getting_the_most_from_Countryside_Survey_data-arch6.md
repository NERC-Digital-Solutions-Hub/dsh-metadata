# Notes on the downloadable data

- Confidentiality: The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH; external users cannot be provided with precision better than 100 square km, so users cannot identify whether squares fall within defined areas below this threshold.

- Sampling design: CS field survey data come from a sample of 1 km squares in Great Britain. Each square is mapped with measurements at two levels (whole square and within-square). Measurements vary from binary to continuous. The sample is not a random subset; it is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16). Classifications evolved from 32 → 42 → 45 classes over time.

- Representativeness and analysis implications: Estimates derived from CS must account for stratification; failing to do so yields non-representative estimates and incorrect variation. Official estimates use ratio estimation for each land class, weighted by the vegetative land area within each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.

- Exclusions and generalisation: Not all GB squares were surveyed; squares with more than 90% sea area or more than 75% urban area were excluded. Official GB or regional estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is generally negligible unless a region has a high proportion of sea or urban squares.

- Estimation details: Land class estimates are computed as ratio estimates and then combined using weights based on the vegetative land area of each class. The bootstrap (Efron and Tibshirani) is used to derive standard errors and confidence intervals.

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.