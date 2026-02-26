# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and highlights changes from previous surveys, especially for CS 2007.
- Old methods were robust but inconsistent: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches.
- Modelling for consistent estimation (the new approach) is feasible and generally robust; differences from old methods are small relative to existing inconsistencies.
- The modelling approach produces more precise estimates by using all available information but requires stronger distributional assumptions and validation, particularly for small data subsets.
- CS 2007 adopts modelling for stock and change, with additional checks against the old method to ensure reliability.
- Unlike previous methods, modelling can handle data from all surveys, improving precision and allowing improvements in previous survey estimates as new data are added.
- Implementation is technically challenging and computationally intensive; AR1 modelling with bootstrap for standard errors was chosen to balance robustness and practicality.
- The approach was validated on Broad Habitat data and soil data, showing feasibility of consistent estimates across square and plot levels; thus, the new methodology was adopted for CS 2007.
- There are implications for reporting: estimates for one survey can be revised upward with new data from subsequent surveys; this reflects updated information rather than errors.

## Introduction
- Purpose: provide an overview of CS sampling and analysis procedures, review previous methodology, and explain changes implemented for CS 2007.
- Emphasizes the shift from describing single surveys and changes to a timeline spanning from the first survey to the present.
- Full methodological detail of CS sampling and estimation is documented in earlier reports.

## Overview of Previous CS Methodology
- CS field data come from a stratified sample of 1 km squares across GB, with measurements at square level and within-square plots.
- Land Classification strata (ITE) evolve over time for England, Wales, and Scotland, affecting reporting classifications.
- Stock estimates combined across Land Classes using area-weighted means; change estimates used repeated measurements, creating potential inconsistency between stock and change.
- Bootstrapping was used to estimate standard errors and confidence intervals for square-level data due to non-normality concerns.

## Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock and change were derived from different data subsets; presenting results as point estimates could mislead when paired with their uncertainties.
- Several approaches to achieve consistency were considered; the chosen path uses modelling to estimate both stock and change consistently across surveys.
- Modelling promises improved efficiency (more precise estimates) and consistency, but requires stronger distributional assumptions and careful validation.

## Modelling Basics
- Incomplete data techniques (e.g., EM, mixed effects) enable consistent estimation across multiple surveys but require assumptions about data distributions.
- Mixed-effects/repeated-measures models are used to handle the hierarchical CS data structure (squares and plots) and to produce stock and change estimates that are internally consistent.
- Fixed effects represent land-class means across surveys; random effects capture square-level and plot-level variation and their correlations across surveys.
- Models must balance complexity (number of random parameters) with robustness and computational feasibility.

## Square Level Data
- Treat CS square-level data as a repeated-measures problem within each land class.
- Basic fixed effects: land-class means across surveys; random effects: square-level deviations and within-square survey deviations with possible correlations.
- A key issue is the large number of random effects relative to data per land class; simplifications are needed to keep models stable and computable.

## Plot Level Data
- Plot-level data within squares require extending models to include plot-level residuals (random effects) in addition to square-level effects.
- Previous analyses treated plots as independent or summarized to square level, which can bias standard errors or waste information.
- Bootstrapping can accommodate either square- or plot-level models, preserving robust uncertainty estimates.

## Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed land-class means per survey, s_ij are square random effects, and e_ijk are repeated-measures residuals.
- Random effects assumed normally distributed with land-class-specific variances; repeated-measures residuals have covariances that vary by land class and survey pair.
- With multiple surveys, many random parameters can overwhelm estimation; reducing complexity is necessary.

## (AR1) Model Reduction and Bootstrapping
- To reduce random-parameter complexity, assume:
  - Variance parameters do not vary across surveys (common σ_i for each land class).
  - Covariances follow an autoregressive structure (AR1) across successive surveys, reducing repeated-measures parameters to one per land class.
- This AR1 model reduces random parameters to a manageable number (three per survey) and stabilizes estimation across many surveys.
- Because variance/covariance estimates can be unstable, bootstrap standard errors (relying only on fixed effects) are recommended for robust inference.
- AR1 with bootstrap was tested to ensure consistent estimation and robustness.

## Model Testing – Broad Habitats
- Historical outputs included stock and change for Broad Habitats; previous methods showed inconsistencies between stock-derived changes and directly estimated changes from repeats.
- Modelling (AR1) across three surveys (1984, 1990, 1998) produced consistent stock and change estimates without the discrepancies observed in older methods.
- Differences between old and new methods were generally within the old method’s own inconsistencies; thus, the modelling approach is supported.
- Extended consistent analyses to soil data and plot-level data, confirming feasibility and encouraging adoption for 2007 CS.

## Limitations and Implications
- Bootstrapped, model-based analysis is computationally intensive but feasible; fixed-effect estimates (stock/change) are robust to some model variation.
- Fully parameterized models are slow; the AR1 approach strikes a balance between speed and robustness, enabling automated analysis across many variables.
- Distributional assumptions affect variance/covariance estimates; bootstrap can mitigate some risks, but complex models may still be sensitive to non-normality.
- Non-normal or highly skewed data (e.g., standing water) can cause convergence issues; in such cases, older methods may be used for those variables.
- Benefits include utilizing all information and properly representing data hierarchy, yielding more precise estimates.
- A notable consequence: estimates for earlier surveys can be updated when new data are added, which is conceptually different from prior inconsistencies and reflects new information incorporation.

## References
- Key references include prior CS methodology reports and foundational statistical texts on EM algorithms and bootstrapping; the modelling approach builds on mixed-effects, AR1 structures, and bootstrap procedures.
- Full citations are provided in the document’s reference list for Barr et al., Haines-Young et al., and methodological works by Dempster et al., Efron & Tibshirani, and Scott.