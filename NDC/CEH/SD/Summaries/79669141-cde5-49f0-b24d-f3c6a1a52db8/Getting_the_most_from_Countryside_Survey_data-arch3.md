# Notes on the downloadable data

- Purpose: Clarifies data confidentiality, sampling design, and estimation methods for Countryside Survey (CS) data to support monitoring and analysis for environmental health policy decisions.

## Data confidentiality and access

- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot identify survey squares with precision better than 100 square kilometers.
- This limits the ability to determine whether squares fall within defined, restricted areas.

## Sampling design of Countryside Survey Data

- Field data come from a sample of 1 km squares across Great Britain (GB).
- Two levels of sampling:
  - Whole-square level: overall square characteristics.
  - Within-square level: detailed measurements (e.g., quadrats for vegetation, soils).
- Measurements span various types, from binary to continuous.
- Sampling is not a random subset; it is stratified by Land Classification (ITE classification).
- Country-specific classifications:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Original Land Classification evolved (32 → 42 in 1998; 45 in 2007) to accommodate separate country reporting; each country effectively has its own classification.

## Exclusions and representativeness

- Squares excluded from field survey if:
  - >90% sea area, or
  - >75% urban area (based on 1:250,000 OS maps).
- Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

## Estimation and uncertainty

- Estimates by land class are produced using ratio estimators, weighting by vegetative land area within each land class.
- Standard errors and confidence intervals (CIs) are estimated using bootstrap methods since 1998 (to address skewness in some features).
- Key references for methods:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) Bootstrap

## Practical implications for monitoring

- Analyses must account for stratified sampling and the GB-wide exclusion criteria.
- Metadata quality and data governance are crucial, given confidentiality and transformation steps required for use.
- When using CS data, ensure appropriate weighting, stratification, and bootstrap-derived uncertainty are applied to produce valid inferences.