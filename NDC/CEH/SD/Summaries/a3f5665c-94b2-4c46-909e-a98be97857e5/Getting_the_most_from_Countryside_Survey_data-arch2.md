# Notes on the downloadable data

- Purpose: Describes how Countryside Survey (CS) field data are collected, sampled, and processed, and how this affects analysis and interpretation for users of downloadable data.
- Data confidentiality: To preserve representativeness, the precise locations of CS survey squares are kept confidential by CEH. External users cannot identify squares with precision better than 100 square kilometres, limiting exact geographic pinpointing.

## Sampling design and data structure

- Data scope: CS field survey data come from a sample of 1 km squares across Great Britain (GB). Each selected square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Data types: Measurements range from binary (yes/no) to continuous (areas, lengths), across multiple features.
- Non-random, stratified sampling: The sample is not a random subset of GB squares. It is stratified by land classification (ITE Land Classification). Country-specific revisions exist:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Classification changes over time: The land-class scheme has evolved (32 classes originally; 1998 updated to 42 for Scotland; 2007 further changes for Wales), resulting in country-specific classifications.
- Coverage exclusions: Squares with more than 90% sea or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field surveys. Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares.
- Representativeness caveat: Estimates for GB or regions assume similarity between included and excluded squares; bias is generally negligible unless a region contains a high proportion of sea or urban squares.

## Estimation and analysis approach

- Estimation method: Official estimates are produced as ratio estimates (per Cochran, 1963) for each land class, accounting for the vegetative land area within each sampled square.
- Weighting: Land-class estimates are combined using weights corresponding to the vegetative land area of each land class across GB.
- Uncertainty quantification: Because of skewness in some features, standard errors and confidence intervals have been estimated using bootstrap methods since 1998 (Efron and Tibshirani, 1993).

## Data accessibility and implications for use

- Data handling: The document outlines how data are sampled, processed, and weighted, informing how to prepare and interpret outputs (maps, charts, reports) and how to store/upload datasets to appropriate portals.
- Privacy vs. utility: The confidentiality of square locations constrains precise geographic analyses at fine scales; users must work with the coarser location information (up to ~100 sq km precision) and the stratified, weighted framework described.

## References (for methodological context)

- Barr, C.J. et al. Countryside Survey 1990 Main Report (1993)
- Cochran, W.G. Sampling Techniques (1963)
- Efron, B. & Tibshirani, R.J. An Introduction to the Bootstrap (1993)