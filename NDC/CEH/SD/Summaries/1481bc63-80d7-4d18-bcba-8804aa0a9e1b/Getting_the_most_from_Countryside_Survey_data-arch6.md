# Notes on the downloadable data

## Data access and confidentiality
- To preserve representativeness, precise locations of CS survey squares are confidential and external users cannot identify squares with precision better than 100 square km.

## Data structure and sampling
- Countryside Survey field data come from a sample of 1 km squares in GB, with two levels of sampling: whole squares and within-square measurements.
- Measurements include binary variables and continuous variables (e.g., areas, lengths), collected from quadrats and other features within squares.

## Sampling design and classifications
- Squares are not a random subset; the sample is stratified within designated strata defined by the ITE Land Classification.
- Land Classification history: originally 32 classes; expanded to 42 in 1998 (Scotland reporting needs); to 45 classes in 2007 (Wales reporting needs).
- Each country now has its own classification (England: 21 classes, Wales: 8, Scotland: 16).

## Representativeness and exclusions
- Estimates must account for stratification; failing to do so yields non-representative estimates and incorrect variation.
- Not all GB squares were surveyed: squares with >90% sea area or >75% urban area were excluded.
- Official GB estimates assume excluded vegetative land is similar in composition to sampled squares; bias is typically negligible unless a region contains a high proportion of sea/urban squares.

## Estimation methodology and uncertainty
- Estimates by land class are derived using ratio estimation (Cochran, 1963).
- Weights are based on the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani, 1993) due to skewness.

## Practical implications for data use
- When analyzing CS data, incorporate stratification and area-based weighting.
- Be cautious with extrapolation to excluded squares; regional analyses should consider potential biases.
- Use bootstrap-derived uncertainty measures for comparisons and interpretation.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.