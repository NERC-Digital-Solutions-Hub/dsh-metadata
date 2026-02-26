# Notes on the downloadable data

- The precise locations of CS survey squares are confidential; external users will not be able to identify square locations with precision finer than 100 square kilometres.
- Consequently, it is not possible to determine whether any survey squares fall within defined areas below this threshold.

## Sampling design and implications

- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain (GB), with measurements at both whole-square and within-square levels (binary and continuous variables).
- The sample is not a random subset; it is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8 classes, Scotland: 16 classes).
- Some squares are excluded from field survey: those with more than 90% sea or more than 75% urban area (based on 1:250,000 OS maps).
- Estimates for GB or regions assume vegetative land in excluded squares is similar to sampled squares; this introduces potential bias, but is generally negligible unless a region has a high proportion of sea/urban squares.

## Estimation approach

- Official land-class estimates are produced using ratio estimates (Cochran, 1963), weighted by the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness concerns.

## Practical considerations for GIS work

- Data are map-oriented and reflect the sampling design; ensure stratification and area-based weights are considered when aggregating.
- Recognize two levels of measurement (square-level vs within-square-level features) when designing visuals or analyses.
- Be mindful of the confidentiality constraint on precise locations when publishing or sharing map products.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons, London.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.