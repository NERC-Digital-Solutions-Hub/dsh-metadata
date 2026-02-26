# Notes on the downloadable data

- Confidentiality of square locations: The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH. External users will not receive information with precision finer than 100 square km, so it is not possible to identify whether specific survey squares fall within defined areas below that threshold.

## Sampling design and representativeness

- CS field survey scope: Data come from a sample of 1 km squares in Great Britain (GB). Each selected square is mapped and measurements are taken at both the square level and within-square features (e.g., quadrats for vegetation, soils, etc.). Measurements vary from binary to continuous.
- Non-random, stratified sample: The sample is not a random subset of all GB squares; it is stratified by ITE Land Classification. Classification changes over time:
  - Originally 32 classes
  - 1998: expanded to 42 classes (Scotland reporting requirements)
  - 2007: expanded to 45 classes (Wales reporting requirements)
  - Result: England has 21 classes, Wales 8, Scotland 16; effectively country-specific classifications.
- Excluded squares: Squares where the area is >90% sea or >75% urban were excluded from field survey. Official estimates assume excluded squares are similar in vegetative land composition to sampled squares; bias is expected to be small except in regions with unusually high sea/urban coverage.
- Implications for analyses: Estimates based on CS data must account for stratification and the sampling design. Estimates that ignore stratification may be biased or have inaccurate variation estimates.

## Estimation and uncertainty

- Estimation method: Official land-class estimates are produced using ratio estimates (Cochran, 1963), weighted by the area of vegetative land in each land class.
- Weighting: Land-class estimates are combined using weights corresponding to the vegetative land area of each land class.
- Uncertainty assessment: Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness concerns in some features.

## Practical implications for data users

- When using CS data, consider the stratified sampling design and country-specific land classifications.
- Be cautious when extrapolating from sampled squares to larger regions, especially where excluded squares (high sea or urban areas) are more prevalent.
- Use the provided weights and the bootstrap-based uncertainty estimates for robust inference.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.