# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify squares with precision finer than 100 square km.
- CS field survey data comprise measurements from a sample of 1 km squares in Great Britain, with two levels of sampling: the whole square and within-square features. Measurements include both binary and continuous variables.

- Sampling design
  - The sample is not a random subset; it is stratified by Land Classes (ITE classification), with country-specific classifications: England (21 classes), Wales (8 classes), Scotland (16 classes).
  - Excluded squares: those >90% sea or >75% urban (based on 1:250,000 OS maps). Estimates for GB or regions assume excluded vegetative land is similar to sampled land; bias is generally negligible unless a region has a high proportion of sea/urban squares.
  - Since the sampling is stratified and not purely random, estimates that ignore stratification may be biased and have incorrect measures of variation.

- Estimation and uncertainty
  - Official estimates are produced as ratio estimates by land class, weighted by the vegetative land area of each land class.
  - Due to skewness in some features, standard errors and confidence intervals are estimated using bootstrap methods (since 1998).

- Implications for analysis and use
  - Analyses should account for the stratified sampling design and weighting.
  - When combining across land classes or regions, use area-weighted approaches and be mindful of the excluded-squares assumption.
  - Interpret area- and region-level estimates with consideration of potential biases in areas with high sea/urban coverage.

- Data access and references
  - Location confidentiality limits precise geospatial identification; metadata describes sampling design and weightings.
  - Key references: Barr et al. (1993), Cochran (1963), Efron & Tibshirani (1993).