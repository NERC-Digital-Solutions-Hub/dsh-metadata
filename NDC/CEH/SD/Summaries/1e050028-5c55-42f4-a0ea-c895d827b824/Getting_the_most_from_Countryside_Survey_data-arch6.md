# Notes on the downloadable data

- Privacy and precision: The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify whether squares fall within defined areas with precision better than 100 square km.
- Sampling overview: CS field survey data come from a sample of 1 km squares in Great Britain. Each square is mapped, with measurements at two levels: the whole square and within-square features (e.g., quadrats for vegetation, soils). Measurements are varied (binary to continuous).
- Non-random sampling and stratification: The sample is not a random subset; it is stratified by the ITE Land Classification. Country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16). Classifications have evolved over time to support separate country reporting.
- Representativeness and exclusions: Not all GB squares were considered for field survey. Squares with more than 90% sea area or more than 75% urban area were excluded. Estimates for GB or regions assume similar vegetative land in excluded squares, which is generally small in extent, though bias could be an issue in regions with substantial sea/urban areas.
- Estimation methodology: Official land class estimates are produced using ratio estimates that weight vegetative land area in each class. Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods due to skewness in some features.
- Implications for use: Analyses should account for stratification, sampling design, and weights. Direct, unweighted estimates may be biased or misleading; use the provided weighting and bootstrap-based uncertainty measures where possible.
- Documentation and references: The notes reference methodological sources and key reports for further detail.

## Sampling Considerations in the use of Countryside Survey Data

- CS field survey data originate from a stratified sample of GB 1 km squares, with measurements at the square level and within-square features.
- The sampling design uses strata defined by the ITE Land Classification, with country-specific versions (England, Wales, Scotland) and changes over time for separate reporting.
- Not all GB squares are surveyed; exclusions are based on sea and urban coverage thresholds, and back-calibration assumes similarity in vegetative land in excluded squares for GB-wide estimates.
- Estimation and uncertainty:
  - Estimates are produced using ratio estimation with weights based on vegetative land area.
  - Bootstrap methods are used to derive standard errors and confidence intervals since 1998.
- Practical takeaways for data users:
  - Incorporate stratification and weights in analyses.
  - Utilize bootstrap-derived uncertainty measures rather than relying on unweighted or simplistic SEs.
  - Be mindful of potential regional biases if a region contains a high proportion of excluded squares (sea/urban).
  - Include metadata on sampling design, exclusions, weights, and uncertainty in any data products or dashboards.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.