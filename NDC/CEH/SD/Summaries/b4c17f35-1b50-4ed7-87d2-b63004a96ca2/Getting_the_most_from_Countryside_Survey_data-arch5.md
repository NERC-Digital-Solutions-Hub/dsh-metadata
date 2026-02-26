# Notes on the downloadable data

- Data confidentiality: precise locations of Countryside Survey (CS) squares are kept confidential by CEH; external users will not receive locations with precision better than 100 square km, making it impossible to identify whether squares fall within defined areas below this threshold.
- Sampling framework: CS field survey data come from a sample of 1 km squares across GB, with two levels of sampling (the whole square and features within the square). Measurements vary in type (binary to continuous).
- Non-random, stratified design: squares are not a random subset; sampling is stratified by the ITE Land Classification, with country-specific classifications (England 21 classes, Wales 8, Scotland 16) and historical changes in classification (32 → 42 → 45 classes). Analyses that ignore stratification may be non-representative.
- Excluded squares and representativeness: squares with >90% sea or >75% urban area are excluded from field surveys. Official estimates assume similarity between excluded and sampled squares; bias is unlikely overall but can be problematic in regions with high sea/urban proportions.
- Estimation and uncertainty: land-class estimates are produced using ratio estimates weighted by vegetative land area. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness.
- References and provenance: key sources include Barr et al. (1993) for the 1990 Main Report, Cochran (1963) on sampling techniques, and Efron & Tibshirani (1993) on the bootstrap.

## Sampling Considerations in the use of Countryside Survey Data

- Levels and data types: measurements are taken at both whole-square and within-square levels, spanning a range from binary to continuous variables.
- Stratified sampling implications: the ITE Land Classification drives the design; country-specific classifications affect estimates and their interpretation.
- Representativeness and analysis: estimates may be biased if stratification and weighting are not properly accounted for; ratio estimates and area-based weights are used to derive land-class estimates.
- Exclusions and potential bias: the same exclusion criteria apply (sea/urban proportion); region-level biases may arise if excluded areas differ markedly.
- Inference methodology: bootstrap is used for standard errors and confidence intervals to accommodate skewness and complex survey design.
- Governance and metadata considerations for data stewards: document and communicate the sampling design, strata, exclusion criteria, weighting approach, and bootstrap methods; clearly state limitations on representativeness and privacy constraints for location data; reference underlying sources.