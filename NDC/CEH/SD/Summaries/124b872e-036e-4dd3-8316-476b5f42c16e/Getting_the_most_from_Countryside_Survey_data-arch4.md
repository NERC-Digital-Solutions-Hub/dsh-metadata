# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain.
- Measurements are taken at two levels: the whole square and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Data types include binary variables and continuous measures (areas, lengths).

## Location privacy and access
- The precise locations of CS survey squares are confidential to preserve representativeness.
- External users cannot identify squares with precision better than 100 square kilometers.
- Therefore, users cannot determine whether survey squares fall within specific, narrowly defined areas.

## Sampling design and representativeness
- Sampling is stratified by ITE Land Classification; country-specific revisions led to different class counts (32 → 42 → 45; 21 England, 8 Wales, 16 Scotland).
- The CS sample squares are not random; estimates rely on stratification and weighting to reflect land classes.
- Not all GB squares were surveyed: squares with >90% sea area or >75% urban area were excluded.
- Extrapolation to GB or regional scales assumes that vegetative land in excluded squares is similar to sampled squares; bias is generally small unless a region has high sea/urban proportions.

## Statistical estimation and uncertainty
- Estimates are produced using ratio estimation by land class, weighted by the vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated with bootstrap methods due to skewness in some features.

## Data structure and usage implications
- Data are organized around two levels of sampling (square and within-square) and a range of variable types (binary to continuous).
- For analysis, essential to apply the appropriate stratification, weighting, and extrapolation considerations to avoid biased inferences.
- Privacy constraints and the stratified, non-random design are important for reproducibility and interpretation, especially for regional or GB-wide estimates.

## Practical considerations for Data Leaders
- Ensure data analyses incorporate stratification, weights, and bootstrap-based uncertainty.
- Be mindful of the confidentiality boundary when sharing or disseminating location-based results.
- Maintain clear metadata on land classification definitions, temporal changes, and sampling exclusions to support robust governance and reuse. 

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.