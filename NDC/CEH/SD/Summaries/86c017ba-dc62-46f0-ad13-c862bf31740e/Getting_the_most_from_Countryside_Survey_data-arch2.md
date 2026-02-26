# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify whether squares fall within defined areas with precision finer than 100 square km.

## Sampling design and data structure

- CS field survey data come from a sample of 1 km squares in Great Britain (GB), with two levels of sampling: the whole square and measurements within the square (e.g., quadrats for vegetation, soils).
- Measurements include binary and continuous variables, covering features at both the square level and within-square features.
- The sample is not a random subset; it is stratified by the ITE Land Classification. Land classifications have evolved:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
  - National classifications changed over time (1998 Scotland, 2007 Wales) to accommodate country reporting requirements.
- Not all GB squares were surveyed. Squares with >90% sea or >75% urban area were excluded. Estimates for GB or regions assume excluded squares are similar in vegetative land composition to sampled squares, which is generally plausible but can bias region-specific results if a region contains a high proportion of sea/urban squares.

## Implications for analysis

- Because of stratified, non-random sampling, analyses must account for the sampling design; naïve estimates may be biased if stratification is ignored.
- Official land-class estimates are produced using ratio estimators that weight by the vegetative land area within each land class; GB-wide or regional estimates use weights based on the vegetative land area of land classes.
- Since 1998, standard errors and confidence intervals have been estimated using the bootstrap due to skewness in some features.

## Data usage considerations for monitoring

- Datasets are designed for consistent, comparable environmental health monitoring over time, suitable for producing outputs (reports, maps, charts) that reflect the stratified design and weighting.
- Confidentiality and sampling design considerations should be incorporated into any data processing, reporting, or policy performance analyses.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.