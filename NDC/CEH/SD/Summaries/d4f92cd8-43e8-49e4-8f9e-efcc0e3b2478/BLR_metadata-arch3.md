# Bootstrapped Loess regression for soil depth profile comparison

- Overview
  - Non-parametric method to compare soil depth profiles across land-use transitions using bootstrapped Loess regressions (BLR); avoids parametric distribution assumptions and is broadly applicable across land uses and soil types.

- Method
  - Build an empty matrix to hold Loess-predicted values for depth profiles based on bootstrap samples.
  - Bootstrap by sampling from the union of data for the two land uses; the envelope represents the null hypothesis of no difference (P > 0.05).
  - Fit Loess for the second land use; if the line lies outside the envelope, infer a significant difference.
  - Compute an overall P value by normalising test statistics across bootstrap samples and using the percentile from bootstrapping the second land use only.

- Data and Code
  - Implemented in R; includes two example scripts (BLR_example_code.R).
  - Example dataset LUC.soil.data.csv describes one land-use change (arable to Short-Rotation Coppice willow) from a UK study on soil carbon under bioenergy crops.
  - Nested sampling design: 3 plots per land use, 3 cores per plot, depths from 0 to 1.5 m in 10 cm increments; variables include landuse, habitat, n.plot, n.core, depth.number, depth.increment, soil.mass, soil.C.per, soil.C.stock.
  - Outputs include a graphical representation (Figure 1) of the depth-profile comparison.

- Outputs and interpretation
  - Provides a graphical envelope and the Loess-fit comparison to indicate significant differences in soil depth profiles.
  - Delivers an overall P value for the profile comparison.

- Relevance to Monitoring Frameworks
  - Offers a robust, non-parametric approach suitable for evaluating environmental health impacts of land-use policies on soil carbon depth profiles.
  - Supports transparent reporting and decision-making with reproducible code and outputs.
  - Highlights the need for well-documented sampling design and metadata to ensure data quality, comparability, and governance across monitoring programs.

- Limitations and considerations
  - Results depend on sample size, bootstrap design, and smoothing parameters; requires careful interpretation.
  - Reliable when depth-resolved data are consistently collected across land-use comparisons.

- Acknowledgments and references
  - Data drawn from the ELUM project; funded by the Energy Technologies Institute (ETI); references include Rowe et al. (2015) and R Core Team (2015).