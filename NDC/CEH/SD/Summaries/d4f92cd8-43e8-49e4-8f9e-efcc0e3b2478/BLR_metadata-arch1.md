# Bootstrapped Loess regression for soil depth profile comparison

- Purpose: Non-parametric comparison of soil depth profiles to detect significant differences across land use transitions without assuming a parametric distribution; suitable for potentially non-linear depth profiles and various soil types.

- Method (BLR approach):
  - Build an empty matrix to hold Loess-predicted values for depth profiles from bootstrapped samples.
  - Bootstrap by sampling from the union of data from the two land uses being compared; construct a confidence envelope representing the null hypothesis of no difference (P > 0.05).
  - Fit Loess predictions for the second land use alone and assess whether the curve lies outside the envelope to infer significance.
  - Compute an overall P value by normalizing test statistics across bootstrap samples and taking the percentile corresponding to the statistic from bootstrapping the second land use only.

- Implementation:
  - Written in R; includes two examples in BLR_example_code.R.

- Example dataset:
  - LUC.soil.data.csv demonstrates a land-use change from arable to Short-Rotation Coppice willow.
  - Study design: 3 plots per land use; 3 soil cores per plot; cores collected at 0 m, 1 m, and 1.5 m from sampling points; soil increments divided into 10 cm depths.
  - Variables cover land use, habitat, plot and core identifiers, depth numbering and increments, soil mass, soil carbon concentration, and soil carbon stock.
  - Dataset used to illustrate BLR outputs (Figure 1).

- Outputs:
  - Graphical output showing depth-profile comparisons (Figure 1).

- Context and references:
  - Data example from the ELUM project, funded by the Energy Technologies Institute (ETI).
  - References: R Core Team (2015) and Rowe et al. (2015).