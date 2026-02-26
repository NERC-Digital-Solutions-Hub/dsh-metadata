# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
- External users will not receive locations with precision finer than 100 square kilometres.

## Sampling Considerations in the use of Countryside Survey Data
- CS field survey data come from a sample of 1 km squares across Great Britain.
- Each selected square is mapped and measured at multiple levels: whole square and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Measurements vary from binary to continuous variables (e.g., areas, lengths).

## Sampling design and representation
- The CS sample is not a random subset of all GB squares; it is a stratified sample with sub-samples within designated strata.
- Strata are defined by the ITE Land Classification. The classification has evolved:
  - Originally 32 land classes.
  - 1998: expanded to 42 classes (Scotland reporting needs).
  - 2007: expanded to 45 classes (Wales reporting needs).
- Each country has its own classification: England (21 classes), Wales (8), Scotland (16).
- Estimates not accounting for stratification may be biased; proper weighting and stratification are essential for valid inference.

## Exclusions and representativeness
- Squares with >90% sea area or >75% urban area (per 1:250000 OS maps) were excluded from field surveys.
- Official GB estimates are computed under the assumption that vegetative land in excluded squares is similar to sampled squares.
- Bias from exclusions is generally negligible unless a region contains a large share of sea or urban squares.

## Estimation and uncertainty
- Estimates are produced using ratio estimation techniques for each land class, weighted by vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated with bootstrap methods (Efron & Tibshirani, 1993) due to skewness concerns.

## Implications for data governance and use
- Documentation should include: sampling design, stratification, exclusions, weighting, and uncertainty methods.
- Users must consider the non-random, stratified design and potential limitations in regions with high exclusion risk.
- Maintain transparency about privacy constraints and the implications for spatial analyses.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.