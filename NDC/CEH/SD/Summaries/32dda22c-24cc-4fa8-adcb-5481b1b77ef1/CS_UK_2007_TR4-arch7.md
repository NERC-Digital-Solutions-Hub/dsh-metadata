# Countryside Survey 2007: Consistent Estimation Methodology

## Executive Summary
- Describes the statistical methodology for analyzing Countryside Survey (CS) data and details changes implemented for CS in 2007 to improve consistency between stock and change estimates.
- Previous methods used all data for stock but only repeated measurements for change, causing inconsistencies between stock and change estimates across surveys.
- Modelling approaches for consistent estimation (via data from all surveys) are feasible and robust, with differences from old methods generally small.
- The new modelling approach provides more precise estimates by using all available information; subsequent surveys can slightly adjust past estimates as more data become available.
- Implementation is technically challenging and computationally intensive due to iterative model fitting and the CS sampling complexity; however, results are a substantially improved product.
- The AR1 modelling framework, with bootstrap for standard errors, was adopted to balance accuracy and computational feasibility.
- Consistent estimation was tested with Broad Habitats data and other datasets (soil, plot level) and found feasible; the 2007 CS adopted the new methodology.

## Introduction
- The report outlines sampling and analysis procedures for CS data, reviews the previous methodology, and explains the 2007 changes aimed at consistent estimation.
- CS sampling involves a stratified 1 km square grid; measurements occur at two levels (square-wide and within-square plots) with varied data types.
- Land Classification (ITE) underpins stratification, with country-specific expansions (45 classes in CS2007: England, Wales, Scotland).

## Reasons for Modifications to CS Methodology
- Inconsistencies arise because stock estimates use all survey data while change estimates rely on repeated measurements.
- The shift to consistent estimates uses modelling to integrate data across surveys, addressing mis-matches and improving reliability.
- Several approaches were considered; modelling stock and change together via incomplete-data techniques offers consistency and efficiency, though it requires stronger distributional assumptions.
- The chosen modelling approach fits mixed/repeated-measures models to data from all surveys, yielding consistent estimates for both stock and change.

## Modelling Basics
- Incomplete-data techniques (e.g., EM algorithm, Bayesian/mixed models) enable consistent estimation across surveys but require distributional assumptions.
- CS uses a two-type parameter model: fixed effects (stock/change) and random effects (sampling variation).
- Mixed models help handle missing data and the hierarchical CS structure, enabling consistent stock and change estimates.

## Square Level Data
- Square-level data are treated as a repeated-measures problem within Land Classes.
- A mixed effects model is used: fixed effects capture land-class means across surveys; random effects capture square-level deviations and within-square repeated-measure correlations.
- This approach ensures stock estimates per survey and the implied changes are consistent.

## Plot Level Data
- Plot-level data within squares introduce a deeper hierarchical structure.
- Previous analyses either reduced data to square level or treated plots as independent; both had drawbacks.
- A mixed model framework can include square-level variation and plot-level residuals, with bootstrapping to derive standard errors.

## Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures error
- Random effects assumed normal with land-class-specific variances; within-land-class covariances vary by survey and land class.
- To manage complexity, random-effect parameters are reduced (e.g., AR1 structure, common variance components across surveys) to create a tractable model.
- Bootstrap is used to obtain standard errors, ensuring robustness to distributional mis-specifications.

## Model Testing – Broad Habitats
- Historically, Broad Habitat stock and change estimates showed inconsistencies when comparing stock-based changes to repeat-squares changes.
- Fitting AR1 mixed models to 1984, 1990, and 1998 data removed discrepancies; changes align with differences of successive stock estimates.
- Differences between old and new methods generally fall within old method inconsistencies; new method provides a coherent, consistent framework.
- Additional testing extended to soil (1978, 1998) and plot-level data, confirming the feasibility of consistent estimation beyond square-level data.

## Limitations and Implications
- The AR1 model with bootstrapped standard errors is robust for fixed effects but more sensitive for variance/covariance parameters; bootstrap mitigates this.
- Fully parameterised models are slow; AR1 offers a practical compromise between accuracy and computation for large-scale analyses.
- Distributions of random effects and potential non-normality can affect variance estimates; results suggest fixed-effect estimates are robust.
- In some very non-normal cases (e.g., standing water), the old method may be preferred if the new approach converges poorly.
- The modelling approach utilizes information from all surveys; past estimates may be updated as new data arrive, which is conceptually different from past reporting inconsistencies.
- Adoption improves precision and consistency but requires automation and careful model checking; results are more data-driven and harmonised across time.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).

## Additional Notes
- The CS2007 methodology is designed to produce robust, repeatable, map-ready estimates for stock and change, suitable for GIS-based data products, while acknowledging the increased computational demands and the need for ongoing data integration across surveys.