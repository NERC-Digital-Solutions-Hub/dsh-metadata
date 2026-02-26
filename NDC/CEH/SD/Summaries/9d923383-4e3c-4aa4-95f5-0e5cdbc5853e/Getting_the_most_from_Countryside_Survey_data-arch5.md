# Notes on the downloadable data

## Confidentiality and data precision
- To preserve representativeness, precise locations of CS survey squares are kept confidential by CEH.
- External users cannot identify square locations with precision finer than 100 square km.

## Sampling design and data structure
- Countryside Survey field data come from a sample of 1 km squares across GB, with measurements made at two levels: the square as a whole and features within the square (e.g., quadrats for vegetation, soils, etc.).
- Data types range from binary to continuous.
- The sampling is stratified by the ITE Land Classification; country-specific classifications have evolved: England (21 classes), Wales (8), Scotland (16). The classification has changed over time (32 -> 42 -> 45 classes) due to separate country reporting.
- Not all GB squares were considered for field survey. Squares that were >90% sea or >75% urban were excluded.
- Official estimates are produced using ratio estimates by land class, weighted by the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to concerns about skewness in some features.

## Data usage implications
- Analyses not accounting for stratification may be unrepresentative; proper weighting by land class and consideration of the sampling design are essential.
- Estimates for the whole GB or regions assume similarity in vegetative land in excluded squares; this assumption may introduce bias, especially in regions with higher sea or urban square proportions.
- The field survey data are not a simple random sample; results rely on the stratified design and weighting.

## Data governance and metadata considerations
- Methodological references: Barr et al. (1993), Cochran (1963), and Efron & Tibshirani (1993) underpin the sampling and bootstrap approaches.
- Data management should document the sampling design, strata, exclusion criteria, weights, and bootstrap-based standard errors to support proper reuse and interpretation.
- Maintain confidentiality constraints and clearly communicate any disclosure risks or limitations to users.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.