# Notes on the downloadable data

- The precise locations of Countryside Survey squares are kept confidential by UKCEH and will not be identified to external users with precision better than 100 square kilometres. Consequently, users cannot determine whether squares fall within specific areas defined below this threshold.
- Countryside Survey (CS) field data come from a sample of 1-km squares in Great Britain (GB). Each selected square is mapped and measured both at the square level and within-square features (e.g., quadrats for vegetation, soils, etc.). Variables range from binary to continuous measurements.

## Sampling framework

- The CS sample squares are not a random subset of all GB 1-km squares; sampling is stratified within Land Classification strata defined by ITE.
- Two levels of sampling and measurement: the whole square and features within the square.
- Land Classification structure has evolved:
  - Original: 32 classes
  - 1998: 42 classes (Scotland reporting needs)
  - 2007: 45 classes (Wales reporting needs)
  - England: 21 classes; Wales: 8 classes; Scotland: 16 classes
- Estimates must account for this stratification; analyses ignoring stratification may be biased or have incorrect variation estimates.

## Representativeness and limitations

- Not all GB squares were surveyed; exclusions included squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps).
- Official estimates pertain to the GB squares that met inclusion criteria; estimates for GB or regions assume removed vegetative land is similar to sampled squares. This assumption is generally acceptable because the excluded land constitutes a small area, though bias could be problematic in regions with high sea/urban coverage.

## Estimation and uncertainty

- Land-class estimates are produced using ratio estimation, weighted by the vegetative land area within each land class.
- For all estimates, land-class results are combined using weights corresponding to the vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) to handle skewness in some features.

## Practical guidance for data usage

- When analyzing CS data, account for stratification by Land Classification to obtain representative estimates and correct variation measures.
- Be aware of the exclusions and the assumptions about excluded land when interpreting GB or regional estimates.
- Use the bootstrap-based standard errors and confidence intervals for robust uncertainty assessment.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.