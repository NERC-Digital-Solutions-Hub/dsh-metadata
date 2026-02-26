# Notes on the downloadable data

- The exact locations of Countryside Survey (CS) field survey squares are kept confidential by UKCEH to preserve representativeness. External users will not receive precision better than 100 square km, so it is not possible to determine whether any survey squares fall within defined areas below this threshold.
- CS field survey data come from a sample of 1 km squares across Great Britain, with measurements at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils). Data types range from binary to continuous measurements.

## Sampling Considerations in the use of Countryside Survey Data

- The CS sample squares are not a random subset of all GB squares. The design is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16; originally 32, then 42, then 45 classes due to reporting needs).
- Estimates that do not account for stratification may be non-representative and misstate variation. The sampling frame excludes some squares based on 1:250,000 OS map area:
  - Excluded if more than 90% sea or more than 75% urban.
  - Therefore, field survey data are strictly representative of the included squares; extrapolation to all GB squares assumes similar vegetative land composition in excluded squares, which may introduce bias in regions with high sea/urban proportions.
- Official estimates are produced using ratio estimates (Cochran 1963) for each land class, weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani 1993) to address skewness in feature estimates.
- Measurement design:
  - Two levels of sampling: whole squares and within-square features.
  - Data include a variety of measurement types, from binary to continuous (e.g., areas, lengths).
- Practical implications for analysts:
  - Incorporate stratification and weights when estimating population characteristics.
  - Use bootstrap-derived SEs and CIs for robust inference, particularly for skewed features.
  - Be cautious when generalising results beyond the sampled and included squares; verify representativeness with respect to land classes and regional composition.

## Implications for Data Leaders

- Ensure metadata clarity on sampling design, classifications, and weighting to support correct use.
- Maintain transparency about exclusions and their potential impact on regional estimates.
- Provide guidance on appropriate analytic approaches that respect stratification, weighting, and bootstrap-based uncertainty.
- Facilitate data discoverability and governance around the confidential location data (location precision limits) to balance usability with protections.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., Fuller, R.M., Furse, M.T., Gillespie, M.K., Groom, G.B., Hallam, C.J., Hornung, M., Howard, D.C., Ness, M.J. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.