# Notes on the downloadable data

- Purpose and scope
  - Documents the Countryside Survey (CS) field survey data handling to preserve representativeness and support analysis.
  - CS data come from a sample of 1 km squares in Great Britain, with measurements at both the square level and within-square features (binary and continuous variables).

- Confidentiality and geographic precision
  - Exact locations of CS survey squares are kept confidential by CEH.
  - External users cannot identify squares with precision finer than 100 square kilometers, limiting micro-level geographic identification.

- Sampling design and representativeness
  - The CS sample is not a random subset; it is stratified by land classification (ITE Land Classification).
  - Country-specific stratifications: England (21 classes), Wales (8), Scotland (16).
  - Some squares are excluded from field survey (areas >90% sea or >75% urban).
  - Estimates for GB or regions assume excluded squares are similar in vegetation composition to sampled squares; potential bias is small unless a region has a high share of sea/urban squares.

- Estimation methods and uncertainty
  - Official estimates are produced using ratio estimates by land class, weighted by the vegetative land area of each class.
  - Standard errors and confidence intervals are estimated using bootstrap methods (since 1998) to address skewness in some estimates.

- Implications for analysis and reporting
  - Analyses must account for stratification and area-based weighting to avoid biased inferences.
  - Caution with extrapolations to whole GB or regions if the sampling exclusions differ regionally.
  - Use bootstrap-derived uncertainty measures for confidence intervals.
  - Public sharing requirements for underlying data can be a barrier for some analyses; data governance and metadata quality are important.

- Data provenance and references
  - References include Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) The Bootstrap.