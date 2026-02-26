# Notes on the downloadable data

- Countryside Survey (CS) field data come from a sample of 1 km squares in Great Britain, with measurements at two levels: the square as a whole and within-square features (e.g., vegetation, soils). Measurements span from binary to continuous variables.

- Location privacy: precise square locations are held confidential by CEH to preserve representativeness; external users cannot identify square locations more precisely than about 100 square kilometres.

- Data scope and representativeness: estimates are based on the sampled squares and are intended to reflect the wider countryside; some extrapolation to GB is used, with caveats about representativeness if excluded areas (e.g., sea or urban) are disproportionately large in a region.

- Metadata and data sharing: there can be barriers to data reuse due to incomplete metadata or the need to contact data originators; metadata may need to be added, and underlying data ideally should be shared publicly under appropriate governance.

- References for methodology: Barr et al. (1993); Cochran (1963); Efron & Tibshirani (1993).

# Sampling Considerations in the use of Countryside Survey Data

- Sampling design: CS squares are not a random subset; they are stratified by the ITE Land Classification. Country-specific revisions have changed the classification over time (32 classes originally; 42 in 1998; 45 in 2007). England has 21 classes, Wales 8, Scotland 16.

- Exclusions and implications: squares with area more than 90% sea or more than 75% urban were excluded from field surveys. Official GB estimates are produced by ratio estimates for each land class, weighted by vegetative land area; extrapolation assumes excluded squares have similar vegetation to sampled squares, which is generally reasonable but could bias regional estimates where sea/urban proportions are high.

- Estimation and uncertainty: standard errors and confidence intervals since 1998 are estimated using bootstrap methods due to skewness in some features (Cochran; bootstrap by Efron & Tibshirani).

- Practical guidance for monitoring frameworks: when analyzing CS data, account for stratification and weighting by vegetative land area; avoid naïve extrapolation across regions with different land-class distributions; use bootstrap-derived uncertainty measures to convey precision.

- Data governance considerations: sharing of underlying data and complete metadata enhances transparency but may require governance steps; maintain documentation of sampling design, stratification, exclusions, and weighting in monitoring outputs.