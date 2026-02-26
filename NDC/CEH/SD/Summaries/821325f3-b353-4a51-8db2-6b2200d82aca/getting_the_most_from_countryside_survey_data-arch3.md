# Notes on the downloadable data

- Confidentiality of locations: The precise locations of Countryside Survey squares are kept confidential by UKCEH. External users will not be provided with precision finer than 100 square km, making it impossible to determine whether squares fall within defined areas below this threshold.

- What the data are: Countryside Survey (CS) field data come from a sample of 1-km squares in Great Britain (GB). In each selected square, the whole square is mapped and detailed measurements are taken for selected features. Measurements occur at two levels: the square level and within-square features (e.g., quadrats).

- Data types: Measurements range from binary (yes/no) variables to continuous metrics (areas, lengths, etc.).

- Sampling design and representativeness: CS squares are not a random subset of all GB 1-km squares; the sample is stratified within Land Classification strata defined by ITE. The land classification has evolved (32 classes originally; 42 in 1998; 45 classes after Wales reporting changes). England has 21 classes, Wales 8, Scotland 16. Analyses that ignore stratification may yield non-representative estimates and incorrect variation.

- Excluded squares: Squares with more than 90% sea or more than 75% urban area were excluded from field survey. Official estimates for GB assume vegetative land in excluded squares is similar to sampled squares; this assumption may introduce bias if a region has a high proportion of sea/urban squares, though the overall impact is expected to be small.

- Estimation approach: Estimates are produced by ratio estimation within land classes, weighting by the area of vegetative land in each class. Since 1998, standard errors and confidence intervals have been estimated using the bootstrap method to address skewness.

- Data handling and transparency: The notes imply a need for careful data governance, including accounting for stratification and ensuring appropriate data sharing and metadata practices to support reuse and verification.

- Data provenance and references: Key methodological references include Barr et al. (1993) for the Countryside Survey 1990 Main Report, Cochran (1963) on sampling techniques, and Efron & Tibshirani (1993) on the bootstrap.

## Sampling Considerations in the use of Countryside Survey Data

- The CS sampling framework is two-level (square-level and within-square measurements) and is not based on a random subset of all GB squares; analyses must account for stratification by Land Classification.

- Land Classification: The country-specific classifications (England, Wales, Scotland) create 21, 8, and 16 classes respectively; estimates should be derived with appropriate weighting by vegetative land area within each class.

- Representativeness and exclusions: Coverage is limited to squares meeting inclusion criteria (not mostly sea/urban). When applying GB- or region-wide inferences, assume similar vegetative composition in excluded squares, acknowledging potential regional bias where exclusions are substantial.

- Uncertainty estimation: Use of bootstrap methods since 1998 provides standard errors and confidence intervals that reflect skewness in some features; ensure bootstrap-based uncertainty is incorporated in monitoring outputs.

- Practical implications for monitoring: When designing monitoring frameworks or dashboards using CS data, ensure metadata clearly documents stratification, weighting, exclusions, and uncertainty procedures; maintain data governance and transparent data-sharing practices for reproducibility.