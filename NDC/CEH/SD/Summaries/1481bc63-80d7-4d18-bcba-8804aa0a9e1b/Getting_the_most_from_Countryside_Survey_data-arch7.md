# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness of the wider countryside.
- External users cannot be identified to a precision finer than 100 square kilometres.
- Consequently, users cannot determine whether survey squares fall within defined areas below this threshold.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and features are measured at two levels:
  - Whole square
  - Within-square (e.g., quadrats for vegetation, soils, etc.)
- Measurements vary from binary to continuous variables.

## Stratification and representativeness
- Squares are not a random subset; the sample is stratified within designated strata.
- Strata are defined by the ITE Land Classification.
- Land classification classifications vary by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Since estimates may be biased if stratification is ignored, analyses should account for this structure.

## Excluded areas and implications
- Squares with >90% sea or >75% urban area (per 1:250,000 OS maps) were excluded from field surveys.
- Official GB or regional estimates assume similarity in vegetative land between excluded and sampled squares; this is typically a small potential bias, except in regions with high sea/urban proportions.

## Estimation approach
- Estimates are produced using ratio estimates for each land class, weighted by the vegetative land area within each sample square.
- Land class estimates are combined using weights equal to the total vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness.

## Practical implications for GIS work
- When using CS data, incorporate stratification and area-based weighting to obtain unbiased estimates.
- Do not rely on unweighted, simple random-sample assumptions; account for country-specific land-class classifications.
- Be mindful of precision limits for square locations (maximum resolution of 100 sq km) when mapping or integrating with other spatial data.
- Use bootstrap-derived standard errors and confidence intervals for uncertainty assessment.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.