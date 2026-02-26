# Notes on the downloadable data

- Purpose and scope
  - Describes Countryside Survey (CS) field data collected from a sample of 1-km squares in Great Britain.
  - Data include square-level measurements and within-square measurements (e.g., vegetation, soils) to characterize features at two levels.
  - Aimed at supporting environmental monitoring and policy evaluation with transparent data handling.

- Data confidentiality and access
  - Precise locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users cannot identify survey squares with precision finer than 100 square km.
  - This confidentiality limits the ability to map squares to defined areas exactly.

- Sampling design and representativeness
  - Sampling units are 1-km squares; measurements occur at the whole square level and within-square features.
  - The CS sample is not a random subset; it is stratified by the ITE Land Classification.
  - Land Classification details:
    - England: 21 classes; Wales: 8 classes; Scotland: 16 classes.
    - Classifications have evolved due to country-specific reporting needs (32 → 42 → 45 classes historically).
  - Exclusions:
    - Squares with >90% sea area or >75% urban area were excluded from field survey.
    - Estimates for GB or regions assume similarity between vegetative land in excluded and sampled squares; potential bias is small unless a region has a high proportion of sea/urban squares.
  - Implications:
    - Official estimates are produced using ratio estimation within land classes and weighted by vegetative land area.
    - Non-random, stratified design means care must be taken to account for strata when estimating variation.

- Estimation methods
  - Ratio estimates (per Cochrane, 1963) used for land-class estimates, weighted by vegetative land area within each land class.
  - Standard errors and confidence intervals (SEs/CIs) for some features estimated with bootstrap methods (Efron & Tibshirani, 1993) from 1998 onward to address skewness.
  - Two-tier measurements (square-level and within-square) provide detailed characterization while enabling proper weighting.

- Data quality and governance considerations
  - Metadata quality and accessibility can be a barrier when applying the data in monitoring frameworks.
  - Public sharing of underlying data is required, which aligns with open data practices but may pose governance and data management challenges.
  - Clear documentation of sampling design, stratification, and estimation methods is essential for correct interpretation and use.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques (2nd ed.).
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.

- Implications for monitoring framework authors
  - Understand and incorporate stratified sampling design and country-specific land classifications when analyzing CS data.
  - Apply appropriate weighting by vegetative land area and consider ratio-estimator approaches for land-class estimates.
  - Use bootstrap-based SEs/CIs to address potential skewness in feature estimates, especially after 1998.
  - Recognize confidentiality constraints that limit precise geographic mapping, which may affect spatially explicit policy evaluation.
  - Be prepared to address metadata gaps and ensure transparent data governance and provenance when integrating CS data into dashboards or reports.