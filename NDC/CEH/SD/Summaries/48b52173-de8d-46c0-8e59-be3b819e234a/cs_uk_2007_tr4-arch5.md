# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used for Countryside Survey (CS) data analysis and details changes implemented for CS in 2007.
- Previous methods used all data for stock estimates but only repeated measurements for change estimates, causing inconsistencies between stock and change.
- Modelling approaches provide consistent estimation for both stock and change by using all available data; differences from old methods generally fall within previously inherent inconsistencies.
- Adoption of modelling requires additional distributional assumptions; results are validated by comparison with prior methods, especially for small data subsets.
- Modelling yields more precise estimates and allows past surveys to be updated when new data are added, though changes to past estimates are typically small.
- Implementation is technically challenging and computationally demanding, prompting the use of a standard AR1 modelling approach with bootstrap for robust standard errors; results are compared against the old method as a check.

## 1. Introduction
- Technical report outlining sampling and analysis procedures for CS data.
- Reviews previous CS methodology and explains reasons and details for 2007 methodological changes.
- Discusses limitations and implications of the new approach.

## 2. Sampling and Data Overview
- CS data are collected from a stratified sample of 1 km squares on a GB-wide 15 km grid; two levels of sampling within each square (square-wide measurements and within-square plots).
- Data types range from binary to continuous (e.g., areas, lengths).
- Land Classification (ITE) classifications evolved for country-specific reporting: 45 classes in 2007 (England 21, Wales 8, Scotland 16), with national classifications closely related to the GB origin.

## 2.2 Estimation
- Old approach: compute means and standard errors for each Land Class, then combine by land-area weighting to obtain regional means or totals; assumes independence between Land Classes and from total land.

## 2.3 Bootstrapping
- Significance testing uses bootstrap due to potential non-normality; resampling (typically 1000–10,000 replicates) yields distributions for stock or change estimates to derive statistics.

## 3. Reasons for Modifications to CS Methodology
- Previous reporting showed inconsistencies: stock estimates used data from all squares, while change estimates came from repeated measurements only.
- Missing information (e.g., unrepeated squares) drove these inconsistencies, especially as new squares were added over time.
- To address these issues, modelling approaches capable of providing consistent estimates for stock and change were explored and adopted for 2007.

## 4. Modelling Basics and Data Structure
- Incomplete data techniques (e.g., EM-like approaches) allow consistent estimation by leveraging correlation structures across surveys.
- Mixed effects/repeated measures models are used, with fixed effects corresponding to stock/change and random effects representing sampling variability (squares, plots, residuals).
- Modelling requires decisions about distributional forms and covariance structures; robustness of fixed effect estimates is a key advantage.

### 4.3 Square Level Data
- Treats square-level measurements as a random sample within each Land Class; uses a repeated measures (mixed) model with fixed effects for land-class means across surveys and random effects for squares and within-square survey deviations.

### 4.4 Plot Level Data
- Plot-level data within squares can be modeled to reflect hierarchical structure; previous approaches either aggregated to square level or treated plots as independent. The new modelling framework accommodates plot-level residuals and can be embedded in bootstrapping.

### 4.5 Model Specification
- General form: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik: fixed effects (stock by survey within land class),
  - s_ij: square-level random effects,
  - e_ijk: repeated-measures residuals.
- Random effects assumed normal with land-class-specific variances; repeated-measures residuals have covariances that can be structured (e.g., AR1) to reduce parameter count.
- To manage complexity, assumptions reduce the number of random parameters (e.g., common variance across surveys, AR1 covariance). Bootstrap standard errors are used to maintain robustness.

## 4.6 Model Testing – Broad Habitats
- Broad Habitat analyses (seven types) demonstrated inconsistencies when using old methods.
- Fitting AR1-based mixed models produced consistent stock and change estimates; differences relative to old methods generally fell within the prior inconsistency bounds.
- Findings supported adopting the consistent modelling approach for CS2007, including plotting and soil data, with potential extension to plot-level data.

## 5. Limitations and Implications
- Bootstrapping with square-level data is computationally demanding; fully parameterised models are slow, so AR1 with bootstrap was favored for large-scale application.
- Fixed effects estimates (stock/change) are robust to some distributional mis-specifications, but variance-covariance parameters can be sensitive; bootstrap mitigates this.
- Very non-normal data (e.g., standing water) can cause convergence issues; in CS freshwater data, older methodology was retained for those variables.
- Adopting a model-based approach uses information from all surveys, implying past estimates may be updated as new data arrive; this is conceptually different from the prior reporting inconsistencies and is generally small in effect.

## 6. References
- Barr et al., 1993; Haines-Young et al., 2000; Dempster, Laird, Rubin, 1977; Efron, Tibshirani, 1993; Scott, 2002.