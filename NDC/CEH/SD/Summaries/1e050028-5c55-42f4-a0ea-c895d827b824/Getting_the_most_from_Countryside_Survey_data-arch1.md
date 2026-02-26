# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data are from a sample of 1 km squares in GB, with measurements at two levels: square-level and within-square (e.g., quadrats for vegetation, soils).
- Data types include binary and continuous variables; not a random subset but a stratified sample defined by the ITE Land Classification, with country-specific classifications (England 21 classes, Wales 8, Scotland 16; 45 classes total).
- A subset of squares was excluded from field surveys: those >90% sea or >75% urban, based on 1:250000 OS maps. Estimates for GB/regions assume excluded squares have similar vegetative land composition to sampled squares; bias is generally small except in regions with high sea/urban proportions.
- Official estimates use ratio estimates by land class, weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods.

## Confidentiality and location precision
- The precise locations of CS survey squares are kept confidential by CEH and are not disclosed to external users beyond a precision of 100 square km, preventing determination of whether a square falls within defined areas.

## Sampling design details
- Two measurement levels: whole square characterization and within-square features (e.g., quadrats).
- Sampling is stratified by the ITE Land Classification; country reporting requirements have driven updates to the classification over time.
- Excluded squares (sea/urban) limit representativeness to included squares; extrapolations assume similarity in vegetative land composition.

## Implications for analysis
- Analyses must account for stratification; ignoring it can yield non-representative estimates and incorrect variation.
- Potential bias from excluded squares is typically negligible unless a region has a large share of sea or urban land.
- Use bootstrap-based standard errors and confidence intervals (since 1998) to handle skewed feature distributions.
- When comparing GB or regional estimates, consider the weighting by vegetative land area and the stratified sampling design.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.