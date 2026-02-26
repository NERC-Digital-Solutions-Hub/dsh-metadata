# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users will not have precision better than 100 square km, so you cannot determine whether squares fall within defined area boundaries at finer scales.
- CS data consist of measurements from a sample of 1 km squares across Great Britain, with two levels of sampling: the square level and within-square (e.g., quadrats, vegetation, soils). Measurements vary from binary to continuous (areas, lengths).

- The sampling is not random but stratified within designated strata defined by the ITE Land Classification. Over time, the land-class classification has evolved (32 → 42 → 45 classes; England, Wales, Scotland have different class counts).

- Estimates derived from CS data without accounting for stratification may be unrepresentative and misstate variation.

- Some squares were excluded from field survey if they were >90% sea or >75% urban according to 1:250,000 OS maps. Official estimates apply only to squares meeting these criteria. In practice, regional GB estimates assume vegetative land in excluded squares resembles that in sampled squares; bias is typically negligible unless a region has a high share of sea or urban land.

- Official estimates use ratio estimation (Cochran, 1963) for each land class, weighting by the vegetative land area within each class. The land-class estimates are then combined using weights equal to the vegetative land area of each land class in the whole area.

- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.

- References:
  - Barr et al., Countryside Survey 1990 Main Report
  - Cochran, Sampling Techniques (2nd ed.)
  - Efron and Tibshirani, An Introduction to the Bootstrap

## Sampling Considerations in the use of Countryside Survey Data

- CS field survey data come from a stratified sample of 1 km squares, with within-square measurements; data include varied types from binary to continuous.

- The sampling design is not random; stratification is based on the ITE Land Classification, with country-specific revisions (England: 21 classes, Wales: 8, Scotland: 16).

- Estimates without correct stratification can be biased, and the variation around estimates may be misrepresented.

- Excluded squares (high sea or urban cover) mean CS data are representative only of included squares; extrapolation to GB or regional scales assumes similarity in vegetative land composition, a simplification that usually implies small bias unless regional sea/urban proportions are high.

- Weighting and methodology:
  - Estimates are derived as ratio estimates for each land class, considering vegetative land area within each sampled square.
  - Land-class estimates are combined using weights based on the vegetative land area of each class across the area.

- Uncertainty:
  - Bootstrap-based standard errors and confidence intervals are used to address skewness and provide more robust uncertainty estimates.

- Practical implications for GIS work:
  - Use aggregated land-class data and be mindful of the confidentiality limit on precise locations (no high-precision point mapping).
  - Apply stratification-aware analysis and incorporate bootstrap SEs when interpreting variability.
  - When aggregating to regional scales, account for potential biases due to excluded squares and country-specific classifications.