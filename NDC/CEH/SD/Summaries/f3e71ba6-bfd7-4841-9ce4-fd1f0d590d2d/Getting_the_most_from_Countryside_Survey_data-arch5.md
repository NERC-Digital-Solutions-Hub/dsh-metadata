# Notes on the downloadable data

- Data confidentiality and location privacy
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users will not receive location precision finer than 100 square km, preventing identification of whether squares fall within certain areas.

- Sampling design and data structure
  - CS Field Survey data come from a sample of 1 km squares across GB.
  - Two levels of sampling: the square level and within-square measurements (e.g., quadrats, vegetation, soils).
  - Measurements include a mix of binary and continuous variables, captured at both levels.

- Sampling methodology and stratification
  - The sample is not a random subset; it is stratified by the ITE Land Classification.
  - Land classification has evolved: originally 32 classes, updated to 42 (1998) for Scotland, and 45 classes (2007) to accommodate Wales reporting; currently separate country classifications (England: 21, Wales: 8, Scotland: 16).

- Representativeness and limitations
  - Estimates must account for stratification; analyses ignoring stratification may be biased.
  - Not all GB squares are surveyed: squares >90% sea or >75% urban (per 1:250,000 OS maps) were excluded.
  - Broad assumption for GB or regional estimates: vegetative land in excluded squares is similar to sampled squares; bias is typically negligible unless a region has a high sea/urban proportion.

- Estimation and uncertainty
  - Official GB and regional estimates use ratio estimators by land class, weighted by vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are estimated with bootstrap methods due to skewness concerns (Efron & Tibshirani).

- Practical implications for data stewardship and reuse
  - Metadata should clearly document sampling design, stratification, weighting, and the bootstrap approach for uncertainty.
  - User guidance should emphasize the non-random, stratified nature of the sample and the implications for representativeness.
  - Location privacy constraints must be reflected in data access controls and data release practices.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.