# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users only have access at a precision no finer than 100 square km, preventing identification of whether squares fall within defined areas.

## Sampling design and representativeness
- CS field survey data come from a sample of 1 km squares across GB, with measurements at two levels: the square level and within-square features.
- Samples are not random; they are stratified by the ITE Land Classification. The land-class classification has evolved by country: originally 32 classes, then 42 (1998, Scotland reporting), and 45 (2007, Wales reporting), resulting in country-specific classifications (England 21, Wales 8, Scotland 16).
- Estimates that ignore stratification may be unrepresentative and have inaccurate variation estimates.
- Not all GB squares were eligible for field survey. Squares that were >90% sea or >75% urban (per 1:250,000 OS maps) were excluded. Official estimates assume excluded squares are similar in vegetative land composition to sampled squares; biases are unlikely overall but could be problematic where a region has a high sea/urban proportion.

## Data processing and estimation methods
- Estimates are produced using ratio estimates for each land class, weighting by the vegetative land area within each class.
- Beginning in 1998, standard errors and confidence intervals are estimated using bootstrap methods due to concerns about skewness in some features.

## Country classifications and exclusions
- Land-class schemes are country-specific, reflecting reporting needs (England, Wales, Scotland). This affects comparability and aggregation across the UK; analyses should account for these differences.

## Uncertainty and references
- Key methodological references underpinning the sampling and estimation approach:
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Cochran (1963): Sampling Techniques
  - Efron & Tibshirani (1993): Bootstrap methods

## Data governance and usage considerations for Data Leaders
- Respect confidentiality of exact survey locations; when integrating with other datasets, manage geospatial privacy implications.
- Account for the stratified sampling design and country-specific land classifications in any analysis; apply appropriate weights and consider cross-country comparability.
- Use bootstrap-derived standard errors and confidence intervals as the uncertainty measure unless another method is justified.
- Be aware of exclusions (sea/urban squares) and the assumption that excluded areas resemble sampled areas; assess potential region-specific biases.
- Maintain clear metadata on sampling design, strata definitions, exclusions, and estimation procedures to support discovery, reproducibility, and governance.