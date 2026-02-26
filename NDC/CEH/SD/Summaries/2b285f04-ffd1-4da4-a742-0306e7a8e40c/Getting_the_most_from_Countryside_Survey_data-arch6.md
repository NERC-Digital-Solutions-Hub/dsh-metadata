# Notes on the downloadable data

- Confidentiality and availability
  - To preserve representativeness of the wider countryside, precise locations of CS survey squares are kept confidential by CEH.
  - External users cannot identify whether squares fall within defined areas to a precision better than 100 square km.

- What the Countryside Survey (CS) Field Survey data include
  - Based on a sample of 1 km squares in Great Britain (GB).
  - Each selected square is mapped and detailed measurements are taken for features within the square.
  - Two levels of sampling and measurement:
    - Whole square level (characterises the square).
    - Within-square level (describes features inside the square).
  - Measurements vary in type, including binary (yes/no) and continuous (areas/lengths).

- Sampling design and representativeness
  - CS sample squares are not a random subset of all GB squares.
  - The sample is stratified, with sub-samples drawn within designated strata defined by the ITE Land Classification.
  - Land Classification history:
    - Original: 32 classes.
    - 1998: revised to 42 classes for Scotland reporting.
    - 2007: revised to 45 classes for Wales reporting.
    - Each country uses its own set of classes (England: 21, Wales: 8, Scotland: 16).
  - Not all GB squares were considered for field survey:
    - Excluded if 1:250,000 scale OS area > 90% sea, or > 75% urban.
  - Implication: official estimates are representative only of included squares; extrapolation assumes similar vegetative land composition in excluded squares. This is generally acceptable because the excluded area is small, but regional differences (e.g., high sea/urban proportions) can cause bias.

- Estimation methods
  - Estimates are produced using ratio estimates (Cochran, 1963) for each land class, incorporating the area of vegetative land in each sample square.
  - Land class estimates are combined using weights equal to the vegetative land area of each land class as a whole.

- Uncertainty and inference
  - Since some features are skewed, standard errors and confidence intervals are estimated using the bootstrap approach (Efron and Tibshirani, 1993) from 1998 onward.

- Practical implications for data use
  - When analyzing CS data, account for stratification and weighting by vegetative land area to obtain representative estimates.
  - Be cautious with regions or analyses that may be sensitive to the inclusion/exclusion of squares with high sea or urban coverage.
  - Understand that extrapolations to GB-wide or regional scales rely on assumptions about excluded squares.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.