# Notes on the downloadable data

- Countryside Survey (CS) field data are collected from a sample of 1 km squares across Great Britain (GB). Each selected square is mapped and measured in detail, including within-square measurements (e.g., quadrats for vegetation, soils, etc.). There are two levels of sampling: the square level and within-square features.
- Measurements vary in type, including binary (yes/no) and continuous (areas, lengths, etc.).
- The sample is not a random subset of all GB squares; it is stratified by land classification, with sub-samples within designated strata.

## Sampling and representativeness

- Land classification stratification:
  - The ITE Land Classification is used to define strata for square selection.
  - England: 21 classes, Wales: 8 classes, Scotland: 16 classes (total classifications have evolved: 32 originally, expanded to 42 in 1998 for Scotland, and to 45 with Wales reporting in 2007).
- Representativeness:
  - Estimates derived from CS data must account for stratification; analyses ignoring stratification may be non-representative and have incorrect variation estimates.
- Excluded squares:
  - Squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps) were not surveyed.
  - Official GB estimates assume similarity in vegetative land between included and excluded squares; bias is generally small, except in regions with substantial sea/urban coverage.
- Whole-GB estimates:
  - Estimates are produced using ratio estimators for each land class, weighted by the vegetative land area of each class.
  - From 1998 onward, standard errors and confidence intervals are estimated via bootstrap methods.

## Implications for analysis

- When using CS data, analysts should:
  - Incorporate the stratified design (land class strata) and square-area weights in analyses.
  - Use bootstrap-based confidence intervals for more robust inference, particularly for skewed features.
  - Be cautious about extrapolations to regions with high proportions of sea or urban squares or to areas outside the sampled squares.
- Data interpretation should acknowledge that some analyses may rely on assumptions about similarity between included and excluded squares.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.