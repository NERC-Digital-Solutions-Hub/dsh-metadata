# Notes on the downloadable data

- Context: Countryside Survey (CS) field data are collected from a sample of 1 km squares in GB, with measurements at both the square level and within-square features (binary and continuous variables).
- Data confidentiality: Precise locations of CS survey squares are kept confidential by CEH; external users will not receive location precision finer than 100 square km, limiting ability to identify whether squares fall in defined areas.

## Sampling design and data structure
- Two levels of sampling: whole square and within-square measurements (e.g., vegetation, soils).
- Not a random subset; the sample is stratified by ITE Land Classification.
- Land Classification: classifications expanded over time (32 → 42 → 45 classes), with country-specific classifications (England 21, Wales 8, Scotland 16).

## Representativeness and limitations
- Estimates derived from CS data must account for stratification; ignoring it can yield non-representative estimates and incorrect variation.
- Exclusions: squares with >90% sea or >75% urban land (based on 1:250000 OS maps) are not surveyed.
- Representativeness caveat: official GB/ regional estimates assume excluded squares have vegetative land composition similar to sampled squares; bias is typically small unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty
- Estimation method: ratio estimates are used for land-class estimates, weighted by the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are calculated using bootstrap methods (per Efron & Tibshirani) to address skewness.

## Practical implications for analysts
- When using CS data, incorporate stratification by land class and the 1 km square sampling framework.
- Respect location confidentiality: use aggregated or coarser geographic units (≤100 sq km precision) for analyses requiring spatial specificity.
- Be aware of exclusions that limit representativeness; exercise caution when extrapolating beyond included squares.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling techniques.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.