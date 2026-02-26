# Notes on the downloadable data

- Confidentiality and representativeness
  - Precise locations of Countryside Survey (CS) field squares are kept confidential by CEH.
  - External users cannot determine whether squares fall within defined areas with precision better than 100 square km.
  - Purpose: preserve representativeness of the wider countryside in analyses.

- Sampling design and data structure
  - CS field survey data come from a sample of 1 km squares in Great Britain (GB).
  - Two levels of measurement: (1) whole squares characterized, (2) features within squares described (e.g., quadrats for vegetation, soils, etc.).
  - Measurements span binary and continuous variables.
  - The sample is not a random subset; it is stratified by Land Classification (ITE classification).

- Land Classification and country specifics
  - Stratification by Land Classification with country-specific classifications.
  - England: 21 classes; Wales: 8 classes; Scotland: 16 classes.
  - Classifications have evolved (32 → 42 → 45 classes) due to separate country reporting needs.

- Exclusions and representativeness caveats
  - Squares with >90% sea area or >75% urban area (as per 1:250,000 OS maps) are excluded from field survey.
  - Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; bias is expected to be small except in regions with high sea/urban coverage.

- Estimation approach
  - Estimates are ratio estimates (Cochran, 1963) calculated for each land class, weighting by vegetative land area in each square.
  - Land-class estimates are combined using weights equal to the vegetative land area of each land class across GB.
  - Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron and Tibshirani, 1993) to handle skewness.

- Implications for analysis
  - Analyses must account for stratified sampling and weighting to obtain representative estimates.
  - Misinterpreting without stratification can lead to biased variances and conclusions.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.