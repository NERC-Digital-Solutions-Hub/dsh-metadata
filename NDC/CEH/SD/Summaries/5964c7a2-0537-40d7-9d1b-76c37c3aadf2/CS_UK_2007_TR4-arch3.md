# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology for analyzing Countryside Survey (CS) data, with a focus on changes implemented for CS in 2007.
- Previously, stock estimates used all data from a survey, while change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling for consistent estimation (via a modelling approach) is feasible and robust, generally aligning with or improving upon prior estimates.
- The new approach uses all available information, producing more precise estimates; future surveys can improve past estimates, though changes are typically small.
- Implementing modelling is technically challenging and computer-intensive due to iterative model fitting and CS’s complex sampling; nonetheless, a more accurate product results from these methods.
- Modelling requires additional distributional assumptions; results, especially for small subsets, are validated by comparison with the old method.
- The methodology was adopted for the 2007 CS data, including application to Broad Habitats and plot-level data, and demonstrated feasibility for broader data types (e.g., soil data).

## Introduction
- This technical report outlines sampling and analysis procedures for CS data, reviews the previous methodology, explains why changes were made for 2007, and discusses limitations and implications.

## Sampling Overview
- Data come from a stratified sample of 1 km squares on a GB-wide grid; each square is mapped and measurements are taken at two levels: square-wide and within-square plots.
- Measurements span binary and continuous variables.
- Land Classification (ITE) classifications are country-specific (England, Wales, Scotland) with evolving class counts to support separate national reporting.

## Estimation and Consistency
- Old method: stock estimates used all square data; change estimates used only repeated measurements, leading to potential inconsistencies between stock and change.
- Several approaches to achieve consistency were considered; modelling was chosen for its ability to provide consistent and efficient estimates across stock and change for both square and plot data.
- The shift to modelling involves assumptions about data distributions and the correlation structure of repeated measures, balanced by robustness checks and bootstrapping.

## Modelling Basics and Data Structures
- Incomplete data techniques (e.g., EM algorithms, mixed models) allow consistent estimation across surveys, but require distributional assumptions.
- CS uses mixed effects/repeated measures models with fixed effects for stock by survey and random effects reflecting the sampling structure.
- Two data levels:
  - Square level data: treated as repeated measures within each land class; random square effects and correlated survey deviations.
  - Plot level data: additional plot-level residuals can be included to capture within-square heterogeneity; models can be embedded within bootstrapping.

## Square Level Data Modelling
- y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residuals
- Random effects are normally distributed with land-class-specific variance; correlations across surveys are modelled.
- A balance is sought between model complexity (number of random parameters) and stability/fit, given CS’s many land classes with limited per-class samples.

## Plot Level Data Modelling
- Plot-level data can be integrated by adding a plot-level random effect in addition to the square-level effect.
- Correlated survey residuals now pertain to plots rather than squares, reflecting the data’s hierarchical structure.
- Both square- and plot-level forms can be bootstrapped to obtain robust standard errors.

## Model Specification and Practicalities
- General model: y_ijk = a_ik + s_ij + e_ijk with distributions for s_ij and e_ijk.
- The full random-effects parameter set grows with the number of surveys; therefore, reduction strategies are used:
  - Assume random effects do not vary across surveys (common σ_i).
  - Use an AR1 (first-order autoregressive) structure for repeated-measures covariances to reduce parameters to three per land class.
- AR1 plus bootstrap is favored for robust standard errors, especially when fitting large numbers of analyses.

## Model Testing – Broad Habitats
- Historical Broad Habitat analyses (1984, 1990, 1998) exhibited stock-change inconsistencies with older methods.
- Modelling (AR1) produced consistent stock and change estimates; changes over periods matched sums of period changes as expected.
- Comparisons showed old vs new methods generally within previous error bounds; where differences occurred, they were small relative to overall uncertainty.
- Results supported adopting the modelling approach for 2007 CS and extending consistency checks to soil and plot-level data.

## Limitations and Implications
- Computational demands are high; fully parameterised models are slow, so a pragmatic AR1 approach with bootstrap is used for large-scale analysis.
- Fixed-effects estimates are robust to moderate mis-specification of random-effects distributions; variance/covariance parameters are more sensitive.
- Non-normal data can pose issues (e.g., freshwater standing water variable); in some cases, old methodologies may be retained for specific variables.
- A key implication: analyses across all surveys are interdependent; adding new data updates past estimates, so results are not strictly “in error” but refined with new information.
- The modelling approach is advantageous for precision and for reflecting data hierarchy; automated implementation is essential for large-scale monitoring programs.

## Implications for Monitoring Framework Authors
- Consider adopting consistent, model-based estimation to avoid stock-change inconsistencies and improve precision.
- Use hierarchical mixed models to reflect square and plot-level data structures; employ AR1 or similar parsimonious structures to manage parameter growth.
- Leverage bootstrap for robust standard errors, particularly with non-normal or complex data distributions.
- Be prepared for increased computational demands and implement automated workflows for large-scale analyses.
- Recognize that updating with new data can revise previous results; communicate these updates transparently.
- Ensure metadata and data governance practices support data sharing, reproducibility, and cross-survey comparability.