# Notes on the downloadable data

## Overview
- To preserve representativeness of the wider countryside, the precise locations of Countryside Survey (CS) field squares are kept confidential by CEH.
- External users will not be able to identify square locations with precision finer than 100 square kilometers.
- This confidentiality aims to prevent disclosure of exact survey locations while still enabling broader analysis.

## Data structure and sampling design
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and detailed measurements are taken at two levels: whole square and within-square.
- Measurements include a mix of binary (yes/no) variables and continuous metrics (e.g., areas, lengths).

## Sampling strategy and implications
- The CS sample squares are not a random subset of all GB squares; the sampling is stratified within designated strata.
- Strata are defined by the ITE Land Classification. The classification has evolved:
  - Originally 32 land classes.
  - In 1998, updated to 42 classes for Scotland separation.
  - In 2007, Wales-only reporting prompted a revision, resulting in 45 classes.
  - Consequently, England has 21 classes, Wales 8, Scotland 16.
- Analyses that ignore stratification may yield non-representative estimates and incorrect variation.
- Not all GB squares were considered for field survey; squares with >90% sea or >75% urban area were excluded.
- In practice, estimates for GB or regions assume excluded areas are similar in vegetative land composition to sampled squares; biases are expected to be small except in regions with high sea or urban proportions.

## Analytical methods and uncertainty
- Official GB land-class estimates are produced using ratio estimates (per Cochran, 1963), weighted by the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness in some features.

## Data governance and usage considerations for Data Stewards
- Documentation should clearly outline:
  - The confidentiality constraint on exact square locations (≤100 square km precision).
  - The two-level sampling design (whole square and within-square) and the stratification by Land Classification.
  - Exclusion criteria for squares (sea/urban thresholds) and the implications for representativeness.
  - The weighting and ratio-estimation approach used for land-class estimates.
  - The use of bootstrap techniques for uncertainty quantification since 1998.
- Metadata should flag potential biases and limitations arising from stratified sampling and excluded areas.
- Guidance for users should emphasize that analyses must account for stratification and area-based weighting to avoid biased conclusions.
- Consider versioning and updates to reflect any methodological or classification changes over time.
- Ensure references to primary sources are accessible for methodological transparency (Barr et al. 1993; Cochran 1963; Efron & Tibshirani 1993).