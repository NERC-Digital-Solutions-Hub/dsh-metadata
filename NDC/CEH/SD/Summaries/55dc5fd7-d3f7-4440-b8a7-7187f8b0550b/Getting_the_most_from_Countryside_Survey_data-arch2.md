# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify whether squares fall within defined areas beyond 100 square km precision.
- CS Field Survey data comes from a sample of 1 km squares in Great Britain, with measurements at two levels: the square as a whole and features within the square (e.g., quadrats for vegetation, soils). Variables range from binary to continuous.

## Sampling design and representativeness

- The sample squares are not a random subset of all GB squares; it is a stratified sample with sub-samples within designated strata defined by the ITE Land Classification.
- Land Classification classifications have evolved: 32 classes originally, expanding to 42 (1998, Scotland reporting), and to 45 (2007, Wales reporting). After these changes, each country has its own set of classes (England 21, Wales 8, Scotland 16).
- Not all GB squares were surveyed; squares more than 90% sea or more than 75% urban were excluded. Official estimates assume similarity between vegetative land in excluded squares and surveyed squares, which may introduce bias mainly if a region has a high proportion of sea/urban squares.

## Estimation and inference

- Estimates are produced using ratio estimates (Cochran, 1963) for each land class, weighting by the vegetative land area of each class.
- From 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness in some features.

## Data privacy, access, and reuse

- The locations’ coarse precision (≤100 km²) supports privacy while enabling broader regional interpretation.
- A key challenge noted is increasing the value of datasets by combining CS data with other data sources and enabling access to the underlying data used to produce outputs.

## Practical guidance for analysts

- When analyzing CS data, account for the stratified sampling design and apply the appropriate land-class weights.
- Use ratio-estimate framework per land class and combine using vegetative land-area weights; interpret region-level estimates with caution due to potential biases from excluded squares.
- Rely on bootstrap-derived standard errors and confidence intervals for inference.
- Be mindful that formal representativeness applies only to squares meeting survey criteria; analyses assuming GB-wide representativeness should consider potential biases in regions with high sea/urban square exclusion.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.