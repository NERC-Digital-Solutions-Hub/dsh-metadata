# Notes on the downloadable data

- Overview
  - Explains how Countryside Survey (CS) data are collected, how to use them correctly, and related privacy and methodological considerations.

- Privacy and data confidentiality
  - Exact locations of CS survey squares are kept confidential by UKCEH.
  - External users cannot identify square locations with precision better than 100 square km.
  - This confidentiality means you cannot determine whether specific squares fall within defined areas.

- Sampling design and data structure
  - Field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Each selected square is mapped and contains within-square measurements (e.g., quadrats for vegetation, soils) and square-level measurements.
  - Two levels of sampling: whole squares and within-square features; measurements include binary and continuous variables.
  - The CS sample is not a random subset; it is stratified by the ITE Land Classification.
  - Land-class classifications are country-specific and have evolved:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Classifications changed over time (32 → 42 in 1998 for Scotland/UK reporting adjustments; further changes to 45 classes by 2007 for Wales/England) resulting in country-specific schemes.

- Representativeness and limitations
  - Estimates derived from CS data require accounting for stratification; unadjusted estimates may be non-representative with biased variation estimates.
  - Not all GB squares were surveyed; squares with >90% sea or >75% urban area were excluded (details in Countryside Survey 1990 Main Report).
  - Official GB estimates reflect only the included squares. To extrapolate to GB, it is assumed vegetative land in excluded squares is similar to included squares; this introduces potential bias, though typically small unless a region has high sea/urban coverage.

- Estimation methods and uncertainty
  - Land-class estimates are computed as ratio estimates (Cochran 1963), weighted by the vegetative land area in each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani 1993) to address skewness.

- Practical guidance for analysts
  - Apply stratification-aware weighting and area-based weights when deriving estimates.
  - Use bootstrap-derived standard errors for uncertainty assessment.
  - Be mindful of non-random, country-specific classifications and the exclusion of certain squares when interpreting GB-wide estimates.
  - Refer to the Countryside Survey 1990 Main Report for detailed exclusion criteria and methodology.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B., & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.