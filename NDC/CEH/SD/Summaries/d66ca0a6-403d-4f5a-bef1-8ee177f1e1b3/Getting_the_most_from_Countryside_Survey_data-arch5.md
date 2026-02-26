# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain (GB).
- Data include measurements at two levels: whole squares and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Measurements vary from binary to continuous (areas, lengths).

## Confidentiality and spatial disclosure
- To preserve representativeness of the countryside, precise square locations are kept confidential by CEH.
- External users will not receive location precision better than 100 square kilometres; users cannot identify whether any survey squares fall within defined areas below this threshold.

## Sampling design and representativeness
- The CS sampling is not a random subset; it is stratified by ITE Land Classification with sub-samples within strata.
- Land Classification evolution:
  - Original: 32 classes
  - 1998: 42 classes (Scotland reporting requirements)
  - 2007: 45 classes (Wales reporting requirements)
  - Result: separate country classifications (England 21, Wales 8, Scotland 16)
- Some GB squares were excluded from field survey:
  - Excluded if more than 90% sea or more than 75% urban (based on 1:250,000 OS map area)
- Estimation approach:
  - Official GB estimates are based on ratio estimates by land class, weighted by vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods.

## Implications for analysis and data usage (Data Steward perspective)
- Users must account for stratified sampling and weighting when analyzing CS data to avoid biased estimates.
- Analyses should consider the two-level sampling structure (square and within-square measurements).
- When combining regions or countries, ensure the country-specific land classifications and reporting changes are respected.
- Be aware of exclusions; estimates for regions with many excluded squares may be biased if vegetative land composition differs.
- Metadata should document the confidentiality constraint on locations, the stratification scheme, the exclusions, and the bootstrap-based uncertainty estimates.

## Documentation and references
- Key references for methodology and sampling:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.