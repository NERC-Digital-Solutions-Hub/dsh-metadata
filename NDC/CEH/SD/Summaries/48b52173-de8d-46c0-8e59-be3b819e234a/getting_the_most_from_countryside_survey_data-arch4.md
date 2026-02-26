# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) survey squares are kept confidential by UKCEH to preserve representativeness, with a precision limit of no greater than 100 square km. Users cannot identify whether squares fall within defined areas below this threshold.
- CS field survey data consist of measurements from a sample of 1 km squares across Great Britain, with two sampling levels: whole squares and within-square features (e.g., quadrats for vegetation, soils). Variables range from binary to continuous.

## Sampling design and representativeness

- The CS sample squares are not a random subset; the design is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16) due to separate reporting needs.
- Estimates derived from CS data must account for stratification; failing to do so can yield non-representative estimates and incorrect variation.
- Not all GB squares were surveyed: squares with more than 90% sea coverage or more than 75% urban were excluded. The official estimates assume unsurveyed vegetative land is similar to surveyed squares; this approximation is generally small in impact unless a region has a very high sea/urban proportion.

## Data processing and estimation

- Estimates are produced as ratio estimates by land class, using weights based on the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to concerns about skewness in some features.
- The sampling framework implies careful use of land-class stratification and area-based weights to avoid biased estimates and misrepresented variability.

## Implications for use

- Analyses should incorporate the stratified sampling design and appropriate weights; simple aggregation without stratification may misstate variation and representativeness.
- The confidentiality of square locations limits fine-grained geographic analyses below 100 sq km precision, but preserves overall representativeness for broader-scale inferences.
- When interpreting estimates for a region, consider the proportion of water/urban squares and the potential bias introduced by excluding certain squares.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.