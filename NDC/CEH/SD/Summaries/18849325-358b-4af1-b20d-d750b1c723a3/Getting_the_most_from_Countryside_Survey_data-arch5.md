# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain. Measurements are taken at two levels: at the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Data are not a random subset; the sampling is stratified by land classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16).
- Estimates are produced using ratio estimates weighted by vegetative land area, and standard errors/confidence intervals are derived via bootstrap since 1998 due to skewness in some features.
- Measurements vary from binary to continuous (areas, lengths, etc.).

## Confidentiality, Access and Provenance
- To preserve representativeness, precise locations of CS survey squares are confidential. External users cannot identify whether squares fall within specified areas with precision better than 100 square km.
- Documentation notes how data are collected, mapped, and transformed, including the provenance of measurements and the processing steps prior to sharing.

## Sampling Design and Representativeness
- Field data come from a subset of GB squares, with some squares excluded from survey:
  - Exclusion criteria based on 1:250,000 scale maps: more than 90% sea or more than 75% urban.
- Official GB estimates assume vegetative land in excluded squares is similar in composition to sampled squares; this is generally considered a negligible bias, except in regions with unusually high sea or urban proportions.
- There are two levels of sampling: across squares (the primary sample) and within squares (detailed measurements).

## Data Processing, Quality Assurance and Sharing
- CS data are quality assured, cleaned, and transformed before sharing.
- Metadata, data formats, and accuracy/consistency standards are applied to ensure usability for downstream users.

## Statistical Methods and Estimation
- Estimates are produced by stratifying by land class and applying ratio estimation, weighted by the vegetative land area within each class.
- Standard errors and confidence intervals are computed using bootstrap methods (since 1998) to address potential skewness in feature estimates.

## Limitations and Assumptions for Users
- Analyses must account for stratification and weighting to avoid biased or unrepresentative results.
- Representativeness is contingent on the sampling design and the treatment of excluded squares; regional estimates may be biased if excluded areas differ markedly from sampled ones.
- The confidentiality constraint on square locations limits precise geographic pinpointing in external analyses.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.