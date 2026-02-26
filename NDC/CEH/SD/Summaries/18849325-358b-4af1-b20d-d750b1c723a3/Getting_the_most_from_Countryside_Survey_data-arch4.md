# Notes on the downloadable data

- Location confidentiality: The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify square locations with precision finer than 100 square kilometers, meaning you cannot determine whether a square falls within defined areas at finer scales.

- Sampling design and data levels: CS field survey data come from a sample of 1 km squares across GB. Each square is mapped and measured at two levels—whole square and within-square features—yielding varied data types from binary to continuous (e.g., areas, lengths, vegetation, soils).

- Non-random, stratified sampling: The sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification. Land classes have evolved over time (32 → 42 → 45 classes) to accommodate country-specific reporting (England, Wales, Scotland). Analyses that ignore stratification may produce biased estimates or misrepresent variability.

- Excluded squares and representativeness: Some squares are excluded from field survey (areas >90% sea or >75% urban, based on 1:250,000 OS maps). Official GB estimates assume excluded squares have similar vegetative land composition to sampled squares; this assumption may introduce bias mainly in regions with high sea/urban proportions and is generally considered small.

- Estimation approach: Estimates are produced using ratio estimators within each land class, weighting by the vegetative land area of each class. The class estimates are then combined across classes using the total vegetative land area as weights.

- Uncertainty estimation: Since 1998, standard errors and confidence intervals are calculated using bootstrap methods due to skewness in some features.

- References and methodological basis: Barr et al. (1993) on Countryside Survey 1990 methodology; Cochran (1963) on sampling techniques; Efron & Tibshirani (1993) on bootstrap methods.