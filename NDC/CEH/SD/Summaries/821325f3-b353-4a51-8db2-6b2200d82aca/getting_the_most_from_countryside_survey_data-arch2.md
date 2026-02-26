# Notes on the downloadable data

## Overview
- Describes how Countryside Survey (CS) field data are collected, stored, and used for environmental monitoring and analysis.

## Confidentiality and spatial precision
- Exact locations of CS squares are kept confidential.
- External users cannot identify whether survey squares fall within defined areas with precision better than 100 square km.

## Sampling design
- CS data come from a sample of 1-km squares across Great Britain.
- Each square is mapped with within-square measurements (e.g., quadrats for vegetation, soils).
- Two levels of measurements: square-level and within-square features.
- Sample is not a random subset; it is stratified by the ITE Land Classification.
  - Land classification evolved: 32 → 42 classes (1998) → 45 classes (2007), with country-specific classifications (England, Wales, Scotland).
- Not all squares were surveyed; exclusions were made for squares that were >90% sea or >75% urban (based on 1:250,000 OS maps).
- Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares, which may introduce bias if this is not true, though the excluded land area is typically small.

## Estimation and analysis method
- Official estimates are produced as ratio estimates weighted by the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani).

## Implications for analysts
- Analyses must account for stratification; ignoring it can yield unrepresentative estimates and incorrect variation.
- Extrapolation should consider the assumption that excluded squares resemble sampled squares; regional bias is most likely when regions have high sea/urban coverage.

## Practical notes for use
- Data are designed for consistent environmental health reporting and policy performance assessment over time.
- Data preparation should include appropriate weighting by vegetative land area and the bootstrap-based uncertainty estimates.

## References
- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Cochran (1963). Sampling Techniques.
- Efron & Tibshirani (1993). An Introduction to the Bootstrap.