# Notes on the downloadable data

## Overview
- Describes how Countryside Survey (CS) data are collected, processed, and what is available to external users.
- Signals confidentiality of precise survey-square locations (maximum precision disclosed is 100 square km).
- Outlines sampling design, estimation methods, and references underpinning the data analysis.

## Sampling design and data structure
- Field survey data come from a sample of 1 km squares across Great Britain.
- Each selected square is mapped and measured at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.).
- Measurements are varied, including binary and continuous variables.
- The sample is not a random subset but is stratified within designated strata.

## Representativeness and scope
- Stratification is defined by the ITE Land Classification, with country-specific classifications evolving over time (32 → 42 → 45 classes; 21 England, 8 Wales, 16 Scotland).
- Estimates that ignore stratification may be biased; analyses should account for the sampling design.
- Not all GB squares were surveyed: squares >90% sea or >75% urban areas were excluded.
- Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; this may introduce bias mainly in regions with high sea/urban square proportions.

## Estimation methods and uncertainty
- Land-class estimates are produced using ratio estimation, weighted by the vegetative land area within each land class.
- Weights are applied to aggregate class estimates to the national level.
- From 1998 onward, standard errors and confidence intervals are derived using bootstrap methods due to concerns about skewness.

## Data confidentiality and access
- Precise square locations are kept confidential to preserve representativeness and prevent misuse.
- External users cannot identify whether specific squares fall within defined areas below the 100 square km precision threshold.

## Implications for data leaders
- Ensure data products include clear documentation of:
  - Sampling design, stratification, and exclusion criteria.
  - Weighting schemes and how class estimates are aggregated.
  - Variance estimation approach (bootstrap) and associated confidence intervals.
  - Confidentiality constraints and their impact on spatial analyses.
- Provide metadata that supports proper interpretation and reuse, including limitations due to stratification and excluded areas.
- Facilitate discoverability and updates by aligning data governance with the sampling framework and representativeness considerations.
- Be mindful of the potential biases when applying GB-wide or regional analyses to areas with higher proportions of sea or urban land.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.