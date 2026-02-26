# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares across GB.
- Measurements are taken at two levels: per square and within-square (e.g., quadrats for vegetation, soils, etc.).
- Variables vary from binary to continuous types and are used to describe square-level and within-square features.

## Location privacy and scope
- Precise locations of CS survey squares are confidential; external users cannot identify whether squares fall within defined areas with precision better than 100 square km.
- Consequently, it is not possible to determine exact square inclusion for some spatial queries at finer scales.

## Sampling design and data structure
- The CS sample squares are not a random subset of all GB squares; they are stratified within land-class strata.
- Two levels of sampling: whole square (for general characteristics) and within-square (for detailed features).
- During data collection, measurements are made at both levels to characterize square-level and within-square features.

## Stratification and land classification
- Strata are defined by the ITE Land Classification; country-specific revisions have occurred:
  - England, Wales, Scotland each have separate classifications.
  - Original classification had 32 land classes; by 1998 it expanded to 42; by 2007 Wales-only reporting led to 45 classes.
  - Current class counts: England 21, Wales 8, Scotland 16.

## Exclusions and representativeness
- Squares with area more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) were excluded from field survey.
- Official GB estimates assume vegetative land in excluded squares is similar to that in included squares; this may introduce bias, but is considered negligible unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty
- Land-class estimates are produced using ratio estimates (Cochran, 1963), weighting by the vegetative land area within each land class.
- After 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness concerns.

## Practical implications for GIS and analysis
- Analyses should account for stratification and weighting by vegetative land area to avoid biased estimates.
- Be cautious about extrapolating results to GB as a whole or to regions with substantial excluded areas.
- When integrating CS data with other GIS datasets, respect the 100 square km precision cap and the two-level data structure (square vs within-square).

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.