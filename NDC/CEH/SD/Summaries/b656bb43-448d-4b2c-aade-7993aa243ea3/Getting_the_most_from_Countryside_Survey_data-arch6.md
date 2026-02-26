# Notes on the downloadable data

- The precise locations of CS survey squares are kept confidential by CEH to preserve representativeness of the wider countryside.
- External users cannot identify survey squares with precision better than 100 square km.

## Sampling Considerations in the use of Countryside Survey Data

- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in GB; each square is mapped and measurements are taken at two levels: for the square as a whole and for features within the square.
- Measurements are varied, including binary and continuous variables (e.g., areas, lengths).
- The CS sample squares are not a random subset of all GB squares; it is a stratified sample with sub-samples selected within designated strata.
- Strata for square selection are defined by the ITE Land Classification. The classification has evolved:
  - Originally 32 land classes
  - 1998: expanded to 42 classes for Scotland reporting
  - 2007: expanded to 45 classes for Wales reporting
  - In effect, each country now has its own classification (England 21, Wales 8, Scotland 16).
- Estimates that do not account for stratification may be unrepresentative and have inaccurate variation estimates.
- Some squares were excluded from field survey based on size criteria from 1:250,000 OS maps:
  - Excluded if more than 90% sea or more than 75% urban.
- Consequently, field survey data are representative of the included squares; extrapolation to all GB squares assumes similarity of vegetative land in excluded squares, which is generally reasonable but may be problematic in regions with many sea/urban squares.
- Official GB estimates are produced by ratio Estimation (Cochran, 1963) for each land class, weighting by the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals have been estimated using the bootstrap method (Efron & Tibshirani, 1993) to address skewness in some features.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.