# Notes on the downloadable data

- Data confidentiality: precise CS survey square locations are kept confidential by CEH; external users will not be able to identify squares more precisely than 100 square km.
- Purpose of confidentiality: preserves representativeness of the wider countryside and prevents identifying squares that may fall within defined areas.
- Sampling design (two levels): field data come from a sample of 1 km squares in GB; measurements exist at both the whole square level and within-square features (binary and continuous variables).
- Stratified sampling: squares are not a random subset; selection is stratified within designated strata based on the ITE Land Classification. Classification has evolved over time (32 → 42 → 45 classes) with country-specific adjustments (England, Wales, Scotland).
- Representativeness caveat: estimates without accounting for stratification may be biased; official estimates are produced with stratified approaches.
- Exclusions: squares with more than 90% sea area or more than 75% urban area are excluded from field surveys; the remaining squares form the basis for GB estimates.
- Implications of exclusions: GB-wide estimates assume excluded land is similar to sampled land; bias is generally negligible unless a region has a high proportion of sea/urban squares.
- Estimation methodology: official estimates are derived using ratio estimates for each land class, weighted by the vegetative land area within each class.
- Weighting: land-class estimates are combined using weights equal to the vegetative land area of each land class overall.
- Uncertainty assessment: due to concerns about skewness, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani) from 1993 onward.
- Data provenance and references: Barr et al. 1993; Cochran 1963; Efron & Tibshirani 1993.