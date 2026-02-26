# Notes on the downloadable data

## Data confidentiality and access
- Precise locations of CS survey squares are kept confidential by UKCEH.
- External users cannot identify squares with precision better than 100 square kilometres.

## Sampling design and scope
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and measurements are taken at two levels: the square level and within-square features.
- Measurements span various data types, from binary to continuous.
- Squares are not a random subset; the sample is stratified by the ITE Land Classification.
- Land Classification counts by country: England (21 classes), Wales (8), Scotland (16). The classification evolved from 32 classes (original) to 42 (1998) to 45 (2007) due to separate country reporting.
- Excluded squares: those with more than 90% sea or more than 75% urban area (based on 1:250,000 OS maps).
- As a result, field survey data are representative only of the included squares. Extrapolation to GB or regions assumes vegetative land composition in excluded squares is similar to sampled squares; potential bias exists, particularly in regions with higher sea or urban proportions.

## Estimation and analysis implications
- Official estimates are produced using ratio estimates for each land class, weighted by the vegetative land area within each class.
- Because some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) since 1998.

## Practical governance and user guidance
- Metadata should emphasise the stratified sampling design, exclusion criteria, and weighting methods to ensure correct analyses.
- Users must account for the two-level sampling (square and within-square) and the non-random nature of square selection.
- Maintain awareness of confidentiality restrictions that limit precise location identification.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.