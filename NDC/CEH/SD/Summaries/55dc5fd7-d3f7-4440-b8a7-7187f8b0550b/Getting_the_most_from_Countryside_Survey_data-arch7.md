# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify square locations to better than 100 square kilometres.
- Consequently, users cannot determine whether any survey squares fall within defined areas below this precision.

## Sampling and data structure

- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels:
  - Square level: characterises the entire 1 km square.
  - Within-square level: measurements of features within the square (e.g., quadrats for vegetation, soils, etc.).
- Measurements include a mix of binary (yes/no) and continuous variables (e.g., areas, lengths).

## Sampling design and stratification

- The sample is not a random subset of all GB squares; it is stratified.
- Stratification is by the ITE Land Classification, which has evolved over time:
  - Original: 32 land classes.
  - 1998: expanded to 42 classes (Scotland reporting requirements led to changes).
  - 2007: 45 classes (Wales reporting requirements led to further changes).
- Each country has its own classification: England (21 classes), Wales (8), Scotland (16).
- Estimates that do not account for this stratification may be unrepresentative and have inaccurate estimates of variation.

## Exclusions and representativeness

- Squares excluded from the field survey if their area (from 1:250,000 OS maps) is >90% sea or >75% urban.
- Official GB estimates are derived by ratio estimates for each land class, weighting by the vegetative land area in each class.
- For GB and regional estimates, vegetative land in excluded squares is assumed to be similar to sampled squares. This is generally a minor bias unless a region has a high proportion of sea or urban squares.

## Estimation and uncertainty

- Estimation follows ratio-estimation techniques (Cochran, 1963) for each land class.
- Land class estimates are combined using weights equal to the vegetative land area of each land class.
- Since some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) from 1998 onward.

## Implications for GIS work

- Data are suitable for map-based analyses at multiple scales, with careful attention to:
  - The confidentiality constraint: precise geolocations are not available beyond 100 km2 resolution.
  - The stratified sampling design: apply appropriate weights when aggregating across land classes or regions.
  - Uncertainty: use bootstrap-based confidence intervals to convey uncertainty in estimates.
  - Excluded areas: recognize potential biases in regions with many sea/urban squares; interpretations should consider the exclusion criteria.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.