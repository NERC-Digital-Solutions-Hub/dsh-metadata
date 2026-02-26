# Countryside Survey 2007 Methodology

- This technical report describes the statistical methodology used to analyse Countryside Survey (CS) data and outlines changes introduced for CS in 2007.

Executive Summary

- Previous CS methods were robust but caused inconsistencies: stock estimates used all data from a survey, while change estimates used only repeatedly measured data, leading to mismatches between stock and change.
- Modelling for consistent estimation using Broad Habitat data showed it was feasible and robust; differences from older methods were generally small.
- Consequently, a modelling approach for consistent estimation was adopted for CS in 2007.
- Modelling requires additional distributional assumptions; results, especially for small data subsets, were checked against the old method to ensure validity.
- The new approach uses all available information, yielding more precise estimates. As new surveys contribute information, previous survey estimates can be slightly updated; such changes are typically small.
- Implementing modelling is technically challenging and more computer time-intensive because it involves iterative model fitting rather than simple calculations. Despite difficulties, this yields a significantly improved product.

1. Introduction

- The report provides an overview of CS sampling and analysis procedures, reviews the previous methodology, and details the changes for CS in 2007.
- Full CS sampling/estimation details are documented in earlier work (Barr et al., 1993).

2. Overview of Previous CS Methodology

- 2.1 Sampling
  - CS field data come from a stratified sample of 1 km squares on a GB-wide 15 km grid.
  - Two sampling levels: square-level measurements (covering the whole square) and plot-level measurements (within squares).
  - Measurements vary from binary to continuous (areas, lengths).
  - Land Classification classification (ITE) underpins strata; classifications have evolved to country-specific versions (England, Wales, Scotland) for CS2000 and CS 2007.

- 2.2 Estimation
  - Regional/national estimates were formed by calculating means and standard errors for each Land Class, then combining them with area-based weights.
  - This approach made minimal assumptions about data distribution and assumed independence between Land Classes and total land.

- 2.3 Bootstrapping
  - Significance testing shifted to bootstrap methods due to concerns about normality, especially for square-level data.
  - Bootstrap allows non-normal data to provide accurate significance and confidence intervals.

3. Reasons for Modifications to CS Methodology

- Point estimates of stock and change in previous reports were seen as inconsistent by users because stock used all data while change used repeated measurements.
- Inconsistencies arise when comparing adjacent survey results with different data availability (missing squares, new squares, refusals).
- Three potential consistent estimation approaches were considered; a modelling approach was chosen because it can provide consistent and efficient estimates for both stock and change across square and plot data.

4. Consistent Estimation

- Modelling estimates use data from all surveys, creating consistent stock and change estimates and improving precision.
- Modelling requires assumptions about data distribution; results are validated against the old method, especially for small subsets.

4.1 Modelling Basics

- Incomplete data techniques (e.g., EM algorithms) enable fitting models across all surveys, but require distributional assumptions.
- Mixed effects/repeated measures models underpin consistent estimation; fixed effects relate to stock/change values, and random effects capture sampling variation.
- After fitting, fixed effects translate into stock and change estimates.

4.2 Square Level Data

- Data are treated as a random sample of squares within each Land Class; a repeated-measures (mixed) model is used.
- Fixed effects model the mean value per Land Class across surveys; random effects model square-level variation and survey-to-survey correlations.

4.3 Plot Level Data

- Plot-level measurements within squares require careful handling of hierarchical structure.
- Earlier CS analyses either aggregated to square level (loss of information) or treated plots as independent (potential bias).
- A mixed model can include both square-level random effects and plot-level residuals, embedded within bootstrapping.

4.4 Model Specification

- General model for square-level data: y_ijk = a_i_k + s_ij + e_ijk with fixed effects a_i_k, square random effects s_ij, and repeated-measures errors e_ijk.
- Random effects are assumed normal with land-class-specific variances; covariances across surveys are modeled.
- The full model has many random parameters; to keep the model tractable, simplifications are used.

4.5 Reducing Model Complexity (AR1 Approach)

- To keep models workable across many surveys and land classes, random effects are reduced by:
  - Assuming common SDs across surveys for a given land class (σ_i).
  - Adopting an autoregressive AR1 structure for repeated-measures covariances (covariances depend on adjacent surveys).
- This AR1 approach reduces random parameters to three per survey, regardless of the number of surveys.
- Fixed effects estimation is robust to some mis-specification of random effects; bootstrap remains robust for SEs.

4.6 Model Testing – Broad Habitats

- Historical Broad Habitat data (1984, 1990, 1998) were re-examined with the new modelling approach.
- Old method inconsistencies between stock and change were evident; the AR1 modelling approach produced consistent estimates where the differences were generally small and within old error bounds.
- Parallel analyses of soil and plot data supported the feasibility of consistent estimation across data types, leading to adoption of the new methodology for 2007.

5. Limitations and Implications

- Bootstrapped, model-based square-level analysis is computationally demanding, but fixed-effect estimates are robust to model variation.
- Fully parameterised models are slow; AR1 provides a practical balance between speed and accuracy for large numbers of analyses.
- Distributional assumptions affect variance estimates; bootstrap SEs mitigate this, but complex models or highly non-normal data may require transformations (with caveats about back-conversions to original scale).
- Very non-normal data (e.g., freshwater standing water) may cause convergence to local maxima; such results may revert to the old method.
- The modelling approach uses information from all surveys, potentially updating earlier survey estimates as new data come in; this means previous results can change slightly with new information.
- The approach aims to be automated and applicable to many variables, prioritising robust fixed-effect estimates over exactness of random-effect parameters.
- Practically, the adoption of a modelling framework means results should be interpreted as part of a continuous, updated time series rather than fixed snapshots.

6. References

- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002) – foundational works cited for methods and modelling approaches.

Notes

- Countryside Survey 2007 was funded by Defra and NERC, with results and methodology implemented to enhance consistency, precision, and comparability across surveys.