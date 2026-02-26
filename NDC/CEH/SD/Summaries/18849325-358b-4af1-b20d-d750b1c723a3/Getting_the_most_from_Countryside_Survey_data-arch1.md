# Notes on the downloadable data

## Data confidentiality and access
- Exact locations of Countryside Survey (CS) squares are kept confidential by CEH; external users cannot identify square locations with precision better than 100 square km.
- This confidentiality constraint limits the ability to determine whether specific survey squares fall within defined geographic areas.

## Sampling design of Countryside Survey
- CS field survey data come from a sample of 1 km squares across Great Britain (GB); each selected square is mapped and measured.
- Two levels of sampling and measurement:
  - Whole square: general characterisation
  - Within-square: detailed measurements of features (e.g., quadrats for vegetation, soils)
- Measurements span various data types, from binary to continuous (areas, lengths, etc.).
- Not a simple random subset; the sample is stratified, with sub-samples drawn within designated strata defined by the ITE Land Classification.
- Land Classification changes over time:
  - Original: 32 classes
  - 1998: 42 classes due to Scotland reporting needs
  - 2007: 45 classes due to Wales reporting needs
  - Each country effectively has its own classification (England: 21, Wales: 8, Scotland: 16).

## Representativeness and sampling limitations
- Estimates derived from CS data must account for stratification; naïve estimates may be unrepresentative.
- Not all GB squares were considered for field survey. Excluded squares had: area > 90% sea or > 75% urban (as per 1:250,000 OS maps).
- Official GB or regional estimates assume excluded squares have vegetative land composition similar to sampled squares; biases are generally negligible unless a region has a high proportion of sea or urban land.

## Estimation and inference
- Estimates by land class are produced using ratio estimation (Cochran 1963), weighting by the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals are calculated using bootstrap methods (Efron & Tibshirani 1993) to address skewness in some features.

## Practical considerations for analysts
- When using CS data, incorporate stratification by land class and apply the appropriate weights based on vegetative land area.
- Be cautious in extrapolating to GB or regional scales if your area includes many excluded (sea/urban) squares.
- Use bootstrap-based confidence intervals for uncertainty assessment, particularly for skewed features.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.