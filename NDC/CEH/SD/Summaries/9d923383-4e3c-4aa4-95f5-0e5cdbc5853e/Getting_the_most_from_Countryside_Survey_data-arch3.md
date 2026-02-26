# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are confidential to preserve representativeness. External users cannot identify square locations with precision better than 100 square kilometers.

## Sampling considerations

- CS Field Survey data come from a sample of 1 km squares across Great Britain, with two levels of measurement: 
  - Whole square (mapped, broader characteristics)
  - Within-square (detailed measurements such as quadrats for vegetation, soils, etc.)
- The sampling is not a random subset; it is stratified by the ITE Land Classification. Classifications have evolved from 32 to 42, and then to 45 classes across the different countries:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Estimates that do not account for stratification may be unrepresentative; weighting is based on the area of vegetative land within each land class.
- Some squares were excluded from field survey:
  - More than 90% sea
  - More than 75% urban (as per 1:250,000 OS maps)
  - Excluded squares are assumed to be similar in vegetative land composition to included squares; bias is generally small, except in regions with a high share of sea or urban area.
- Estimation approach:
  - Official estimates are produced using ratio estimates (Cochran, 1963) for each land class, with weights derived from the vegetative land area of each class.
- Uncertainty and inference:
  - From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness in some features.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.