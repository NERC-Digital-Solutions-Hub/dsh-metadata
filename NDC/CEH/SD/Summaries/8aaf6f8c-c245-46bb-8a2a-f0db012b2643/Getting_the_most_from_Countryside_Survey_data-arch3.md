# Notes on the downloadable data

## Purpose and scope
- Provides guidance on data availability, privacy, and sampling design for Countryside Survey (CS) field data used to monitor environmental features in Great Britain.
- Aims to support monitoring, scrutiny, and informing future decisions by clarifying limitations and methods.

## Data privacy and access
- Precise locations of CS survey squares are kept confidential to preserve representativeness.
- External users cannot identify survey squares with precision finer than 100 square kilometers.
- Public sharing of underlying datasets and metadata can be a barrier to data use and reproducibility.

## Sampling design and representativeness
- Data come from a sample of 1 km squares in GB, with two sampling levels: each square is mapped, and features within the square are measured (quadrats, vegetation, soils, etc.).
- The CS sample is not a random subset; it is stratified within designated strata defined by the ITE Land Classification.
- Land Classification changes over time and by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
  - Historical progression: originally 32 classes; 1998 revision for Scotland; 2007 revision for Wales leading to country-specific classifications.
- Exclusion criteria: squares with >90% sea or >75% urban area (based on 1:250,000 OS maps) were not surveyed.
- Practical implication: official GB or regional estimates assume excluded land is similar in composition to sampled land; bias is considered small unless a region has a high sea/urban proportion.

## Data processing, estimation and uncertainty
- Estimation method: ratio estimates are calculated for each land class, using the area of vegetative land in each square as weights.
- Post-1998 treatment of uncertainty: standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.
- Data handling requires careful transformation and weighting to ensure representative estimates across land classes and countries.

## Practical implications for monitoring and reporting
- When using CS data for monitoring, account for:
  - Stratified sampling design and country-specific land classifications.
  - Non-random selection and potential biases due to excluded squares.
  - Weighting by vegetative land area to derive land-class estimates.
  - Bootstrap-based uncertainty estimates for robust inference.
- Metadata quality and data governance are important considerations for transparency and reuse.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.