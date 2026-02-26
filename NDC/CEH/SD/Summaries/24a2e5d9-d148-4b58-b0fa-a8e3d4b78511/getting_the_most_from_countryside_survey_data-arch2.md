# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field squares are kept confidential by UKCEH to preserve representativeness; external users will not receive locations with precision better than 100 square km, making it impossible to identify whether squares fall within very specific areas.

## Sampling considerations in the Countryside Survey data

- CS field survey data come from a sample of 1 km squares in Great Britain, with measurements at two levels: the square as a whole and within-square features (various data types from binary to continuous).
- The sampling is not a simple random sample; it is stratified with sub-samples within designated strata defined by the ITE Land Classification.
  - Land Classification classifications have evolved: 32 classes originally; 42 in 1998 (Scotland reporting requirement); 45 classes in 2007 (Wales reporting requirement).
  - Each country has its own classification: England (21 classes), Wales (8), Scotland (16).
- Not all GB squares were surveyed. Squares with more than 90% sea or more than 75% urban area were excluded; thus field data represent only the included squares. Estimates for GB or regions assume excluded squares are similar in vegetative land composition; biases are expected to be small unless a region has a high proportion of sea/urban squares.
- Official estimates use ratio estimation (Cochran, 1963) for each land class, weighting by the vegetative land area within each class, and then combining these estimates using the total vegetative land area as weights.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness in some features.

## Implications for analysis and use

- Analyses that do not account for stratification and weighting may yield unrepresentative estimates or inaccurate measures of variation.
- When using CS data, follow standardized methods, verify and quality-assure data, and apply the appropriate stratified design and bootstrap-based uncertainty measures.
- Outputs are typically presented in clear formats (reports, maps, charts) and datasets are stored/uploaded to appropriate portals to support data accessibility.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.