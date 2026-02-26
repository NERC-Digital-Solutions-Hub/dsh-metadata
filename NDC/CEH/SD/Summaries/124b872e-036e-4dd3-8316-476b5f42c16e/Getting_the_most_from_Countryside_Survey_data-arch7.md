# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey collects data from a sample of 1 km squares in Great Britain, with measurements at both whole-square and within-square levels (e.g., vegetation, soils).
- Measurements include varied data types, from binary to continuous (areas, lengths, etc.).
- The sample is not a random subset; it is stratified by the ITE Land Classification, with country-specific revisions over time, resulting in England (21 classes), Wales (8), and Scotland (16) classifications.
- Estimates are produced by ratio estimates for each land class, weighted by the vegetated land area within each class.
- Standard errors and confidence intervals have been estimated using bootstrap methods since 1998 due to skewness in some features.

## Location confidentiality and precision
- To preserve representativeness, precise locations of CS survey squares are confidential. External users cannot identify square locations with precision better than 100 square kilometers.
- This limitations means you cannot determine whether specific survey squares fall within defined, finer geographic areas.

## Sampling design and representativeness
- CS sampling has two levels: the whole 1 km square and measurements within each square.
- The design is stratified and country-reported; estimates must account for this stratification to avoid biased variation estimates.
- Not all GB squares were considered for field survey; squares exceeding 90% sea or 75% urban at 1:250,000 scale were excluded. Estimates for GB or regions assume excluded squares have vegetation similar to sampled squares, which is a potential source of bias, particularly in regions with high sea/urban proportions.

## Data limitations and implications for GIS work
- Data are representative only of the squares included in the survey; extrapolation to the entire GB area relies on assumptions about excluded areas.
- Because of geographic and data-collection constraints, users must integrate the sampling design (stratification, weights, and bootstrap-derived uncertainty) into any GIS analyses and map products.
- The confidential location information affects the granularity available for map display; maps should reflect generalized locations or aggregated zones.

## Practical guidance for GIS specialists
- When creating map-based products, use the land-class stratification and vegetated-area weights to produce area-adjusted estimates.
- Incorporate bootstrap-based standard errors or confidence intervals to convey uncertainty, especially for features with skewed distributions.
- Acknowledge that estimates are representative only for included squares and may not fully generalize to all GB areas, particularly those with high seas or urban areas.
- Respect the confidentiality constraint by avoiding precise pinpointing of square locations and representing data at appropriate generalized scales.

## References
- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.