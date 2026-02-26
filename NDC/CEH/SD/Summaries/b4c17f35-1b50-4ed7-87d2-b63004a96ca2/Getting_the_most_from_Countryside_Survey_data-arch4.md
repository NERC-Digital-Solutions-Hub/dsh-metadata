# Notes on the downloadable data

## Key points for data leaders

- Access and confidentiality
  - Precise locations of Countryside Survey (CS) squares are confidential to preserve representativeness.
  - External users cannot identify whether survey squares fall within defined areas with precision better than 100 square km.

- Data collection design
  - CS field data come from a sample of 1 km squares across Great Britain.
  - Each square is mapped and measured at two levels: the square as a whole and features within the square.
  - Measurements cover a range of types, from binary to continuous (e.g., areas, lengths).

- Sampling design and representativeness
  - The sample is not a random subset of GB squares; it is stratified by land classification (ITE Land Classification), with country-specific revisions over time.
  - Land classification counts: England 21 classes, Wales 8, Scotland 16 (total 45 classes across the three countries).
  - Estimates ignoring stratification may be unrepresentative; analyses should incorporate stratification to capture variation.

- Exclusions and generalizability
  - Squares with >90% sea or >75% urban area were excluded from field surveys.
  - Official GB estimates assume similarity in vegetative land between excluded and included squares; bias is generally small unless a region has a high share of sea/urban squares.

- Analysis methods and uncertainty
  - Estimates by land class are produced using ratio estimation techniques, weighted by vegetative land area per class.
  - Standard errors and confidence intervals are estimated with bootstrap methods since 1998, addressing skewness concerns.

- Practical implications for data use
  - Users should account for stratification, weighting, and the partial coverage due to exclusions when deriving GB or regional inferences.
  - Data interpretation relies on the assumption that excluded areas do not drastically differ from sampled areas in vegetative composition, except in regions with substantial sea or urban coverage.

## Data structure and measurement details

- Two levels of measurement per square: square-level characterisations and within-square features (e.g., quadrats for vegetation, soils).
- Variables range from binary to continuous, enabling a variety of analyses but requiring careful handling of sampling design.

## Considerations for data governance and quality

- Representativeness relies on the stratified design and area-weighted aggregation by land class.
- Uncertainty is addressed via bootstrap methods, reflecting potential variability across strata and sample squares.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.