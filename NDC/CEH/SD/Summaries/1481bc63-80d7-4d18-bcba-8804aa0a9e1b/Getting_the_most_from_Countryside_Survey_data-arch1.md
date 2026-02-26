# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify whether squares fall within defined areas with precision finer than 100 square kilometers.
- CS field survey data come from a sample of 1 km squares across GB, with two levels of sampling: the square itself and measurements within the square (e.g., quadrats for vegetation, soils). Measurements include binary and continuous variables.

## Sampling design and representativeness

- The CS sample is not a random subset; it is stratified by the ITE Land Classification. Each country uses its own classification: England (21 classes), Wales (8 classes), Scotland (16 classes). Classifications have evolved (32 → 42 → 45) for separate country reporting.
- Estimates drawn from CS data must account for stratification; ignoring it can lead to non-representative results and incorrect variation estimates.
- Some squares were excluded from field survey: area > 90% sea or > 75% urban (based on 1:250,000 scale OS maps). Official estimates assume excluded squares have similar vegetative land composition to sampled squares; bias is expected to be small unless a region has a high proportion of sea/urban squares.
- Estimates are produced using ratio estimates by land class, weighting by the vegetative land area in each land class. Since 1998, standard errors and confidence intervals are estimated via bootstrap methods due to skewness in some features.

## Measurement and data structure

- Measurements are taken at two levels: characterising the entire square and describing features within the square.
- Data types vary from binary to continuous (e.g., areas, lengths). Measurements cover vegetation, soils, and other surveyed features.

## Estimation and uncertainty

- Ratios by land class are used with area-based weights to produce GB-wide or regional estimates.
- Bootstrap is used to estimate standard errors and confidence intervals, addressing skewness in certain features.

## Data access and privacy

- Location privacy considerations govern data release; detailed site-level precision is limited to protect broader representativeness.
- Metadata and dataset provenance are important for reproducibility; datasets may be discoverable with proper metadata.

## Practical guidance for analysts

- When analyzing CS data, incorporate stratification by country-specific land classes and apply appropriate weights.
- Be cautious with extrapolation to excluded squares; the assumption that excluded areas resemble sampled areas underpins GB-wide estimates.
- Use bootstrap-based uncertainty estimates rather than relying on simple standard errors that ignore skewness.
- Reference the original sources for methodology and context when interpreting estimates.

### References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.