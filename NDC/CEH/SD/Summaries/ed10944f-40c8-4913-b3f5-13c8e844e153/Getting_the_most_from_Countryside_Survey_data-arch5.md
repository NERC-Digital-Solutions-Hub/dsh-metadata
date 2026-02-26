# Notes on the downloadable data

- The exact locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot be provided with precise locations beyond 100 square km.
- CS field survey data cover 1 km square samples in Great Britain, with measurements at two levels: the whole square and within-square features. Data types range from binary to continuous.

## Data structure and content

- Sampling is not a random subset of GB squares; it is stratified by the ITE Land Classification, with country-specific classifications (England: 21, Wales: 8, Scotland: 16; revised across years).
- Within each square, multiple measurements are taken (e.g., quadrats for vegetation, soils, etc.).
- Some squares are excluded from field surveys based on land cover criteria: more than 90% sea or more than 75% urban.
- Estimates of vegetative land are produced by combining land-class estimates using weights based on vegetative land area.

## Sampling design and representativeness

- The design includes two levels of sampling (whole square and within-square) and is not a simple random sample of GB squares.
- Because classification and country reporting have evolved, estimates without accounting for stratification may be biased; proper analyses must incorporate the stratified design.

## Estimation and uncertainty

- Official estimates are derived using ratio estimation for each land class, weighted by the area of vegetative land in each class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani).

## Data processing and governance implications

- Because of confidentiality and sampling design, users should:
  - Acknowledge stratification and weighting in analyses.
  - Use bootstrap-based uncertainty estimates for confidence intervals.
  - Be mindful of potential biases due to excluded squares (sea/urban-dominated areas) and extrapolation assumptions.
- Metadata and provenance should document the sampling design, exclusion criteria, stratification, and weighting schemes to ensure reproducibility.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.