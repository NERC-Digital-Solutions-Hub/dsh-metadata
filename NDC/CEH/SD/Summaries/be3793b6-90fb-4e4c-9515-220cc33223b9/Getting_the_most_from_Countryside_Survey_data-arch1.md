# Notes on the downloadable data

- Location confidentiality: precise CS survey square locations are kept confidential by CEH and external users cannot identify squares with precision finer than 100 square kilometres.
- Implication: users cannot determine whether specific survey squares fall within defined areas below this threshold.

## Sampling Considerations in the use of Countryside Survey Data

- Data scope: Countryside Survey (CS) Field Survey data come from a sample of 1 km squares across Great Britain (GB), with measurements at both the square level and within-square features (e.g., quadrats for vegetation and soils).
- Two-level sampling: Measurements characterize the whole square and features within the square; data types range from binary to continuous.
- Non-random, stratified sample: The CS sample is not a random subset; it is stratified by the ITE Land Classification. Country-specific updates changed the classification over time (32 → 42 → 45 classes); England, Wales, and Scotland have 21, 8, and 16 classes respectively.
- Representativeness caveat: Estimates that do not account for stratification may be biased; variations may be misrepresented if stratification is ignored.
- Excluded squares: Some squares (based on 1:250,000 OS map area) were excluded from field survey if more than 90% sea or more than 75% urban. The field-survey data thus representations are strictly for squares meeting these criteria.
- Extrapolation and bias: When estimating for GB or regions, vegetative land in excluded squares is assumed similar to sampled squares. This bias is generally small unless a region has a high proportion of sea or urban land.
- Estimation method: Official CS estimates are produced as ratio estimates by land class, weighting by the vegetative land area within each land class.
- Uncertainty assessment: Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.
- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.