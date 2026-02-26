# Notes on the downloadable data

- Confidentiality of precise survey locations: CS square locations are not identifiable to external users beyond a 100 square km precision to preserve representativeness.
- Data scope: Countryside Survey field data come from a sample of 1 km squares in Great Britain, with measurements at two levels—per square and within-square features (varied types from binary to continuous).

## Sampling design and representativeness

- Not a random sample; the CS sample is stratified by the ITE Land Classification, with country-specific classifications (England 21 classes, Wales 8, Scotland 16).
- Some squares are excluded from field survey (areas >90% sea or >75% urban by 1:250,000 maps). Estimates for GB or regions assume similarity of vegetative land in excluded squares, which may introduce bias primarily in regions with high sea/urban proportions.
- Official estimates are generated using ratio estimates that account for land-class area, then combined with weights based on vegetative land area in each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to concerns about skewness in some features.

## Data handling and provenance

- Key references: Barr et al. 1993; Cochran 1963; Efron and Tibshirani 1993.
- Measurements cover a range of feature types and are subject to the sampling design when interpreting results (e.g., representativeness depends on stratification and square exclusion criteria).

## Analytical implications for data leaders

- When using CS data, ensure analyses account for stratified sampling and the exclusion of certain squares; failing to do so may yield biased variability estimates.
- Use the provided land-class stratification and vegetative-land area weights to derive representative estimates.
- For uncertainty, rely on bootstrap-based standard errors and confidence intervals introduced from 1998 onward.
- Be mindful that precise geographic pinpointing is restricted; analyses requiring exact square-level locations should consider the 100 sq km precision limitation.

## Practical notes on data quality and access

- Access limitations due to confidentiality may affect data discoverability and reuse.
- Verification of data content and metadata is essential, given the complexity of sampling and potential regional biases.