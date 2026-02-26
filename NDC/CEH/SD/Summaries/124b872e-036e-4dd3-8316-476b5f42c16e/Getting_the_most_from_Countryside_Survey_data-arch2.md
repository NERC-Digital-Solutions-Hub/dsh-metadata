# Notes on the downloadable data

- To preserve representativeness of the wider countryside, the precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH. External users cannot identify square locations with precision better than 100 square km.
- As a result, it is not possible to determine whether any survey squares fall within defined areas below this threshold.

## Sampling Considerations in the use of Countryside Survey Data

- CS field survey data come from a sample of 1 km squares in Great Britain. Each selected square is mapped and detailed measurements are made of features within the square, including quadrats for vegetation, soils, etc. There are two levels of sampling: whole square and within-square; measurements cover both levels (binary and continuous variables).
- The CS sample squares are not a random subset of all GB squares. The design is stratified, with sub-samples selected within designated strata defined by the ITE Land Classification. The classification has evolved:
  - Originally 32 Land Classes
  - 1998: revised to 42 classes for Scotland reporting
  - 2007: revision for Wales reporting, resulting in 45 classes
  - Thus England, Wales, and Scotland effectively have country-specific classifications (England 21, Wales 8, Scotland 16).
- Estimates derived from CS data without accounting for stratification may not be representative and can misstate variation. In practice, estimates for GB or regions are made under the assumption that vegetative land in excluded squares is similar to that in sampled squares; bias is expected to be small since the excluded area is typically small, unless a region has a high proportion of sea or urban squares.
- Exclusion criteria: Squares with area more than 90% sea or more than 75% urban (as measured from 1:250,000 OS maps) were excluded from field survey. Official GB estimates use ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area in each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness in some features.
- Practical implications for analysts:
  - When analysing CS data, account for the stratified design and apply appropriate weights by land class and vegetative area.
  - Use bootstrap-based SEs and CIs rather than assuming simple random sampling, especially for skewed features.
  - Be mindful of regional reporting differences and the non-random nature of square selection when aggregating to GB or regional levels.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.