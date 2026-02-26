# Notes on the downloadable data

## Key data characteristics
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain.
- Each selected square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils).
- Measurements include a range of variable types from binary to continuous.
- The sample is not a random subset; it is stratified within designated strata defined by the ITE Land Classification.
- Countries have separate land classifications: England (21 classes), Wales (8 classes), Scotland (16 classes).

## Confidentiality and access
- The precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify whether specific survey squares fall within targeted areas with precision finer than 100 square km.

## Sampling design and stratification
- The sampling is two-tier: whole squares and within-square measurements.
- Stratification is based on Land Classification, with revisions over time (32 → 42 classes in 1998 for Scotland, → 45 classes in 2007 for Wales).
- Because not all GB squares were surveyed (squares >90% sea or >75% urban excluded), the field data represent only the included squares. Extrapolation to GB assumes similarity of vegetative land in excluded squares, a reasonable assumption given the small total area excluded but a potential issue where regions have higher sea/urban coverage.

## Exclusions and representativeness
- Official estimates are produced by ratio estimation by land class and weighted by the vegetative land area in each class.
- The practice assumes excluded areas are similar to sampled areas; biases are expected to be minimal unless a region has a high proportion of sea or urban land.

## Estimation and uncertainty
- Ratio estimates are used for land-class-level estimates.
- Standard errors and confidence intervals have been estimated using bootstrap methods since 1998 (to address skewness in some features).

## Data governance and usage considerations
- When analyzing CS data, account for the stratified sampling and weighting to obtain valid inferences.
- Be mindful of the representativeness limitations due to exclusions and non-random sampling.
- Use bootstrap-based uncertainty measures for robust inference.
- Data provenance notes and metadata (including confidentiality constraints) are essential for correct interpretation and use.

## References
- Barr, C.J., et al. 1993. Countryside Survey 1990 Main Report.
- Cochran, W.G. 1963. Sampling Techniques.
- Efron, B. & Tibshirani, R.J. 1993. An Introduction to the Bootstrap.