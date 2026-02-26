# Notes on the downloadable data

- The precise locations of Countryside Survey squares are kept confidential by UKCEH to preserve representativeness; external users cannot identify whether survey squares fall within defined areas with precision finer than 100 square km.

- Consequently, users cannot map exact square-level positions for analyses requiring finer spatial detail.

# Sampling Considerations in the use of Countryside Survey Data

- Countryside Survey field data come from a sample of 1-km squares across Great Britain, with measurements at two levels: whole squares and within-square features (binary and continuous variables).

- The CS sample is not a random subset of GB 1-km squares; it is stratified by the ITE Land Classification. Land classifications have evolved:
  - 32 classes originally
  - 42 classes in 1998 (Scotland reporting)
  - 45 classes in 2007 (Wales reporting)
  - Therefore, England: 21 classes; Wales: 8; Scotland: 16
  - Estimates must account for stratification; unstratified estimates may be biased or have incorrect variation.

- Not all 1-km squares were surveyed. Excluded squares are those with more than 90% sea area or more than 75% urban area (as defined at 1:250,000 OS map scale). Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; bias is generally small unless a region has substantial sea/urban coverage.

- Official estimates are produced as ratio estimates for each land class, weighting by the vegetative land area within each class. Since some features can be skewed, standard errors and confidence intervals have been estimated using bootstrap methods since 1998 (Efron and Tibshirani).

- References for methodology and sampling design:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap