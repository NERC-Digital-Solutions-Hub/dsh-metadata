# Notes on the downloadable data

## Overview
- Explains confidentiality and usage constraints for Countryside Survey (CS) data.
- Precise square locations are withheld; external users only have up to 100 square km precision.
- CS field data come from a sample of 1-km squares in Great Britain, with measurements at both the square level and within-square features.

## Sampling design and representativeness
- The CS sample is not a random subset; it is stratified within designated land classes defined by the ITE Land Classification.
- Country-specific classifications: England (21 classes), Wales (8), Scotland (16).
- Not all 1-km squares are surveyed; exclusions include squares that are more than 90% sea or more than 75% urban (per 1:250,000 OS maps).
- Estimates for GB or regions assume the vegetative land in excluded squares is similar to sampled squares; this bias is usually small unless a region has a high proportion of sea/urban squares.
- Official estimates use ratio estimation (Cochran, 1963) weighted by vegetative land area within each land class; since 1998, standard errors and confidence intervals are derived using bootstrap methods (Efron & Tibshirani, 1993).

## Data structure and measurements
- Field data include two levels of measurements:
  - Whole-square level (e.g., general square characteristics)
  - Within-square level (e.g., measurements from quadrats on vegetation, soils, etc.)
- Data types range from binary (yes/no) to continuous variables (areas, lengths, etc.).

## Data quality and interpretation considerations
- Analyses must account for stratification and weighting to avoid biased estimates.
- The sampling design affects representativeness; unweighted analyses may misstate variation.
- Bootstrap-based standard errors help address skewness and complex sampling when estimating uncertainty.

## Practical implications for data use
- When combining CS data with other datasets or creating products, incorporate:
  - Stratified design and area-based weights.
  - Confidentiality constraints limiting fine-scale localization.
  - Bootstrap-based uncertainty estimates for robust inference.
- Outputs should reflect the country-specific land-class classifications and the sampling frame limitations.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.