# Notes on the downloadable data

- Confidentiality of locations: precise locations of Countryside Survey (CS) field squares are kept confidential by CEH to preserve representativeness; external users will not have precision better than 100 square km, preventing identification of whether squares fall within defined areas.

- CS data structure: field survey data come from a sample of 1 km squares across GB; each square is mapped and measurements are taken at two levels—across the square and within the square (multiple measurement types from binary to continuous).

- Sampling design: squares are not a random subset; the design is stratified by the ITE Land Classification, with country-specific revisions over time (32 classes originally; 42 in 1998; 45 in 2007; England 21, Wales 8, Scotland 16).

- Representativeness and analysis: estimates that do not account for stratification may be unrepresentative and misstate variation.

- Excluded squares and applicability: squares with more than 90% sea area or more than 75% urban area were excluded from field surveys; GB estimates assume vegetative land in excluded squares is similar to sampled squares; this introduces little bias except in regions with high sea/urban proportions.

- Estimation approach: official GB estimates are produced using ratio estimates for each land class, weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated with bootstrap methods due to skewness in some features.

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap. 

- Implications for data use: users should consider the stratified design, confidentiality constraints, and bootstrap-based uncertainty when interpreting CS estimates.