# Notes on the downloadable data

- To preserve representativeness of the wider countryside, exact locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
- External users cannot identify whether survey squares fall within defined areas with precision finer than 100 square km.

## Sampling considerations in the Countryside Survey Data

- CS field survey data come from a sample of 1 km squares in GB, with measurements at two levels: the entire square and features within the square.
- Measurements vary in type, from binary to continuous (e.g., areas, lengths).
- The CS sample is not a random subset of all GB squares; it is stratified by designated strata defined by the ITE Land Classification.
- Land Classification details have changed over time:
  - Originally 32 classes
  - 1998: expanded to 42 classes for Scotland reporting
  - 2007: expanded to 45 classes to accommodate Wales reporting
  - Each country effectively has its own classification (England: 21 classes, Wales: 8, Scotland: 16)
- Estimates based on CS data must account for stratification; ignoring it leads to non-representative estimates and incorrect variation estimates.
- Not all GB squares were surveyed:
  - Squares with >90% sea or >75% urban area were excluded from field survey.
  - Official GB or regional estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is generally negligible except when a region has a high proportion of sea/urban squares.
- Estimation approach:
  - Uses ratio estimates for each land class, weighting by vegetative land area within each class.
  - Land-class estimates are then combined using the total vegetative land area as weights.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features (Efron & Tibshirani, 1993).

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.