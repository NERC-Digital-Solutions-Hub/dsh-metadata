# Notes on the downloadable data

- Purpose and scope
  - Describes confidentiality, sampling design, measurement levels, and estimation methods for Countryside Survey (CS) data to aid appropriate use and interpretation.
  - Aims to preserve representativeness of the wider countryside while enabling external use under defined constraints.

- Data confidentiality and access
  - Precise locations of CS survey squares are kept confidential by CEH.
  - External users cannot identify square locations with precision finer than 100 square km.
  - This limitation prevents users from determining whether specific squares fall within defined areas below the threshold.

- Data collection and structure
  - CS field survey data come from a sample of 1 km squares across GB.
  - Measurements occur at two levels: characteristics of the square as a whole and features within the square (e.g., quadrats for vegetation, soils).
  - Variables range from binary to continuous (areas, lengths, etc.).

- Sampling design and representativeness
  - The CS sample is not a random subset of all GB squares; it is stratified within designated strata.
  - Strata are defined by ITE Land Classification; country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16).
  - Analyses that do not account for stratification may yield biased estimates of variation.
  - Some squares were excluded from field survey: those with more than 90% sea area or more than 75% urban area.
  - Official GB/regional estimates assume excluded squares are similar in vegetative land composition to sampled squares; bias is considered small unless a region has a high proportion of sea/urban squares.

- Estimation and uncertainty
  - Estimates by land class are produced using ratio estimation methods, weighting by the vegetative land area within each land class.
  - Land-class estimates are combined using weights equal to the total vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated via bootstrap methods to address skewness.

- Data provenance and references
  - Area calculations for squares rely on 1:250,000 OS map measurements.
  - Key references: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.

- Implications for data governance and use
  - Analysts must incorporate the stratified sampling design and weighting when analyzing CS data.
  - Public sharing of precise coordinates is restricted, affecting spatial analyses at fine scales.
  - Metadata quality and clear documentation (e.g., sampling design, exclusions, weighting) are essential for appropriate use and reproducibility.

## Sampling considerations in the use of Countryside Survey Data

- Two levels of sampling and measurement
  - Whole-square level and within-square level measurements; mixture of binary and continuous variables.

- Representativeness and limitations
  - The stratified sampling design and exclusions mean that estimates are representative only under the stated assumptions; region-level inferences require careful handling of design effects.

- Estimation approach
  - Ratio estimates by land class with area-based weights; bootstrap-based SEs and CIs to address skewness.

- Practical guidance
  - Use design-aware analysis (account for stratification and weights).
  - Be cautious when extrapolating to areas with high sea/urban coverage or when precise spatial placement is required given location confidentiality.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.