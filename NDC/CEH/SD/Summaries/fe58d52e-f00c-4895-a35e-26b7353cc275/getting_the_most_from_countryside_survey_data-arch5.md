# Notes on the downloadable data

- Confidentiality of locations: Precise positions of Countryside Survey squares are kept confidential by UKCEH. External users will not be able to identify squares with precision finer than 100 square km, limiting ability to map to defined areas below that threshold.
- Data scope: Field data come from a sample of 1-km squares in Great Britain, with measurements made at two levels (whole square and within-square) and across various variable types (binary to continuous).
- Publication and reuse implications: Because the sample is not a simple random sample of all 1-km squares, analyses must account for stratification and sampling design to avoid biased estimates.

## Sampling design and data structure

- Two-level sampling: Each selected 1-km square is mapped and measured at both the square level and within-square features (e.g., vegetation quadrats, soils).
- Variable types: Measurements range from binary Yes/No to continuous metrics (areas, lengths), across both levels.

## Stratification and land classifications

- Non-random, stratified sampling: The CS sample is stratified by designated strata within the ITE Land Classification framework.
- Classification revisions: 
  - Original 32 land classes
  - 1998: revised to 42 classes to support Scotland-specific reporting
  - 2007: revised to 45 classes to support Wales-specific reporting
  - Each country uses its own class structure (England, Wales, Scotland).
- Implication for analyses: Estimates that ignore stratification may be unrepresentative and misstate variation.

## Representativeness and geographic coverage

- Exclusions: Squares with more than 90% sea or more than 75% urban area (as per 1:250,000 OS maps) were excluded from field survey.
- Practical representation: Field data primarily represent the included squares. Extrapolation to GB or regional scales assumes excluded vegetative land resembles included areas; bias is expected to be small except in regions with high sea/urban square proportions.

## Estimation and uncertainty

- Estimation approach: Official land-class estimates are produced using ratio estimators that weight by the vegetative land area within each land class.
- Handling skewness: Since some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) since 1998.

## Practical implications for data governance and sharing

- Metadata considerations: Document the stratification scheme, classification versions by country, and the exclusion criteria to ensure correct interpretation and reuse.
- User guidance: Clearly communicate that analyses must account for stratified sampling and weighting; avoid naive aggregation that ignores the sampling design.
- Reproducibility: Note the bootstrap-based uncertainty measures and the need to apply the same estimation framework when reusing the data.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.