# Countryside Survey in 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and the changes implemented for CS in 2007 to achieve consistent estimation of stock and change.
- Previous methods were robust but produced inconsistencies between stock and change estimates; the new modelling approach uses all available survey data to produce consistent and more precise estimates.
- A modelling framework (mixed effects/repeated measures with AR1 structure) is adopted for square-level data, with extensions to plot-level data, implemented with bootstrapping for robust standard errors.
- While model-based, the approach requires additional distributional assumptions; results are validated by comparison with the old method, showing most differences fall within existing uncertainty.
- Computationally intensive; AR1 modelling provides a practical balance between robustness, precision, and feasibility for large numbers of variables.
- Implications include potential updates to past survey estimates as new data arrive, and broader data governance considerations (data sharing, metadata, and transparency) that align with the monitoring framework goals.

## Introduction
- Purpose: outline sampling and analysis procedures for CS data and justify changes made for CS2007.
- Background: review of CS2000 methods; emphasis shifts from single-survey emphasis to timelines spanning from the first survey to the present.
- Previous methodology used stock estimates from all data in a survey and change estimates from repeated measurements, causing inconsistencies.

## Sampling and Data
- CS data come from a stratified sample of 1 km squares on a 15 km grid covering Great Britain.
- Two hierarchical data levels:
  - Square level: measurements that relate to the whole square.
  - Plot level: measurements within each square (e.g., vegetation, soils).
- Stratification by Land Classification (ITE system), with country-specific adaptations (England, Wales, Scotland) leading to 45 Land Classes in CS2007.
- Estimation historically weighting land-class estimates by land area within each class.

## Estimation (Pre-2007)
- Stock estimates: means and standard errors for each Land Class, then area-weighted to regional/national totals.
- Change estimates: typically derived from repeated measurements (limited subset of data).
- Assumptions of independence across Land Classes; minimal assumptions about data distribution.
- Inconsistencies arose because stock used all data from a survey while change used only repeated measurements.

## Bootstrapping
- Significance testing for square-level data uses bootstrap (1000–10,000 resamples) due to concerns about normality.
- Bootstrapping provides distribution-free standard errors and confidence intervals, accommodating skewness in data.

## Reasons for Modifications to CS Methodology
- Goal: provide consistent estimates of stock and change over time and across non-adjacent surveys.
- Issues with old approach: discrepancies between stock and change estimates, especially when including unrepeated squares.
- CS2007 adopted modelling approaches that ensure consistency and leverage all available data, improving precision while acknowledging additional modelling assumptions.

## Modelling for Consistent Estimation
- Incomplete data techniques (mixed effects/repeated measures) used to handle missing information and ensure consistency across surveys.
- Modelling requires specifying fixed effects (stock and change values) and random effects (e.g., square or plot-level deviations, within-land-class variability).
- Two main model types discussed: square-level data and plot-level data; both rely on hierarchical mixed models.

### Square Level Data
- Treats each Land Class as a random sample of squares; uses repeated measures models (mixed models) with:
  - Fixed effects: land-class means across surveys.
  - Random effects: square-level deviations; within-square repeated-measures deviations across surveys.
- Aims to produce stock estimates by survey year and consistent change estimates from the model.

### Plot Level Data
- Plots within squares provide additional detail; earlier analyses treated plots inconsistently.
- Extended models include plot-level residuals (random effects) in addition to square-level effects.
- Both square- and plot-level models can be embedded within bootstrapping.

## Model Specification
- General model for square-level data:
  y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square random effects
  - e_ijk: repeated measures residuals
- Distributional assumptions:
  - s_ij ~ N(0, τ_i^2) varies by land class
  - e_ijk ~ N(0, σ_ik^2), with covariances between surveys
- Complexity: with K surveys, many random-effects parameters; full model can be unstable with many land classes and surveys.
- Practical reduction: AR1 (autoregressive) structure and common variance parameters to reduce random-effect parameters while preserving essential correlation structure.
- Bootstrap estimation of standard errors is recommended for robustness, given potential mis-specifications.

### Model Testing – Broad Habitats
- Historically, Broad Habitats (proportions per square) were estimated for multiple survey years (1984, 1990, 1998).
- Old method produced inconsistencies between stock and change; models (AR1 with bootstrap) provided consistent stock and change estimates across periods.
- Comparison showed most differences between old and new methods were within old method uncertainty bounds; changes were modest but improved consistency.

## Limitations and Implications
- Some variables (e.g., very non-normal freshwater standing-water data) can cause convergence issues; in such cases, old methods may be reported.
- AR1 modelling is robust for fixed effects but can be sensitive for variance-covariance parameters; bootstrap mitigates this.
- Fully parameterised models are slow; the AR1 approach balances robustness and computational feasibility for large-scale surveys.
- Adopting a consistent, information-rich modelling approach means past estimates may be revised as new data become available; results are not strictly identical across reporting occasions due to updated information.
- Benefits include improved precision, coherent treatment of hierarchical data (square and plot levels), and a standardized approach suitable for automation across many variables.
- Implications for data governance: data sharing, metadata quality, and transparency are critical to enable reproducible monitoring and evaluation.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (1977); Efron and Tibshirani (1993); Scott (2002).