# Consistent Estimation for Countryside Survey 2007

## Executive Summary

- Describes the statistical methodology used to analyse Countryside Survey (CS) data and outlines changes implemented for CS in 2007.
- Old methods used robust, minimal-assumption estimates but produced inconsistencies: stock estimates used all survey data while change estimates used only repeated measurements across survey pairs.
- Modelling approaches using Broad Habitat data demonstrated that consistent estimation is feasible and robust; differences from old methods were generally within existing inconsistency ranges.
- The 2007 CS adopts a modelling-based approach that uses all available information, yielding more precise (higher precision) estimates; subsequent surveys can update previous estimates, with changes expected to be small.
- Implementation is computationally intensive, requiring iterative model fitting and careful handling of CS’s complex sampling design.
- Validation shows new methods align with old results within their error bounds; especially for large Broad Habitat datasets, the shift to modelling improves consistency and efficiency.
- The AR1 modelling framework with bootstrap for standard errors is chosen for square-level data to balance stability, speed, and robustness; the approach is extended to plot-level data with appropriate random effects.
- A key implication is that estimated stock and change for a given survey may be revised as new data are incorporated from later surveys.
- The report provides a basis for adopting consistent estimation across CS outputs and outlines limitations and considerations for non-normal data and computational constraints.

## Introduction and Data Structure

- CS data derive from a stratified sample of 1 km squares across GB on a 15 km grid; measurements occur at two levels: square-level and within-square plot-level.
- Land Classification (ITE) underpins stratification; classifications have evolved (GB → country-specific classifications) to support separate reporting (England, Wales, Scotland).
- Data types range from binary to continuous measurements (areas, lengths), requiring flexible modelling to capture hierarchical structure.

## Estimation Methods: From Stock/Change to Modelling

- Previous approach: compute means and standard errors per Land Class, then combine to region totals; stock estimates used all data, change estimates used repeated data, leading to potential inconsistencies.
- Bootstrapping introduced (CS2000 onwards) to obtain significance without strict normality assumptions, especially for square-level data.
- Motivations for change: ensure consistency between stock and change across adjacent and non-adjacent surveys; address the mismatch introduced by incomplete (missing) information.

## Modelling Approach for Consistent Estimation

- Modelling uses mixed-effects/repeated-measures frameworks to handle incomplete data and the hierarchical sampling design.
- Fixed effects represent Land Class means over surveys; random effects capture square-level and plot-level variation and their correlations across surveys.
- To manage model complexity (many random parameters), the AR1 structure is adopted to reduce parameters while preserving essential correlation across successive surveys.
- The AR1 model assumes common within-land-class variance across surveys and first-order autoregressive correlations between successive surveys for repeated measures.
- Bootstrap is used to obtain robust standard errors, given potential distributional mis-specifications.

## Square-Level Data Modelling

- Data are treated as repeated measures within squares across surveys.
- Model: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects (land-class means by survey), s_ij are square-level random effects, and e_ijk are repeated-measures errors.
- Distributions: random effects assumed normal, with variances/covariances that may vary by land class; AR1 structure reduces parameters to a manageable set.

## Plot-Level Data Modelling

- Plot-level data within squares were previously handled inconsistently; the new approach uses hierarchical mixed models that incorporate both square-level and plot-level variability.
- Models can include an additional plot-level random effect; plots can be analyzed within the bootstrapping framework to obtain valid standard errors.

## Model Specification and Assumptions

- General square-level model: y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land-class means by survey) and random effects s_ij, e_ijk.
- Random effects distributions: normal with land-class-specific variances; covariances vary by land class and survey pair.
- AR1 simplifications reduce random parameter count, aiding stability and computational feasibility for large CS analyses.
- Bootstrap estimation of standard errors remains robust to some mis-specifications of random-effect distributions.

## Model Testing: Broad Habitats

- Re-analysis of seven Broad Habitats using three surveys (1984, 1990, 1998) showed that modelling eliminates the inconsistencies between stock and change seen with previous methods.
- Change estimates from the new models align with sums of inter-survey stock differences, and differences between old/new methods fall within old method discrepancies.
- Additional checks using soil and plot-level data confirmed feasibility and consistency of the modelling approach across scales.

## Limitations and Implications

- Computationally intensive; fully parameterised models are slow, so AR1 with bootstrap is preferred for large numbers of variables.
- Fixed-effects estimates (stock/change) are robust to some mis-specification, but variance/covariance parameters require careful handling; bootstrap mitigates potential mis-specification issues.
- Some non-normal data (e.g., very skewed freshwater standing water) may converge to local maxima with the new method; in such cases, the old method may be used for that variable.
- Adopting a consistent, model-based approach means estimates for earlier surveys may be updated as new data are incorporated; this reflects a shift from merely historical consistency to ongoing data integration.
- The approach is designed to be automated and scalable for large CS datasets; standard model choices (like AR1) are preferred to maintain consistency across analyses.

## References

- Barr et al. (1993) Countryside Survey 1990 Main Report
- Dempster, Laird, Rubin (1977) EM algorithm for incomplete data
- Efron, Tibshirani (1993) Bootstrap
- Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside
- Scott (2002) Maximum likelihood estimation using the empirical Fisher information matrix