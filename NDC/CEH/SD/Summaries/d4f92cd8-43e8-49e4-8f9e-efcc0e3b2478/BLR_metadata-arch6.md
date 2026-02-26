# Bootstrapped Loess regression for soil depth profile comparison

## Purpose and scope
- Presents a non-parametric method to compare soil depth profiles and test for significant differences across land use transitions.
- Uses bootstrapped Loess regressions (BLR) to accommodate potentially non-linear depth profiles and avoid parametric distribution assumptions.
- Aims to be broadly applicable across different land uses and soil types.

## Method overview
- Build an empty matrix to hold Loess-predicted depth profiles derived from bootstrapped samples.
- Bootstrap by sampling from the union of data for the two land uses being compared; the resulting envelope represents the null hypothesis (no difference) at P > 0.05.
- Fit Loess predictions for the second land use only; if this line falls outside the bootstrap envelope, a significant difference is inferred.
- Compute an overall P value for the profile comparison by normalising test statistics across bootstrap samples and taking the percentile relative to bootstrap results for the second land use.

## Data structure and example dataset
- Example dataset: LUC.soil.data.csv, illustrating one land use change from arable to Short-Rotation Coppice willow, part of a UK study on bioenergy land use and soil carbon.
- Sampling design:
  - For each land use, 3 plots with 3 soil cores per plot.
  - Cores taken at 0 m, 1 m, and 1.5 m from the plot center in random directions (nine nested sampling locations per field).
  - Depth increments from 0–10 cm downward in 10 cm steps (e.g., up to 150 cm).
  - Analyses include soil carbon content (soil.C.per) and cumulative soil carbon stocks (soil.C.stock).
- Variables described in Table 1 include:
  - landuse: Original vs new land use (factor)
  - habitat: Habitat name for contextualizing land use change
  - n.plot, n.core: Indicate the number of plots and cores
  - depth.number, depth.increment: Depth indexing and increment in cm
  - soil.mass: Cumulative soil mass in the depth increment (g)
  - soil.C.per: Soil carbon concentration (%) in the depth increment
  - soil.C.stock: Cumulative soil carbon stock (g)

## Outputs and interpretation
- Graphical output (Figure 1) demonstrates the BLR results for comparing depth profiles of soil carbon content.
- The approach yields an overall P value for the comparison, enabling inference about significant differences in soil depth profiles between land uses.

## Implementation details
- Code is written in R.
- The workflow includes creating the prediction matrix, performing bootstrap resampling, fitting Loess curves for both profiles, and assessing significance against the bootstrap envelope.
- Example workflows and outputs are provided in BLR_example_code.R.

## Context and acknowledgments
- Example data derived from the ELUM project (Ecosystem Land Use Modelling & Soil Carbon GHG Flux Trial), funded by the Energy Technologies Institute (ETI).

## References
- R Core Team. R: A language and environment for statistical computing. 2015.
- Rowe, R.L. et al. (2015) Initial soil C and land use history determine soil C sequestration under bioenergy crops. GCB Bioenergy (in press).