# Notes on the downloadable data

- Purpose: Describes the Countryside Survey (CS) Field Survey data collected from a sample of 1 km squares in Great Britain, including data collection at two levels (whole squares and within-square features) and the types of measurements collected.
- Data scope: Information on vegetation, soils, and other features collected via mapped squares and within-square quadrats; measurements range from binary to continuous variables.

## Data confidentiality and access

- To preserve representativeness of the wider countryside, precise square locations are held confidential by CEH.
- External users are not provided with square locations at a precision better than 100 square kilometers.

## Sampling design and classifications

- Sampling involves two levels: whole 1 km squares and within-square measurements.
- The sample is not a random subset of all GB squares; it is stratified within the ITE Land Classification framework.
- Land Classification changes over time and by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Classifications have evolved: originally 32 classes, updated to 42 in 1998 for Scotland, and to 45 in 2007 due to Wales reporting needs.

## Representativeness and exclusions

- Not all GB squares were considered for field survey.
- Exclusions: squares >90% sea or >75% urban by 1:250,000 OS map area.
- Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; bias is generally negligible unless a region has a high proportion of sea or urban squares.

## Estimation and statistical methods

- Estimates are produced by ratio estimation (Cochran, 1963) for each land class, using the vegetative land area within each sample square as a weight.
- Land class estimates are combined using the overall vegetative land area as weights.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness in some features.

## Implications for data use and stewardship

- Analyses should account for stratification by land class and the weighting scheme; simple non-weighted estimates may be biased.
- Users should be aware of the sampling design, exclusions, and the bootstrap-based uncertainty estimates.
- Metadata should document:
  - Sampling design (stratified by land class, country-specific classifications)
  - Exclusions criteria and potential regional biases
  - Weighting structure and bootstrap SEs
  - Confidentiality constraints on location data

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.