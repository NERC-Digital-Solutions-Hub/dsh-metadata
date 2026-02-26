# Notes on the downloadable data

- Location confidentiality and precision limits
  - Exact CS survey square locations are kept confidential by CEH to preserve representativeness.
  - External users cannot identify squares with precision finer than 100 square km; this prevents mapping to defined areas below that threshold.

- Sampling design and data structure
  - Field data come from a sample of 1 km squares across Great Britain.
  - Two sampling levels: whole squares and within-square measurements (e.g., quadrats for vegetation, soils).
  - Measurements vary from binary to continuous data.
  - Not a random sample; it is stratified with sub-samples within designated strata defined by the ITE Land Classification.
  - The Land Classification has evolved:
    - 1990: 32 classes
    - 1998: 42 classes (Scotland reporting required)
    - 2007: 45 classes (Wales reporting required)
    - England: 21 classes, Wales: 8 classes, Scotland: 16 classes

- Implications for analysis
  - Estimates derived without accounting for stratification may be unrepresentative and have biased variation estimates.
  - Analyses should incorporate the stratified design to obtain valid inferences.

- Exclusions and representativeness
  - Squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field surveys.
  - Official GB or regional estimates assume excluded squares have similar vegetative land composition as sampled squares.
  - Potential bias is generally negligible unless a region has a high proportion of sea or urban squares.

- Estimation methodology
  - Official land-class estimates are produced using ratio estimates (Cochran, 1963), weighted by the vegetative land area within each land class.
  - Weights are the vegetative land area of each land class as a whole.
  - From 1998, standard errors and confidence intervals are estimated using bootstrapping (Efron & Tibshirani, 1993) due to concerns about skewness.

- Practical considerations for analysts
  - Treat CS data as stratified survey data; apply appropriate ratio-estimator and area-weighted methods.
  - Use bootstrap-based uncertainty measures for robust CIs.
  - Be aware that precise square-level locations are withheld; use area- and class-level summaries for representativeness.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.