# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped, with measurements at two levels: the square as a whole and features within the square (e.g., vegetation, soils).
- Measurements include both binary and continuous variables.
- The sample is not a random subset; it is stratified by land classification, with country-specific versions (England: 21 classes; Wales: 8; Scotland: 16). Original classifications evolved from 32 to 45 classes over time.
- Estimates are produced using ratio estimation for each land class, weighted by vegetative land area in each class. Bootstrap methods (since 1998) are used to estimate standard errors and confidence intervals due to skewness concerns.

## Sampling design and classification
- The sampling design is explicitly stratified by the ITE Land Classification; sub-samples of squares are selected within strata.
- Not all GB squares were surveyed: any square with area more than 90% sea or more than 75% urban on 1:250,000 OS maps was excluded.
- Official GB or regional estimates assume vegetative land in excluded squares is similar to sampled squares; bias is generally small unless a region has high sea/urban coverage.

## Spatial confidentiality and data availability
- To preserve representativeness, precise locations of CS survey squares are confidential.
- External users will not have location precision finer than 100 square kilometers, limiting ability to determine whether squares lie within defined areas below that threshold.

## Analysis implications for GIS
- Data are best used at the level of land classes and vegetative land area rather than attempting precise square-level inference in restricted areas.
- When mapping or modeling, account for stratification by land class and apply the appropriate area-based weights.
- Use bootstrap-derived standard errors to convey uncertainty, particularly for skewed features.
- Be cautious about region- or area-specific biases due to excluded squares (e.g., high sea/urban proportions).

## Uncertainty and bias
- Stratification and non-random selection mean analyses must incorporate survey design (weights and stratification) to avoid biased estimates.
- Bias due to excluded squares is expected to be small overall but can be problematic in regions with substantial sea or urban coverage.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B., & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.