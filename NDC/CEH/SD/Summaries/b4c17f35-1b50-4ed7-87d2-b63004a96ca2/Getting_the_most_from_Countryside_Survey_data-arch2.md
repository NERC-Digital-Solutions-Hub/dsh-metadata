# Notes on the downloadable data

- The exact locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision better than 100 square km.

## Sampling framework and data structure

- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and detailed measurements are taken both at the square level and within-square (e.g., quadrats for vegetation, soils, etc.).
- Measurements include a range of data types, from binary (yes/no) to continuous (areas, lengths).

## Representativeness and exclusions

- The CS sample squares are not a random subset of all GB squares; sampling is stratified by the ITE Land Classification.
  - Country-specific classifications: England (21 classes), Wales (8), Scotland (16); classifications have evolved (32 → 45 classes historically) to accommodate separate country reporting.
- Estimates ignoring stratification may be unrepresentative and have incorrect variation estimates.
- Not all GB squares were surveyed; squares with more than 90% sea or more than 75% urban area (per 1:250,000 OS maps) were excluded.
  - Official GB estimates assume that vegetative land in excluded squares is similar in composition to sampled squares; this may introduce bias mainly in regions with high sea/urban area proportions, though such areas are generally small.

## Estimation and uncertainty

- Land class estimates are produced using ratio estimates (weighted by the vegetative land area within each land class).
- For global GB estimates and regional estimates, area weights by vegetative land are used.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993).

## Practical implications for analysts

- When using CS data, account for stratified sampling and area-weighted estimation.
- Be cautious about extrapolating to excluded squares (high sea/urban regions) and acknowledge potential bias in such areas.
- Use bootstrap-based standard errors and confidence intervals for uncertainty assessment.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.