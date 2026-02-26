# Notes on the downloadable data

## Data confidentiality and location information
- Precise locations of Countryside Survey (CS) squares are held in confidence by UKCEH to preserve representativeness of the countryside.
- External users will not be able to identify survey squares with accuracy better than 100 square kilometres.
- This confidentiality limits the ability to determine whether squares fall within defined areas.

## Sampling design of Countryside Survey
- CS field data come from a sample of 1-km squares across Great Britain (GB), with measurements taken at two levels: whole square and within-square features.
- Data types range from binary to continuous (e.g., areas, lengths).

## Exclusion criteria and representativeness
- The sample is not a random subset; it is stratified within designated strata defined by the ITE Land Classification.
- Land Classification classifications vary by country (England: 21 classes, Wales: 8, Scotland: 16); classifications have evolved since 1990.
- Estimates must account for stratification; unadjusted estimates may be non-representative.
- Squares excluded from field survey: those with area more than 90% sea or more than 75% urban (per 1:250,000 OS maps).
- Official GB estimates assume excluded squares have similar vegetative land composition to sampled squares; biases are thought to be small except in regions with unusually high sea/urban areas.

## Estimation methods and uncertainty
- Estimates by land class are produced using ratio estimation, weighting by the vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated using the bootstrap method to address skewness.

## Practical implications for monitoring framework authors
- When using CS data, account for stratified sampling and area-based weighting to avoid biased inferences.
- Be aware of confidentiality constraints that limit precise geographic pinpointing.
- Use bootstrap-based uncertainty estimates for robust confidence intervals.
- Ensure metadata and data provenance are clear to facilitate data governance, quality assurance, and reproducibility.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.