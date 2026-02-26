# Notes on the downloadable data

## Overview
- Describes how Countryside Survey (CS) data are prepared, georeferenced, and analysed for monitoring environmental features in GB.
- Highlights sampling design, representativeness, data privacy, and methods used to estimate and quantify uncertainty.

## Data privacy and spatial precision
- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify survey squares with precision better than 100 square kilometres.

## Sampling design
- CS field survey uses a sample of 1 km squares across GB.
- Each selected square is mapped and measurements are taken at two levels: 
  - Characteristics of the whole square
  - Within-square features (e.g., quadrats for vegetation, soils)
- Measurements include both binary (yes/no) and continuous variables (areas, lengths).

## Stratification and country-specific classifications
- The sample is not random; it is stratified within designated strata defined by the ITE Land Classification.
- Land classification has evolved:
  - Original: 32 classes
  - 1998: Scotland reporting required, classification expanded to 42 classes
  - 2007: Wales reporting requirement led to 45 classes
- Each country uses a separate classification: England (21 classes), Wales (8), Scotland (16).

## Exclusions and representativeness
- Squares excluded from field survey if:
  - Area > 90% sea, or
  - > 75% urban (based on 1:250,000 OS map data)
- Official GB estimates are produced using ratio estimates by land class, weighted by vegetative land area in each class.
- Excluded squares are assumed to be similar in vegetative composition to included squares; bias is considered negligible overall, but may affect regions with many excluded squares (e.g., high sea/urban proportions).

## Estimation and uncertainty
- Since some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (since 1998; Efron & Tibshirani).

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.