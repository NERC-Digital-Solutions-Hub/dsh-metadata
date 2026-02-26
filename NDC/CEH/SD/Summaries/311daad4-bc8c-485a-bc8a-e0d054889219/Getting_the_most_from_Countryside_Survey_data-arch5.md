# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain, with measurements at two levels: the whole square and features within the square.
- Data include a mix of variable types (binary and continuous) and reflect the sampling design rather than a simple random sample.
- Sampling is stratified by a Land Classification (ITE), which has evolved from 32 to 42 to 45 classes, with separate country classifications (England: 21, Wales: 8, Scotland: 16).
- Estimates are produced using ratio estimation by land class and are weighted by the vegetative land area within each land class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods.

## Location confidentiality and data sharing
- To preserve representativeness, precise locations of CS survey squares are confidential. External users are not provided with any location precision finer than 100 square kilometers, meaning discrete identification of squares within defined areas is not possible.

## Sampling design and representativeness
- Not a random subset of GB squares; it is stratified by land class with sub-samples within strata.
- Some squares were excluded from field survey: those with more than 90% sea or more than 75% urban area (based on 1:250,000 OS maps). Estimates for GB or regional scales assume excluded squares are similar in vegetative composition to sampled squares; bias is likely small except in regions with unusually high sea/urban square proportions.
- Official estimates rely on ratio estimation by land class and are weighted by vegetative land area; bootstrap is used for uncertainty estimation due to potential skewness.

## Implications for data users and stewards
- Analyses must account for stratification, sampling design, and weighting; results are not directly generalizable without these adjustments.
- Users should review documentation on land classification schemes, country-specific classifications, and inclusion/exclusion criteria to correctly interpret estimates and uncertainties.
- Data stewardship considerations include maintaining metadata that clearly communicates: sampling design, strata definitions, exclusion criteria, location masking, estimation methods, and bootstrap-based uncertainty.

## Documentation, metadata, and references
- Key methodological references:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap
- Metadata should disclose: sampling levels (whole square and within-square), stratification, country-specific land classes, exclusion rules, estimation approach (ratio estimates with area weights), and bootstrap uncertainty estimates.

## Practical guidance for data management and reuse
- When sharing or publishing CS-derived datasets, explicitly document:
  - The two-level sampling design and how within-square measurements were collected
  - The stratification scheme and country-specific land classifications
  - Exclusion criteria and their impact on representativeness
  - The weighting scheme (vegetative land area) and the use of bootstrap for uncertainty
  - The confidentiality constraint on square locations (100 km2 precision)
- Provide users with reproducible procedures for estimating values that respect stratification and weighting, and clearly denote any region- or class-specific caveats.