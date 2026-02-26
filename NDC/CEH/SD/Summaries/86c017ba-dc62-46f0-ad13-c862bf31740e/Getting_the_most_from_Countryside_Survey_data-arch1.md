# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain, with measurements at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.). Measurements vary from binary to continuous.

## Confidentiality and geography
- Precise locations of CS survey squares are confidential. External users have a maximum precision of 100 square km, meaning you cannot determine whether squares fall within defined areas below this threshold.

## Sampling design and stratification
- The sample is not random; it is stratified by the ITE Land Classification. The classification has evolved:
  - Originally 32 classes
  - 1998: expanded to 42 classes (Scotland reporting)
  - 2007: expanded to 45 classes (Wales reporting)
  - England, Wales, Scotland each have their own country-specific classifications (England 21, Wales 8, Scotland 16).
- Estimates must account for stratification; ignoring it can yield biased variation estimates.

## Exclusions and representativeness
- Squares with >90% sea area or >75% urban area were excluded from field surveys.
- Estimates for GB or regions assume excluded squares are similar in vegetative land composition to sampled squares. This assumption introduces bias mainly in regions with substantial sea or urban areas.

## Estimation methods
- Official GB estimates are produced using ratio estimates (per land class) and are weighted by the vegetative land area within each land class.
- Since 1998, due to skewness concerns, standard errors and confidence intervals are estimated using bootstrap methods.

## Data usage considerations for analysts
- When analyzing CS data, apply the stratification and weighting by vegetative land area.
- Exercise caution with extrapolation to whole GB or large regions, especially if they contain many excluded squares.
- Be mindful of the country-specific land classifications when combining data across England, Wales, and Scotland.

## Data types and measurement details
- Within-square measurements provide additional detail on vegetation, soils, etc., using various variables (binary and continuous).

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.