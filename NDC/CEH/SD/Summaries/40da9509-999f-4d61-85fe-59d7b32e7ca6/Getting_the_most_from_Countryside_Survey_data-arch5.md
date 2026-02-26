# Notes on the downloadable data

- Location confidentiality: The precise locations of Countryside Survey (CS) field squares are kept confidential by CEH. External users will not be provided with location precision better than 100 square km, preventing identification of squares within defined areas.

- Data scope and structure: CS field survey data come from a sample of 1 km squares in Great Britain. Each selected square is mapped and surveyed at two levels—across the whole square and within-square measurements (e.g., quadrats for vegetation and soils). Measurements include a mix of binary and continuous variables.

- Sampling design: The sample squares are not a random subset of all GB squares; they are stratified within designated strata defined by the ITE Land Classification. The land classification has evolved over time:
  - Original: 32 classes
  - 1998: 42 classes (Scotland reporting considerations)
  - 2007: 45 classes (Wales reporting considerations)
  - Each country now has a separate classification (England: 21, Wales: 8, Scotland: 16)

- Representativeness and extrapolation: Official estimates use ratio estimates by land class, weighting by the vegetative land area within each class. Estimates for GB or regions are produced under the assumption that excluded vegetative land resembles that in sampled squares; this assumption introduces potential bias mainly in regions with substantial sea or urban areas, though the overall area of excluded land is small.

- Excluded areas in sampling: Squares with more than 90% sea area or more than 75% urban area were excluded from field surveys (details in Barr et al., 1993). This affects which squares are represented in the data.

- Estimation and uncertainty: Because of sampling design and potential skewness of some features, estimates are computed using ratio-estimation methods at the land-class level, then combined using vegetative land area as weights. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993).

- Data provenance and references: 
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.

## Sampling Considerations in the use of Countryside Survey Data

- Two-level sampling and measurement: Data include whole-square characterizations and within-square measurements (e.g., grid quad data). Measurements vary from binary to continuous, enabling both square-wide and within-square analyses.

- Stratification and non-randomness: The sampling is stratified by land class and not a simple random sample of all GB squares. Analysts must account for stratification (and country-specific classifications) to produce valid inferences.

- Implications for analyses: 
  - Analyses that ignore stratification may yield biased estimates and incorrect variability.
  - When using CS data, apply the provided stratification framework and weights (by vegetative land area in each land class).

- Representativeness caveats: Exclusions (sea/urban-dominated squares) and country-specific classification changes can affect regional representativeness. The assumption that excluded land is similar to sampled land is generally reasonable due to the small total excluded area, but may be problematic in regions with substantial sea or urban land.

- Uncertainty handling: Use bootstrap-based standard errors and confidence intervals as recommended, due to potential skewness in feature distributions.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.