# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at both the square level and within-square (using quadrats).
- Measurements vary from binary to continuous (e.g., areas, lengths).

## Data Structure and Sampling
- Two levels of sampling: whole square and within-square measurements.
- CS samples are not random; they are stratified by land-class, defined by the ITE Land Classification.
- Land Classification has evolved by country (England 21 classes, Wales 8, Scotland 16) for separate reporting; classifications differ across England, Wales, and Scotland.
- Some squares are excluded from field survey (area > 90% sea or > 75% urban), meaning official estimates are based on the remaining squares with the assumption that excluded areas are similar in vegetative land composition.

## Representation and Inference
- Estimates should account for stratification; ignoring it can lead to non-representative estimates and incorrect estimates of variation.
- Because the sampling is not entirely random and exclusions exist, estimators are implemented as ratio estimates by land class, weighted by the vegetative land area of each class.
- From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani).

## Exclusions and Bias Considerations
- Excluded squares (high sea/urban content) limit representativeness; bias is generally small unless a region has a high proportion of sea or urban squares.

## Privacy and Data Access
- Precise locations of survey squares are kept confidential to preserve representativeness; external users cannot identify whether squares fall within defined areas below a 100 square km precision.

## Practical Implications for Data Leaders
- Ensure metadata clearly documents: sampling design, stratification by land class, country-specific classifications, exclusion criteria, and the weighting scheme.
- Use design-aware analysis that incorporates stratification and weights; prefer ratio-estimate-based summaries and bootstrap-derived uncertainty.
- Be cautious about extrapolating to unrepresented squares or regions with many exclusions; document potential biases and caveats.
- Facilitate discoverability and reproducibility by providing clear references to the sampling framework and uncertainty methods.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.