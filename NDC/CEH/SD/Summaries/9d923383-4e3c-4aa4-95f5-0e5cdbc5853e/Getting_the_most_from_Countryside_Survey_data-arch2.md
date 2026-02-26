# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness of the wider countryside; external users cannot identify squares to a precision finer than 100 square km, making it impossible to determine whether squares fall within defined areas below this threshold.

- Sampling framework:
  - CS Field Survey data come from a sample of 1 km squares across GB.
  - Each selected square is mapped and measured at two levels: the square as a whole and features within the square (e.g., quadrats for vegetation and soils).
  - Measurements span various data types from binary to continuous.

- Sampling design and representativeness:
  - The sample is not a random subset of all GB squares; it is stratified by ITE Land Classification.
  - The land classification system has evolved: 32 classes originally; 42 classes in 1998 for Scotland reporting; 45 classes after Wales reporting adjustments (now 21 England, 8 Wales, 16 Scotland). Estimates should account for stratification; ignoring it may yield non-representative results or incorrect variation estimates.
  - Not all GB squares were surveyed; squares without vegetation-dominant land in surveyable areas (e.g., more than 90% sea or more than 75% urban as per 1:250,000 OS maps) were excluded. Estimates for GB or regions assume similar vegetative land composition in excluded squares, which is generally a reasonable assumption because the excluded land area is small, though problems may arise in regions with high sea/urban proportions.

- Estimation approach:
  - Official estimates are produced using ratio estimates for each land class, weighted by the vegetative land area of the class.
  - From 1998 onward, standard errors and confidence intervals are estimated via bootstrap methods to address skewness in some features.

- Implications for analysis and data use:
  - Analysts should incorporate stratification by land class and area weights when deriving estimates.
  - When combining CS data with other datasets or when performing regional analyses, be mindful of the underlying sampling design and the bootstrap-based uncertainty estimates.
  - Use the confidentiality constraints to understand spatial resolution limitations when interpreting results or mapping outputs.

- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.