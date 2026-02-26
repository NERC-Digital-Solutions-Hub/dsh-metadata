# Notes on the downloadable data

- Confidentiality of precise locations: UKCEH holds exact survey-square locations to preserve representativeness; external users cannot identify square locations with precision finer than 100 square km.
- Implication for map-based data: spatial precision is intentionally coarse, affecting the ability to determine whether specific survey squares fall within defined areas below the 100 sq km threshold.

## Sampling and data structure

- Countryside Survey (CS) field data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped, with measurements at two levels: the whole square and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Measurements vary (binary to continuous); some describe the square as a whole, others describe inner features.
- The CS sample is not a random subset; it is stratified by the ITE Land Classification. Stratification has evolved:
  - Original 32 classes
  - 1998: expanded to 42 classes (Scotland reporting)
  - 2007: 45 classes (Wales reporting)
  - Today: England 21 classes, Wales 8, Scotland 16
- Estimates drawn from CS data are sensitive to stratification; analyses that ignore stratification may yield biased results.

## Coverage and representativeness

- Not all GB squares were surveyed: squares with more than 90% sea or more than 75% urban area were excluded from field survey.
- Official estimates assume vegetative land in excluded squares is similar in composition to sampled squares; this assumption is generally reasonable because the excluded area is small, but regional biases can occur in areas with high sea/urban proportions.

## Estimation methods

- Estimates are produced by ratio estimation (Cochran) for each land class, weighting by the vegetative land area within each class.
- From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani) to address skewness in some features.
- When using CS data for GB or regional analyses, account for stratification, weighting, and the potential bias from excluded squares.

## Practical implications for GIS work

- Map products should reflect the coarse locational precision (no exact pinpointing of survey squares).
- Analyses should incorporate stratification, weighting by vegetative area, and bootstrap-derived uncertainty.
- Be cautious about analyses that assume random sampling or that generalize from unstratified samples.
- Consider the possibility of bias where excluded squares (sea/urban) are geographically concentrated.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.