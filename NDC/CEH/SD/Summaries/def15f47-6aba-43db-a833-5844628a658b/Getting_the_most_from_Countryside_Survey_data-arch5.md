# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data cover a sample of 1 km squares in Great Britain, with measurements at both whole-square and within-square levels.
- To preserve representativeness, the precise locations of survey squares are confidential; external users cannot identify squares with precision finer than 100 square km.

## Sampling design and implications
- Two-level sampling: measurements characterize whole squares and features within squares (e.g., quadrats for vegetation, soils, etc.).
- Not a random subset; the sample is stratified by ITE Land Classification, with country-specific revisions:
  - England, Wales, Scotland each have their own classification schemes; England (21 classes), Wales (8), Scotland (16) in the current framework.
  - Classifications have evolved: 32 classes originally, 42 in 1998, 45 in 2007 due to country reporting needs.
- Some squares were excluded from field survey (area > 90% sea or > 75% urban, as per 1:250,000 maps).
- Estimates for GB or regions assume excluded squares are similar in vegetative land composition to sampled ones; bias is expected to be small except where a region has a high proportion of sea/urban squares.

## Estimation and uncertainty
- Official estimates are produced using ratio estimates for each land class, weighted by the vegetative land area within that class.
- Standard errors and confidence intervals have been estimated using bootstrap methods since 1998 due to skewness concerns (Efron and Tibshirani).

## Data governance and usage implications for Data Stewards
- Metadata must clearly document:
  - The two-level sampling design, stratification by country-specific land classifications, and the non-random nature of the sample.
  - Exclusion criteria and the representativeness limits of GB-wide or regional estimates.
  - The weighting scheme (vegetative land area per land class) and the bootstrap-based uncertainty estimates.
  - Evolution of land-class classifications across England, Wales, and Scotland (and how to handle cross-country analyses).
- Disclosure risk and privacy:
  - Precise locations are withheld; guidance should accompany data downloads on how this affects spatial analyses at finer scales.
- Reuse guidance:
  - Users should account for stratification and weights; analyses using the data should reference the underlying sampling and estimation methods.
  - Consider providing or linking to bootstrap SEs or replication procedures to aid robust uncertainty assessment.
- Documentation and provenance:
  - Include references to key methodological sources for sampling and estimation (Barr et al. 1993; Cochran 1963; Efron & Tibshirani 1993) to support reuse.
- Update and versioning:
  - Track changes in land-class classifications and country-specific schemes to ensure reproducibility over time.

## Practical considerations for data management
- Data are not a simple random sample; analysts must respect stratification and weighting when combining classes or regions.
- Location confidentiality constraints require careful handling in metadata and data-sharing processes.
- Data formats and interoperability considerations may require bespoke approaches due to the multi-level sampling design and classification changes.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.