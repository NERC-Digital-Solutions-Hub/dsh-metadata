# Bootstrapped Loess regression for soil depth profile comparison

- Scope and purpose
  - Non-parametric approach to compare soil depth profiles across land-use transitions.
  - Tests for significant differences without assuming any parametric distribution; aims to be broadly applicable across land use and soil types.
  - Demonstrates the BLR method with a small dataset to illustrate outputs.

- How BLR works (method overview)
  - Uses bootstrapped Loess regressions to compare depth profiles.
  - Creates an empty matrix to store Loess-predicted values from bootstrap samples.
  - Bootstraps from the union of data from the two land uses to form a null envelope representing no difference (P > 0.05).
  - Fits Loess for the second land use alone; if the fitted line lies outside the envelope, a significant difference is inferred.
  - Overall P-value is computed by normalizing test statistics across bootstrap samples and taking the percentile corresponding to bootstrap results for the second land use only.

- Implementation and outputs
  - Code written in R; two examples provided in BLR_example_code.R.
  - Process yields a graphical output and a statistical assessment of depth-profile differences.
  - Example includes a figure illustrating BLR results (Figure 1 in the document).

- Example dataset (LUC.soil.data.csv)
  - Represents a single land-use transition: arable to Short-Rotation Coppice willow.
  - Part of a UK study on bioenergy land-use change and soil carbon (Rowe et al., 2015).
  - Sampling design: 3 plots per land use; 3 soil cores per plot; depth sampling at 0, 1, and 1.5 m in random directions; soil cores divided into 10 cm increments.
  - Variables described: landuse, habitat, n.plot, n.core, depth.number, depth.increment, soil.mass, soil.C.per, soil.C.stock.
  - Graphical output accompanies the dataset (Figure 1).

- Practical notes for GIS applications
  - BLR outputs include envelopes and significance evidence suitable for incorporation into map-based reports and visualizations.
  - Requires depth-profile data with consistent depth increments and adequate replication to generate robust bootstrapped envelopes.
  - Useful for communicating whether soil depth features differ significantly across land-use transitions in spatial analyses.

- Acknowledgments and references
  - Data reference: ELUM project (funded by the Energy Technologies Institute).
  - References: R Core Team (R language) and Rowe et al. (2015) on soil carbon and land-use history.