# Notes on the downloadable data

- Purpose and scope
  - Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain (GB).
  - Each selected square is mapped and measured at two levels: the square as a whole and features within the square.
  - Measurements include a mix of binary and continuous variables (e.g., vegetation, soils, areas, lengths).

- Confidentiality and data precision
  - To preserve representativeness, precise locations of CS survey squares are kept confidential.
  - External users cannot identify square locations with precision finer than 100 square kilometers.
  - Consequently, it is not possible to determine if survey squares fall within specific defined areas below this threshold.

- Sampling design and representativeness
  - The CS sample squares are not a random subset of all GB squares.
  - The design is stratified: squares are selected within designated strata defined by the ITE Land Classification.
  - Land Classification changes by country:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Historical changes: classifications evolved from 32 to 42 (1998) to 45 (2007) to accommodate separate country reporting.
  - Some GB squares were excluded from field survey if at the 1:250,000 OS map scale their area was more than 90% sea or more than 75% urban.
  - Official GB or regional estimates assume vegetative land in excluded squares is similar to sampled squares; bias is expected to be small except in regions with high sea/urban square proportions.

- Estimation and uncertainty
  - Estimates are produced using ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area of that class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrapping (Efron & Tibshirani, 1993) due to skewness concerns.

- Measurements and data structure
  - Two levels of measurements:
    - Square-level: characterizes the overall square.
    - Within-square: detailed measurements (e.g., quadrats for vegetation, soils).
  - Data types range from binary variables to continuous measures (areas, lengths).

- Practical implications for GIS work
  - When using CS data in map-based analyses, account for stratified design and area-weighting by vegetative land area.
  - Incorporate uncertainty estimates (bootstrap-derived SEs) for robust spatial analyses.
  - Be mindful of non-random sampling and exclusions; avoid assuming complete representativeness of all GB squares.
  - Use the confidentiality constraint (location precision limited to 100 km^2) when integrating CS data with high-resolution spatial layers.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.