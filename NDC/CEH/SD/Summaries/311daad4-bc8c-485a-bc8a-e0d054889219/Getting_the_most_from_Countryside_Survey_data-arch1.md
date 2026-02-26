# Notes on the downloadable data

- Confidentiality of locations: precise CS survey square locations are held confidential by CEH; external users cannot be identified to any more precise than 100 square km. This prevents determining whether squares fall within defined areas below that threshold.

## Sampling design and structure

- Data scope: Countryside Survey (CS) Field Survey data come from a sample of 1 km squares across GB.
- Two levels of sampling: whole squares and within-square measurements (e.g., quadrats for vegetation, soils).
- Measurement types: varied, including binary and continuous variables.
- Non-random, stratified sampling: squares are not a random subset; sampling is stratified by the ITE Land Classification.
- Land classification evolution:
  - Original: 32 classes
  - 1998: Scotland-specific reporting increased to 42 classes
  - 2007: Wales-specific reporting increased to 45 classes
  - Currently: England (21 classes), Wales (8 classes), Scotland (16 classes)
- Implication: estimates from CS data without accounting for stratification may be unrepresentative and have inaccurate variation estimates.

## Selection and coverage of squares

- Exclusions: squares with >90% sea area or >75% urban area (based on 1:250,000 OS maps) were excluded from field survey.
- Representativeness caveat: official GB/ regional estimates assume vegetative land in excluded squares is similar to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty

- Estimation method: official land-class estimates are produced using ratio estimation (Cochran, 1963), weighted by the vegetative land area of each land class.
- Uncertainty assessment: since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness concerns.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.