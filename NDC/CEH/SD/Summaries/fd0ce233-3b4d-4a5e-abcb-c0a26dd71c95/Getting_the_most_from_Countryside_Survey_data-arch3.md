# Notes on the downloadable data

- Confidentiality of locations: Precise CS survey square locations are held in confidence by CEH and not provided to external users with precision finer than 100 square km; this prevents identifying whether squares fall within defined areas.

- Sampling design: Field data come from a sample of 1 km squares across GB, with two levels of sampling (the whole square and within-square measurements). Measurements include binary and continuous variables, collected via mapped squares and quadrats.

- Non-random, stratified sampling: The sample is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16). The classifications have evolved (32 → 42 → 45 classes) to accommodate separate country reporting.

- Representativeness and coverage: Not all GB squares are surveyed; excluded squares are those more than 90% sea or more than 75% urban (based on 1:250,000 OS map area). Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; this assumption introduces potential bias mainly in regions with high sea/urban proportions, though the impact is generally small.

- Estimation methods: GB estimates are produced using ratio estimates (per land class) weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness.

- Implications for monitoring and policy: Analysts must account for stratification, weighting by vegetative land area, and the exclusion of certain squares when interpreting regional or national trends. Transparency about data limits and the need to verify representativeness are essential for informed decision-making.

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) Bootstrap.