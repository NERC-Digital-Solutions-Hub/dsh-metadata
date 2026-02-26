# Notes on the downloadable data

## Data characteristics
- Countryside Survey (CS) field survey data come from a sample of 1 km squares in Great Britain.
- Each selected square is mapped and measured at two levels: the whole square and features within the square.
- Measurements include a range of variable types, from binary (yes/no) to continuous (areas, lengths).

## Sampling considerations
- The CS sample squares are not a random subset; they are stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16).
- Some squares are excluded from field survey: squares whose area is more than 90% sea or more than 75% urban.
- Consequently, official estimates are representative only of GB squares meeting the survey criteria. Estimates for GB or regions are derived under the assumption that vegetative land in excluded squares is similar to sampled squares; this bias is generally small unless a region has a high proportion of sea or urban squares.
- Estimation approach: ratio estimates are calculated for each land class, weighting by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated using the bootstrap due to skewness in some features.

## Estimation and inference
- Land class estimates are produced using ratio estimation with area-based weights.
- Bootstrapping is used to derive standard errors and confidence intervals, reflecting skewness in some measurements.

## Access, privacy, and caveats
- To preserve representativeness, the precise locations of CS survey squares are confidential; external users cannot identify survey squares with precision finer than 100 square kilometers.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.