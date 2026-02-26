# Notes on the downloadable data

- Purpose and scope
  - Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with two sampling levels: whole squares and within-square measurements.
  - Measurements include diverse data types, from binary yes/no to continuous values like areas or lengths, collected via mapped squares and quadrats.

- Confidentiality and data privacy
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users cannot identify square locations with precision finer than 100 square kilometres.

- Sampling design and implications
  - The CS sample is not a random subset; it is stratified by the ITE Land Classification.
  - Land classifications have evolved: 32 classes originally, 42 (1998) for Scotland, 45 (2007) for Wales, resulting in country-specific classifications (England: 21, Wales: 8, Scotland: 16).
  - Analyses must account for stratification to avoid biased estimates and mischaracterised variation.

- Exclusions and representativeness
  - Squares with >90% sea or >75% urban area were excluded from field surveys.
  - Official estimates assume similarity between vegetative land in excluded squares and sampled squares; bias is generally small unless a region has substantial sea/urban square coverage.

- Estimation methods
  - Estimates are produced using ratio estimates by land class, weighted by the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani).

- Data usage considerations
  - Analysts should incorporate stratification and weights when estimating regional or national figures.
  - Be mindful of potential biases if extrapolating beyond the sampled, stratified framework, and when dealing with regions with high proportions of excluded squares.

- References for methodology
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Cochran (1963): Sampling Techniques
  - Efron & Tibshirani (1993): An Introduction to the Bootstrap