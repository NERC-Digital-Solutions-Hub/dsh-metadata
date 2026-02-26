# Notes on the downloadable data

- Purpose and confidentiality
  - Aimed at preserving representativeness of the wider countryside.
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users will not be given location precision finer than 100 square km.

- Data structure and sampling
  - Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain.
  - Each selected square is mapped and contains detailed measurements within the square (e.g., quadrats for vegetation, soils).
  - Two sampling levels: measurements characterize the whole square and measurements describe features within the square.
  - Measurements include binary and continuous variables (e.g., areas, lengths).

- Sampling design and stratification
  - Squares are not a random subset; the sample is stratified with sub-samples within designated strata.
  - Stratification is defined by the ITE Land Classification.
  - Land classification changes over time:
    - Original: 32 classes
    - 1998: expanded to 42 classes (Scotland reporting)
    - 2007: expanded to 45 classes (Wales reporting)
  - Country-specific classifications:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes

- Representativeness and exclusions
  - Some GB squares were not considered for field survey.
  - Excluded if over 90% sea or over 75% urban (based on 1:250,000 OS maps).
  - Estimates for GB or regions assume excluded land has similar vegetative composition to sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.

- Estimation, weighting, and uncertainty
  - Official GB estimates use ratio estimation for each land class, weighted by the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.