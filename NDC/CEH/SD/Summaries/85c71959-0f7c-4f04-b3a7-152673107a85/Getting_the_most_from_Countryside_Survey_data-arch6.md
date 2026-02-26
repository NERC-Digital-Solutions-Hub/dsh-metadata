# Notes on the downloadable data

## Overview
- Document outlines how Countryside Survey (CS) field data are collected, sampled, processed, and presented to users.
- Emphasizes data representativeness, sampling design, and methodological caveats for analysis.

## Data confidentiality and geography
- Precise locations of CS survey squares are kept confidential by CEH to preserve representativeness.
- External users cannot be provided with location precision finer than 100 square kilometres.
- This confidentiality means users cannot identify whether specific survey squares fall within defined sub-areas below that threshold.

## Sampling design: two levels and non-random subset
- CS Field Survey data come from a sample of 1 km squares across GB.
- Two levels of measurement:
  - Whole square: general characterisations.
  - Within-square: detailed measurements (e.g., quadrats for vegetation, soils).
- Measurements are of varied types (binary to continuous).
- Not a random subset of all GB squares; the sampling is stratified by designated strata.

## Stratification and land classification
- Strata defined by the ITE Land Classification.
- Classification history:
  - Originally 32 classes; expanded to 42 in 1998 for Scotland-specific reporting.
  - Further revised to 45 classes due to Wales-focused reporting.
  - Each country has its own classification: England (21), Wales (8), Scotland (16).
- Estimates must account for stratification; unstratified estimates may be biased and misrepresent variation.

## Exclusions and representativeness
- Squares excluded from field survey if:
  - Area > 90% sea, or
  - > 75% urban (as measured on 1:250000 OS maps).
- Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares.
- If a region has a high proportion of sea/urban squares, bias risk rises; otherwise bias is likely negligible.

## Estimation methods and uncertainty
- Estimates are produced via ratio estimation (Cochran, 1963), using vegetative land area within each land class as weights.
- Land-class estimates are combined using the total vegetative land area as weights.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993).

## Data handling and implications for analysis
- Data include both square-level and within-square measurements; users should respect the dual sampling levels when modeling.
- Important to apply the stratified design and weighting when deriving inferences about land classes or regional patterns.
- Bootstrap-derived uncertainty should be incorporated into any inference about estimates.

## Practical guidance for data users (Data Support perspective)
- Be explicit about the sampling design and stratification when performing analyses or creating products.
- Use ratio-estimation weights and account for land-class areas to avoid biased estimates.
- Incorporate bootstrap-derived confidence intervals to reflect uncertainty.
- Recognize limitations due to confidentiality (100 km^2 precision) and exclusions (sea/urban-heavy squares) when interpreting geographic patterns.
- When communicating results, explain potential biases and the basis of regional or GB-wide estimates.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.