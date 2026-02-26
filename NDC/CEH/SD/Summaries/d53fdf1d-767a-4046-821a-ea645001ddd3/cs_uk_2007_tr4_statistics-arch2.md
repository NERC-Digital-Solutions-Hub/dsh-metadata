# Statistical Methodology for Countryside Survey Data

## Executive Summary
- Describes the statistical methodology used for analysing Countryside Survey (CS) data and outlines changes implemented for CS in 2007.
- Previous methods were robust but produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.
- Modelling approaches using CS Broad Habitat data demonstrated that consistent estimation is feasible and robust; differences from old methods are generally small.
- The 2007 CS adopts a modelling approach to achieve consistency for both stock and change estimates.
- Modelling requires additional distributional assumptions; results, especially for small subsets, are validated by comparison with the previous methodology.
- The new approach leverages all available information, yielding more precise estimates; new survey data can also refine past estimates, though changes are typically small.
- Implementation is technically demanding and computationally intensive, but results are a markedly improved product.
- The AR1 modelling framework with bootstrap-based standard errors is favoured for square-level data; the approach is extended to plot-level data and validated against older methods.
- For Broad Habitats, the modelling approach resolves inconsistencies observed with the old methods; setup supports plotting and soil data analyses at both square and plot levels.
- The switch implies that estimates for any one survey may be revised as new data are added; this reflects a continual improvement approach rather than static re-interpretation.

## Introduction
- The report outlines sampling and analysis procedures for Countryside Survey data, reviews the previous methodology, and explains the reasons and details for changes made for CS in 2007, including implications and limitations.

## Overview of Previous CS Methodology
- CS field data come from a stratified sample of 1 km squares within a 15 km GB grid; data are collected at two levels: square-wide and within-square plots.
- Land Classification (ITE) stratifies squares; classifications expanded over time (GB: 32 → 42 → 45 classes) with national sub-classifications (England/Wales/Scotland).
- Estimation combined land-class means weighted by land area to produce regional/national estimates; means and standard errors were robust under minimal distributional assumptions and treated stock and change differently.

## Bootstrapping
- Prior to CS2000, significance relied on normality assumptions.
- CS2000 introduced bootstrapping to better handle non-normal data, providing more accurate significance estimates for square-level data.

## Reasons for Modifications to CS Methodology
- Stock and change estimates were historically inconsistent due to using all data for stock but only repeated data for change.
- Inconsistencies arose primarily from missing information across survey pairs (new squares added, some squares not recorded in earlier surveys).
- The goal was to provide consistent estimates across time and reporting scales; multiple approaches exist, but modelling offers a coherent solution for both square and plot data.

## Consistent Estimation

### 4.2 Modelling Basics
- Incomplete data necessitate models that jointly estimate stock and change across all surveys (mixed effects/repeated measures).
- Fixed effects capture stock/change values; random effects reflect sampling structure and within-square/within-land-class variation.
- Full models with many random parameters can be unstable; practical reduction of random effects is needed to obtain robust estimates.

### 4.3 Square Level Data
- Square-level data are modeled as repeated measures with fixed effects for land-class means across surveys and random square effects, plus within-square residuals that may be correlated across surveys.
- Mixed models formalize this structure; they provide consistent stock and change estimates when fitted properly.

### 4.4 Plot Level Data
- Plot-level measurements within squares require extending models to include plot-level random effects in addition to square-level effects.
- Both square- and plot-level forms can be embedded within bootstrapping to derive standard errors.

### 4.5 Model Specification
- General model: y_ijk = a_iK + s_ij + e_ijk, where a_iK are fixed effects by land class and survey, s_ij are square-level random effects, e_ijk are repeated-measures residuals.
- Random effects distributions are specified (e.g., normal), with variances/covariances that may vary by land class and survey.
- The large number of random parameters can be problematic; reducing parameters (e.g., common variance across surveys, AR1 covariance structure) improves stability and feasibility.

### 4.6 Model Testing – Broad Habitats
- Analyses showed that old methods produced inconsistencies in stock/change for several Broad Habitats.
- Fitting AR1-consistent mixed models to the three surveys (1984, 1990, 1998) yielded results without the previous discrepancies; changes are computed consistently as differences of stock estimates or via summed inter-survey changes.
- Comparisons indicated that differences between old and new estimates were generally small and within existing inconsistencies, supporting adoption of the modelling approach.

## Limitations and Implications
- Bootstrapped standard errors with AR1 models are robust, though computationally demanding.
- Fully parameterised models are slow; AR1 offers a practical balance between accuracy and run-time.
- Model assumptions (distributional forms) affect variance/covariance estimates; fixed-effects estimates (stock/change) are fairly robust to some mis-specification, but standard errors can be sensitive.
- Very non-normal data (e.g., standing water) can cause convergence issues; in such cases, historical (old) methodology estimates are retained.
- Using data from all surveys means past estimates are updated as new surveys are added; this aligns with the goal of continual improvement rather than static re-interpretation.
- Overall, the modelling approach uses more information and better represents data hierarchy, producing more precise estimates, with manageable practical limitations.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (1977); Efron, Tibshirani (1993); Scott (2002).
- Countryside Survey project information and methodology details are provided by CEH/NERC with Defra partnership funding.