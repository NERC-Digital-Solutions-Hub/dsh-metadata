# Notes on the downloadable data

- Overview of confidentiality: precise locations of Countryside Survey (CS) squares are kept confidential by CEH; external users cannot identify squares with precision finer than 100 square km, limiting ability to determine whether squares fall within specific areas.

- Data structure and measurements: CS field survey data come from a sample of 1 km squares in Great Britain; each selected square is mapped and measured at two levels (the square as a whole and within-square features); measurements include both binary and continuous variables (e.g., areas, lengths).

- Sampling design and stratification: the sample is not a random subset but a stratified sample based on the ITE Land Classification; classifications have evolved by country (England, Wales, Scotland) with country-specific numbers of classes (England 21, Wales 8, Scotland 16) and revisions over time (32 → 42 → 45 classes). Analyses should account for stratification to avoid biased estimates.

- Exclusions and representativeness: some GB squares were excluded from field survey if their area was more than 90% sea or more than 75% urban (based on 1:250,000 OS maps). Consequently, CS field data are strictly representative of the included squares; GB-wide estimates assume excluded squares have similar vegetative land composition, which may introduce bias if a region contains many sea/urban squares, though such bias is likely small overall.

- Estimation and uncertainty: official estimates are produced by ratio estimation within land classes, weighting by vegetative land area in each class; since 1998, standard errors and confidence intervals have been estimated using bootstrap methods to address skewness.

- References for methodology: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.