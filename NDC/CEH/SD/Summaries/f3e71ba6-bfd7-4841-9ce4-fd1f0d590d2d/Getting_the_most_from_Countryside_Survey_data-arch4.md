# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km² squares across Great Britain.
- Data include measurements at two levels: the whole square and features within each square (e.g., quadrats for vegetation, soils).
- Data types range from binary to continuous measurements.

## Data access, confidentiality and metadata
- The precise locations of CS survey squares are confidential to protect representativeness.
- External users cannot identify whether squares fall within defined areas with precision better than 100 square kilometers.
- Metadata should reflect location precision limitations and confidentiality constraints.

## Sampling design and representativeness
- The CS sample is not a random subset; it is stratified by the ITE Land Classification.
- Country-specific classifications exist (England 21, Wales 8, Scotland 16; previously 32, then 45 overall).
- Analyses must account for stratification; estimates not adjusting for this may be biased.
- Not all squares were surveyed: squares >90% sea or >75% urban, by area, were excluded from field work.
- Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; bias is typically negligible except in regions with high sea/urban proportions.

## Estimation and uncertainty
- Land class estimates are produced as ratio estimates, weighting by the vegetative land area within each land class.
- Combined estimates across land classes use weights equal to the total vegetative land area of each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani).

## Practical implications for data leaders
- Data products should document:
  - The stratified sampling design and country-specific classifications.
  - The weighting scheme (area-based) and the use of ratio estimates.
  - The bootstrap approach used for uncertainty estimates.
  - The exclusion criteria for squares and the resulting representativeness limitations.
  - The confidentiality threshold (location precision limited to 100 km²) and its impact on spatial analyses.
- Data governance and metadata should:
  - Clearly state representativeness limits and potential biases.
  - Provide guidance on appropriate analyses (e.g., when to use weights, how to handle stratification).
  - Ensure discoverability of methodological notes and references (e.g., Barr et al. 1993; Cochran 1963; Efron & Tibshirani 1993).
- When integrating or disseminating this data, prefer aggregated outputs and documented methods over raw, highly precise location data to respect confidentiality while preserving analytical utility.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.