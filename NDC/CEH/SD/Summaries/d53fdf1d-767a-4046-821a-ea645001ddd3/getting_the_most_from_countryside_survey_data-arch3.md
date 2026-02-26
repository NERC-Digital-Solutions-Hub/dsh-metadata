# Notes on the downloadable data

- Purpose and confidentiality
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users cannot identify survey squares with precision finer than 100 square km.
  - Consequently, it is not possible to determine whether any survey squares fall within certain defined areas below this threshold.

- Sampling design and data structure
  - Countryside Survey (CS) field data come from a sample of 1-km squares in GB.
  - Each selected square is mapped and measured at two levels: the square as a whole and features within the square; measurements include binary and continuous variables.
  - The CS sample squares are not a random subset; they are stratified by the ITE Land Classification.
  - Land Classification:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
    - The classification has evolved (32 → 42 → 45 classes) due to country-specific reporting needs.
  - Representativeness caveat: analyses that do not account for stratification may be biased; estimates should weight by land-class area.
  - Exclusions: squares with area > 90% sea or > 75% urban (based on 1:250,000 OS maps) were not surveyed.
  - Practical implication: estimates for GB or regions are derived by assuming excluded squares have similar vegetative land composition to sampled squares; bias is generally small except in regions with high sea/urban proportions.

- Estimation methods and uncertainty
  - Official land-class estimates are produced using ratio estimates, weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals for some features are estimated using bootstrap methods to address skewness concerns.

- Implications for users
  - Analyses must consider stratification to obtain valid measures of variation.
  - Confidentiality and data governance constraints may affect data accessibility and sharing of underlying data.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.