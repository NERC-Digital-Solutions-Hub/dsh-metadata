# Countryside Survey 2007: Statistical Methodology for Stock and Change

## Executive Summary
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data and documents changes to estimation for CS 2007.
- Previous methods used minimal assumptions and were robust but produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.
- Modelling approaches for consistent estimation, demonstrated with Broad Habitat data, proved feasible and generally aligned with old method results within their inherent discrepancies.
- The 2007 CS adopts consistent, model-based estimation that uses all available data, yielding more precise estimates; updates to previous surveys may occur as new data are incorporated.
- Implementing modelling is technically challenging and computationally intensive; to practicality, an AR1 (autoregressive) mixed-model with bootstrap for standard errors was chosen to balance robustness and efficiency.
- The approach was tested on Broad Habitats and other data (including soil and plot-level data) and shown to produce consistent results; the new method is adopted for the 2007 CS.
- Limitations exist: model-based estimates rely on distributional assumptions; some data may require alternative handling (e.g., non-normal distributions). Bootstrap helps maintain robust standard errors.
- Overall, the modelling approach uses more information and respects data hierarchy, improving precision, but implies that estimates for earlier surveys may be revised as new data are added.

## Introduction
- This technical report outlines the sampling and analysis procedures for CS data, contrasting the previous methodology with the changes implemented for CS2007, and discusses limitations and implications.
- Full details of prior CS sampling and estimation are documented in Barr et al. (1993).

## Overview of Previous CS Methodology
- Sampling: CS field data come from a stratified sample of 1 km squares on a 15 km GB grid. Each selected square has square-level measurements and within-square plots, covering diverse data types. Land Classification stratifies squares; classifications evolved (32 → 42 → 45 classes) with separate national classifications for England, Wales, and Scotland.
- Estimation: Regional/national estimates are formed by means and standard errors for each Land Class, then combined (weighted by land area). Stock estimates used all data from a survey; change estimates used repeated measurements only, leading to potential inconsistencies.
- Bootstrapping: Significance testing for square-level data used bootstrap due to concerns about non-normality, providing robust standard errors and confidence intervals.

## Reasons for Modifications
- Inconsistencies arose because stock and change were derived from different data subsets; adjacent-survey changes did not guarantee consistency with non-adjacent changes.
- Three potential approaches to consistency were weighed; modelling (consistent estimation) was found feasible and robust, and the evidence supported moving to a modelling framework for 2007.

## Modelling Approach
- Modelling basics: Incomplete data techniques (mixed effects and repeated measures) allow consistent estimation by leveraging data from all surveys. This requires distributional assumptions about random effects and measurement errors; fixed effects yield stock across surveys, with random effects capturing variability by square and by survey.
- Square level data: View data as a repeated-measures problem within Land Classes. A mixed model uses fixed effects for Land Class means by survey and random effects for squares and repeated measures, with correlations across surveys.
- Plot level data: Within-square plots add complexity. Earlier analyses either summarized at square level or treated plots as independent. The modelling approach accommodates plot-level residuals and can be embedded in bootstrapping for standard errors.
- Model specification: General form for square level data is y_ijk = a_ik + s_ij + e_ijk, with a_ik fixed effects (land class means by survey), s_ij square random effects, and e_ijk repeated-measures residuals. Random effects are assumed normal with land-class-specific variances; repeated effect covariances are modeled and may vary by land class and survey.
- Reduction of parameters: Full models with many random effects are unstable and slow. Two practical reductions are adopted:
  - Variance parameters are common across surveys (σ_i).
  - Covariances follow an AR1 structure (correlation declines with time) to limit parameters.
- AR1 with bootstrap: The AR1 model reduces complexity to a manageable number of random parameters (three per survey per land class) and bootstrap estimation of standard errors provides robust inference when distributional assumptions are uncertain.
- Model testing – Broad Habitats: Analyses of 1984, 1990, and 1998 Broad Habitats showed that modelling produced consistent stock and change estimates, with differences from old methods generally within existing inconsistencies. The AR1 approach removed discrepancies present in older methods. Differences between old and new methods were small relative to old method discrepancies.
- Practical implementation: While some models are slow, the AR1 model with bootstrap was deemed feasible for large numbers of analyses, enabling automated application across many variables.

## Model Testing – Broad Habitats
- Old vs new methodology showed inconsistencies in stock and change when using previous approaches.
- Mixed-effects AR1 modelling produced consistent stock and change estimates across the three surveys, with changes computed as differences of consecutive stock estimates.
- Comparisons indicated that differences between methods were typically small and within the range of prior discrepancies; testing supported adopting the modelling approach for 2007 data.

## Limitations and Implications
- Computational demands: Model-based analyses with bootstrapping are more time-consuming; however, AR1 offers a practical balance of speed and robustness.
- Model choice sensitivity: Fixed-effect estimates are robust to moderate mis-specification of random effects; variances/covariances are more sensitive, so bootstrap is preferred for standard errors.
- Non-normal data: For highly non-normal variables (e.g., standing water), the new method may converge to local maxima; in such cases, the old method may be used for that variable to avoid biased estimates.
- Updating and consistency: Because analyses incorporate data from all surveys, estimates for earlier surveys may be revised as new data are added. This reflects improved information use and should be expected rather than treated as inconsistency.
- General benefits: The modelling approach better utilizes all information, respects data hierarchy (square and plot levels), and should yield more precise estimates, provided distributional assumptions are reasonable.

## Data Stewardship Implications
- Data governance: Model-based estimates rely on transparent, well-documented modelling choices (AR1 structure, distributional assumptions, random-effects specifications). Documentation and metadata must accompany data outputs to ensure auditability and reproducibility.
- Provenance and versioning: As new survey data are incorporated, past estimates may be updated. Version control of models, inputs, and outputs is essential to track changes and enable reproducible analyses.
- Data hierarchy and metadata: Clear metadata about the two-level sampling (square-level and plot-level) and Land Class definitions is critical for correct interpretation and reuse.
- Automated pipelines: The approach supports automated processing across many variables, but requires robust pipelines, logging, and validation checks to ensure consistent outputs across updates.
- Quality assurance: Employ bootstrap-based SEs for robust uncertainty quantification; keep parallel runs comparing old and new methods during transition to ensure traceability of changes.
- Access to methods: Provide access to model specifications (including AR1 parameters, variance assumptions) and validation results to data users for transparency and trust.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P. et al. (1977). Maximum likelihood from incomplete data via the EM Algorithm.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.