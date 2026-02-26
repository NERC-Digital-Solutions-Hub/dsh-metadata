# Notes on the downloadable data

## Purpose and scope
- Countryside Survey (CS) field data collected from a sample of 1 km squares across Great Britain (GB).
- Two levels of data within each square: the square itself and features within the square (e.g., vegetation, soils) measured via quadrats.
- Data types range from binary yes/no to continuous measures (areas, lengths).
- Aimed at providing representative environmental health measures for monitoring and decision-making.

## Sampling design
- The CS sample is not a random subset of all GB squares; it is stratified by designated strata.
- Stratification based on the ITE Land Classification, with country-specific adaptations:
  - England: 21 land classes
  - Wales: 8 land classes
  - Scotland: 16 land classes
- Changes over time reflect separate country reporting; overall classification has evolved (32 → 42 → 45 classes historically).
- Only squares with certain land characteristics are surveyed; not all GB squares are considered.

## Data confidentiality and geolocation
- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify squares with precision finer than 100 square kilometres.
- This confidentiality limits external geospatial identification of survey coverage.

## Exclusions and representativeness
- Squares excluded from field survey if:
  - 90% or more of the area is sea, or
  - 75% or more urban land cover.
- Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; bias is expected to be small unless a region has unusually high sea/urban coverage.

## Estimation methods and uncertainty
- Estimates are produced as ratio estimates for each land class, weighting by the vegetative land area within each class.
- Land-class estimates are combined using weights that reflect the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features.

## Implications for analysis and monitoring
- Analyses must account for stratified sampling design; ignoring stratification can yield unrepresentative estimates and incorrect variation.
- Extrapolations to whole GB or regions rely on assumptions about excluded squares; potential biases are region-dependent.
- The need to handle differing country classifications and reporting structures when aggregating or comparing results.

## Data quality, governance, and metadata
- Data quality considerations include the need for appropriate transformation, cleaning, and the ability to verify metadata.
- Public sharing of underlying data is subject to confidentiality and representativeness considerations; governance processes are important to ensure comparability and transparency.
- Foundational references for methodology include Barr et al. (1993), Cochran (1963), and Efron & Tibshirani (1993).