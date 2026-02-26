# Bootstrapped Loess regression for soil depth profile comparison

## Purpose and scope
- Non-parametric method to compare soil depth profiles and test for significant differences across land use transitions.
- Does not rely on parametric distribution assumptions; designed to be broadly applicable across land use types and soil contexts.

## How BLR works
- Create an empty matrix to store Loess-predicted values of a depth profile from bootstrapped samples.
- Bootstrap by drawing samples from the union of data from both land uses being compared, forming a null envelope representing no difference at P > 0.05.
- Fit Loess predictions for the second land use and check if it lies outside the confidence envelope to infer a significant difference.
- Compute an overall P value by normalizing test statistics across bootstrap samples and taking the percentile relative to bootstrap of the second land use only.

## Implementation details
- Implemented in R; code and examples provided (BLR_example_code.R).
- Outputs include a graphical representation of the depth-profile comparison (Figure 1).

## Example dataset and variables
- Dataset: LUC.soil.data.csv; demonstrates BLR using a land-use transition from arable to Short-Rotation Coppice willow, from a UK bioenergy LUC study.
- Sampling design: three plots per land use, three soil cores per plot, depth increments of 0–10 cm, 10–20 cm, etc., arranged in nine nested locations per field.
- Key variables (as described):
  - landuse: factor indicating 'original' vs 'new' land use.
  - habitat: context of soil cores.
  - n.plot: plot number.
  - n.core: core number within a plot.
  - depth.number: depth increment index (e.g., 1 = 0–10 cm).
  - depth.increment: depth increment in cm.
  - soil.mass: cumulative soil mass in the depth increment (g).
  - soil.C.per: soil carbon concentration (%).
  - soil.C.stock: cumulative soil carbon stock (g).
- Figure 1 provides a graphical example of BLR output for comparing depth profiles of soil carbon content.

## Outputs and interpretation
- Graphical output shows how the second land-use Loess curve compares to the bootstrap-derived envelope; outside the envelope indicates a significant difference.
- Overall P value summarizes the likelihood of observed differences under the null hypothesis of no difference between land uses.

## Data governance and reuse notes
- Example data sourced from the ELUM project (Ecosystem Land Use Modelling & Soil Carbon GHG Flux Trial), funded by the Energy Technologies Institute.
- Emphasizes reproducibility and applicability across contexts where non-linear depth-profile differences are of interest.

## References and acknowledgments
- References to R (R Core Team, 2015) and to Rowe et al. 2015 (bioenergy soil carbon study) for context and data origin.