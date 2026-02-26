# Bootstrapped Loess regression for soil depth profile comparison

## Overview
- Non-parametric method to compare soil depth profiles and test for significant differences across land use transitions using bootstrapped Loess regressions (BLR).
- No parametric distribution assumptions; aims to be broadly applicable across land use contexts and soil types.
- Includes a small example dataset and code to demonstrate BLR outputs.

## Data and Dataset Structure
- Implemented in R; two example files are provided (BLR_example_code.R) to illustrate the approach.
- Core procedure:
  - Create an empty matrix to store Loess-predicted depth profiles from bootstrap samples.
  - Bootstrap samples are drawn from the union of data for the two land uses being compared; envelopes represent the null hypothesis of no difference at P > 0.05.
  - Loess predictions for the second land use are tested against the envelope; outside the envelope indicates a significant difference.
  - A single overall P value is computed by normalising test statistics across bootstrap samples and taking the percentile relative to bootstrap of the second land use only.
- Example dataset details:
  - LUC.soil.data.csv represents one land-use-change transition (arable to Short-Rotation Coppice willow) from UK soil C studies (Rowe et al., 2015).
  - Sampling: 3 plots per land use; 3 soil cores per plot; depth increments of 0–10 cm, 10–20 cm, up to 1.5 m.
  - Measurements include soil carbon content and cumulative soil carbon stocks.
  - Variables include: landuse, habitat, n.plot, n.core, depth.number, depth.increment (cm), soil.mass (g), soil.C.per (%), soil.C.stock (g).
- Visual output: Figure 1 illustrating BLR results for soil C depth profiles.

## Methods and Reproducibility
- Bootstrapped Loess regression framework:
  - Loess-predicted values summarize depth profiles for bootstrap iterations.
  - Confidence envelopes are constructed from bootstrap samples under the null hypothesis of no difference.
  - Significance determined if second land use predictions fall outside the envelope.
- Outputs:
  - Normalised test statistics across bootstrap samples.
  - Overall P value derived from bootstrap distributions.
- Reproducibility:
  - Code is provided in R; references include R Core Team (2015) and the accompanying example script BLR_example_code.R.
  - Data provenance tied to the ELUM project and ETI funding; Rowe et al. (2015) cited for related soil C work.

## Example Dataset Details (Data Stewardship View)
- Dataset purpose: demonstration of BLR approach for soil depth-profile comparison during land-use transitions.
- Structure supports traceability from sampling design to analysis: explicit depth increments, plotting contexts, and land-use labeling.
- Metadata considerations:
  - Clear variable descriptions and units (e.g., depth.increment in cm, soil.mass in g, soil.C.per in percent).
  - Documentation of sampling scheme (plots, cores, depth increments) for proper interpretation and reuse.
- Provenance and credits:
  - Data originate from the ELUM project; acknowledged funding and related publications.
  - Include related references for traceability and methodological grounding.

## Outputs, Interpretation, and Stewardship Guidance
- Interpretation guidance:
  - If Loess-based predictions for the second land use lie outside the bootstrap envelope, infer a significant difference in depth profiles between land uses.
  - Use the overall P value to assess significance across the full depth profile.
- Stewardship considerations:
  - Maintain metadata-rich datasets with explicit sampling designs and depth increments.
  - Ensure versioning of code and data; preserve the reproducibility of the BLR analysis.
  - Provide or link to example datasets and code to facilitate reuse in similar cross-context soil-profile comparisons.

## References and Acknowledgments
- R Core Team (2015). R: A language and environment for statistical computing.
- Rowe et al. (2015). Initial soil C and land use history determine soil C sequestration under bioenergy crops.
- ELUM project; funded by Energy Technologies Institute (ETI).