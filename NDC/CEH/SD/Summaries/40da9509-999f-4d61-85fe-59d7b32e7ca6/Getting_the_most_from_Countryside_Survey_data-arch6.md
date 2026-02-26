# Notes on the downloadable data

- To preserve representativeness of the wider countryside, precise locations of CS survey squares are kept confidential by CEH and are not identifiable to external users with precision finer than 100 square km.
- Consequently, users cannot determine whether any survey squares fall within defined areas below this threshold.

## Data collection and sampling design

- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain.
- Each selected square is mapped and detailed measurements are taken at two levels: the whole square and within-square features.
- Measurements vary from binary to continuous (e.g., areas or lengths).
- The sample is not a random subset of all GB squares; it is stratified by designated strata defined by the ITE Land Classification. Country-specific classifications have evolved:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Estimates must account for stratification to avoid biased variation estimates.

## Representativeness and limitations

- Some squares are excluded from field survey: squares with >90% sea area or >75% urban area.
- Official estimates assume vegetative land in excluded squares is similar to sampled squares; bias is generally negligible, except where regions contain many sea/urban squares.
- The sampling design implies that simple, unweighted extrapolations may be misleading without considering stratification and area weights.

## Estimation methods and statistics

- Estimates by land class are produced using ratio estimation (Cochran, 1963), incorporating the vegetative land area of each sample square.
- Land-class estimates are combined using weights equal to the vegetative land area of each land class as a whole.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness concerns.

## Privacy and data accessibility

- Location precision is deliberately limited to protect representativeness and confidentiality.
- Users should not assume exact square locations or easy geographic pinpointing beyond the 100 square km threshold.

## Practical considerations for data users

- When using CS data, account for stratification and weighting; avoid analyses that assume simple random sampling.
- Use bootstrap-derived standard errors and confidence intervals for uncertainty assessment.
- Be cautious with regional extrapolations in areas with high proportions of sea or urban squares.
- Reference the methodological sources for sampling design and estimation techniques when reporting results:
  - Barr et al. (1993)
  - Cochran (1963)
  - Efron and Tibshirani (1993)

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.