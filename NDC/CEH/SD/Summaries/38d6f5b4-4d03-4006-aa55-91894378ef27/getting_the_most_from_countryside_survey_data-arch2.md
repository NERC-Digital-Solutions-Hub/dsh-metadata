# Notes on the downloadable data

- Purpose and scope
  - Describes Countryside Survey (CS) field data collected from a sample of 1-km squares in Great Britain.
  - Data include square-level measurements and within-square measurements (e.g., quadrats for vegetation, soils).

- Confidentiality and geographic precision
  - Exact square locations are kept confidential by UKCEH.
  - External users cannot identify whether squares fall within defined areas with precision better than 100 square km.

- Sampling design and structure
  - Two levels of sampling: whole square and within-square features.
  - Sample is stratified, not random, with strata defined by the ITE Land Classification.
  - Land Classification evolution:
    - Originally 32 classes; expanded to 42 in 1998 for Scotland reporting.
    - Revised to 45 classes after Wales-only reporting; now England (21), Wales (8), Scotland (16) have country-specific classifications.
  - Estimates ignoring stratification may be unrepresentative and misstate variation.

- Coverage and representativeness
  - Not all 1-km squares were surveyed; excluded if area was more than 90% sea or more than 75% urban (based on 1:250,000 OS maps).
  - Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; bias is usually small unless a region has a high share of sea/urban areas.

- Analytical methods and outputs
  - Estimates per land class are computed as ratio estimates, weighted by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness (Efron and Tibshirani).

- Implications for analysts
  - Must account for stratified sampling and apply appropriate weights when analyzing CS data.
  - Be cautious about extrapolation beyond surveyed squares or across regions with different land-class compositions.
  - Use bootstrap-based uncertainty measures for robust inference.

- References
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Cochran (1963): Sampling Techniques
  - Efron and Tibshirani (1993): An Introduction to the Bootstrap