# Notes on the downloadable data

- Privacy and geographic precision
  - Exact counts of Countryside Survey squares are confidential to preserve representativeness.
  - External users cannot identify survey squares with precision better than 100 square km.
  - Consequently, users cannot determine whether squares fall within defined areas below that threshold.

- Structure and scope of Countryside Survey data
  - Field data come from a sample of 1-km squares across Great Britain.
  - Each selected square is mapped; measurements are taken at two levels: whole square and within-square features.
  - Measurements vary from binary to continuous (e.g., areas, lengths).

- Sampling design and representativeness
  - The CS sample is not a random subset of all 1-km squares; it is stratified by land class.
  - Land classification evolves by country (England, Wales, Scotland) and has changed over time (21 classes in England, 8 in Wales, 16 in Scotland as of revisions).
  - Estimates must account for stratification; ignoring it can lead to unrepresentative estimates and incorrect variation.

- Exclusions and implications for representativeness
  - Squares with more than 90% sea or more than 75% urban area were excluded from field surveys.
  - Official GB estimates assume excluded vegetative land is similar in composition to included squares; bias is likely small unless a region is dominated by sea/urban squares.

- Estimation and weighting
  - Estimates by land class are produced using ratio estimates that weight by the vegetative land area within each class.
  - From 1998, to address skewness in certain features, standard errors and confidence intervals are estimated using bootstrap methods.

- Practical guidance for analysis
  - When using CS data, adjust analyses for stratification and appropriate weighting to obtain valid variance estimates.
  - Be mindful of regional representativeness and potential biases from excluded squares.
  - Use the reported bootstrap-based uncertainty measures for inference where applicable.

- References and methodological basis
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Cochran (1963): Sampling Techniques
  - Efron & Tibshirani (1993): An Introduction to the Bootstrap

- Key takeaway for data strategy
  - Clearly document sampling design, exclusions, and weighting when integrating CS data with other datasets.
  - Communicate limitations related to geographic precision, stratification, and assumptions about excluded areas to stakeholders.