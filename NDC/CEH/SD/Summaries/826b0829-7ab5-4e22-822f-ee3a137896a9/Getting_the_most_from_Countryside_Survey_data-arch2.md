# Notes on the downloadable data

## Confidentiality of locations
- Precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify squares to better than 100 square km, limiting ability to determine whether squares fall within defined areas.

## Sampling design and levels
- CS field survey data come from a sample of 1 km squares in Great Britain.
- Two levels of sampling and measurement:
  - Whole square: characterises the square.
  - Within-square: detailed measurements of features inside the square (e.g., vegetation quadrats, soils).
- Measurements include a mix of binary and continuous variables.

## Representativeness and non-random sampling
- The sample is not a random subset of all GB squares; it is stratified within designated strata.
- Strata are defined by the ITE Land Classification, with country-specific classifications:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Land Classification classifications have evolved (32 → 42 in 1998 for Scotland, then 45 in 2007 for Wales) to accommodate country reporting needs.
- Analyses that do not account for stratification may be unrepresentative and have misestimated variation.

## Exclusions and implications for representativeness
- Squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field surveying.
- Official estimates effectively apply only to the squares meeting these criteria.
- Extrapolation to GB or regional scales assumes similar vegetative land composition in excluded squares; bias is usually small except in regions with high sea/urban square proportions.

## Estimation and uncertainty
- Estimates are produced using ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area of each class.
- Land class estimates are combined using the vegetative land area as weights.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani, 1993) due to concern about skewness of some features.

## Measurements and data structure
- Data include both square-level characterisations and within-square features, enabling analysis of overall square conditions and finer details like vegetation, soils, and related metrics.
- The approach supports standardized outputs suitable for monitoring environmental health and policy performance over time.

## Practical implications for analysts
- When using CS data, account for stratified design and weighting by vegetative land area.
- Use bootstrap-based confidence intervals for uncertainty assessment.
- Be aware that some areas are not represented due to exclusions; regional estimates may be biased if excluded areas are substantial.
- Location confidentiality limits precise geographic pinpointing, but data remain usable for broad monitoring and comparisons over time.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report. DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman & Hall; London.