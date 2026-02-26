# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data are from a sample of 1 km squares across Great Britain, with additional measurements within each square.
- Data are designed to characterize squares and features within squares, using a mix of binary and continuous measurements.

## Spatial confidentiality and representativeness
- The precise locations of CS survey squares are kept confidential to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision better than 100 square kilometres.
- Consequently, users cannot determine if specific survey squares lie inside certain areas below the 100 km² threshold.

## Sampling design and levels
- Two levels of sampling: whole 1 km squares (for square-level characteristics) and within-square measurements (e.g., quadrats for vegetation, soils).
- Measurements are taken at both levels, yielding both square-wide and within-square data.

## Land Classification Stratification
- Sampling is stratified by ITE Land Classification.
- Land classification counts have evolved by country: England (21 classes), Wales (8), Scotland (16); historic versions included 32 classes (original) and up to 45 classes after revisions for country reporting.
- Estimates not accounting for stratification may be biased; appropriate analyses should incorporate stratification by land class.

## Exclusion criteria and implications
- Squares excluded from field surveys if their mapped area (1:250000 OS maps) is more than 90% sea or more than 75% urban.
- Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; bias is likely small overall but could be problematic in regions with high sea/urban proportions.

## Data processing and estimation methods
- Official estimates use ratio estimation (Cochran, 1963) for each land class, weighted by vegetative land area within each class.
- To address skewness, standard errors and confidence intervals are estimated using bootstrap methods (since 1998; Efron and Tibshirani, 1993).

## Implications for GIS map products
- When creating map-based data products, account for the stratified sampling design and potential non-randomness of the sample.
- Apply land-class weights if aggregating across classes; be mindful of exclusions and potential biases in regions with high sea/urban squares.
- Use bootstrap-derived uncertainty measures to convey uncertainty in estimates.
- Data provide square-level representativeness with within-square detail, suitable for depicting spatial patterns and feature distributions while acknowledging sampling limitations.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.