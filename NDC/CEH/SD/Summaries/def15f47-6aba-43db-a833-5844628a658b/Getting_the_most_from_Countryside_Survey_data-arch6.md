# Notes on the downloadable data

- Purpose and scope
  - Describes considerations for using Countryside Survey (CS) Field Survey data, including privacy constraints and sampling design.
  - Data comprise measurements from a sample of 1 km squares in Great Britain, with two levels of sampling (whole square and within-square features).

- Privacy and data availability
  - Precise locations of CS survey squares are confidential and anonymized to no greater precision than 100 square kilometers.
  - Users cannot identify whether specific squares fall within defined areas below this threshold.

- Sampling design and representativeness
  - Not a random subset; the CS sample is stratified by ITE Land Classification.
  - Country-specific land-class classifications exist: England (21 classes), Wales (8), Scotland (16); classifications have been revised over time (32 → 42 → 45 classes).
  - Some squares are excluded from field surveys (more than 90% sea or more than 75% urban by 1:250,000 maps). Estimates are generally produced for the included squares; GB estimates assume excluded squares have similar vegetative land composition, which may introduce bias if regional sea/urban proportions are high.

- Estimation and analysis implications
  - Official estimates use ratio estimators for each land class, weighted by the vegetative land area of each class.
  - Since some strata and areas are omitted or skewed, proper analysis requires accounting for stratification and weighting.
  - From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods to address skewness.

- Practical guidance for data users
  - Ensure analyses reflect the stratified design and weighting; avoid unadjusted pooling across strata.
  - Be aware that the data are representative only of the included squares, with potential regional biases if excluded areas (sea/urban) are substantial.
  - Reference materials provide methodological foundations for sampling and estimation (Cochran 1963; Efron & Tibshirani 1993).

- References
  - Barr et al. 1993. Countryside Survey 1990 Main Report.
  - Cochran, W.G. 1963. Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. 1993. An Introduction to the Bootstrap.