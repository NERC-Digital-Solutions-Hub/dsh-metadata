# Countryside Survey in 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data and outlines changes made for CS in 2007.
- Old methods: stock estimates used all data from a survey; change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling for consistent estimation was found feasible and robust, with differences from old methods generally within existing variability.
- CS 2007 adopts a modelling approach that uses all available information to produce more precise (efficient) estimates; new survey data can update past estimates, with changes typically small.
- Implementation is technically challenging and computationally intensive, requiring iterative modelling rather than formulaic calculations; practical issues arising from CS sampling were overcome to deliver a markedly improved product.
- The approach necessitates checks of model validity, especially for small subsets, by comparison with old methods; results remain broadly consistent with prior findings.
- For Broad Habitats, soil data, and plot-level data, consistent estimation was demonstrated, supporting adoption of the new methodology for 2007 CS and potential alignment across data levels.

## Introduction
- This technical report outlines the sampling and analysis procedures for Countryside Survey data, reviews the previous CS methodology, and explains why and how estimation procedures were changed for 2007.
- Fuller historical methodology is documented in prior CS reports.

## Sampling and Data Structure
- CS data come from a stratified sample of 1 km squares over a GB grid, with measurements at two levels:
  - Square level: whole-square measurements across Land Classes.
  - Plot level: within-square measurements (e.g., vegetation, soils).
- Land Classification (ITE) classifications evolved over time:
  - GB: 32 classes originally; CS2000: 42 classes; CS2007: 45 classes (England, Wales, Scotland reporting separated).
- Data types include binary and continuous variables; sampling design supports robust regional/national estimates via weighted aggregation by land-class area.

## Estimation and Bootstrapping
- Early method: estimate means and standard errors per Land Class, then combine by land-area weighting to regional totals; assumed independence between Land Classes.
- Bootstrapping (from CS2000 onward) used for square-level data to obtain significance without relying on normality, accommodating skewed distributions.

## Reasons for Modifications to CS Methodology
- Previous point estimates (stock vs. change) were inconsistent because stock used all data while change used only repeated measurements.
- Inconsistencies arose mainly from missing information between survey pairs (new squares added, some squares not recorded in one of the surveys).
- Aim: produce consistent estimates across time horizons (e.g., between non-adjacent surveys) and to use all available data effectively.
- Modelling approaches (consistent estimation) can be applied to both square and plot data; they require more assumptions about data distributions but improve precision and coherence.

## Modelling Basics
- Incomplete data techniques (e.g., EM-like mixed models) enable consistent stock and change estimates by leveraging data across all surveys.
- Mixed effects/repeated-measures models include:
  - Fixed effects: land-class means across surveys (stock-related parameters).
  - Random effects: square-level effects, plot-level effects, and repeated-measure correlations.
- Two main modelling paths:
  - Square level data: repeated-measures mixed model with land-class fixed effects and square random effects; correlations across surveys handled via random components.
  - Plot level data: extend models to include plot-level residuals in addition to square-level effects; bootstrapping can incorporate either form.

## Model Specification
- General square-level model: y_ijk = a_iK + s_ij + e_ijk
  - a_iK: fixed effects (land-class means across surveys)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Random effects are assumed normal with land-class-specific parameters; variances and covariances are estimated.
- To keep the model tractable with many surveys and Land Classes, random-effects parameterization is reduced (notably via AR1 assumptions):
  - Common standard deviation across surveys for each land class (σ_i)
  - Autoregressive AR1 structure for covariances across successive surveys
- This AR1 approach drastically reduces the number of random parameters (three per land class regardless of survey number) while preserving essential correlation structure.
- Bootstrap is used to obtain standard errors, ensuring robustness to distributional mis-specifications.

## Model Testing – Broad Habitats
- Historical CS outputs for Broad Habitats used 1984, 1990, and 1998 data; prior methods yielded stock-change inconsistencies.
- Modelling (AR1 with consistent estimation) yields estimates where change equals the difference of stock estimates and where summed inter-survey changes align with overall changes.
- Comparison between old and new methods shows differences are generally within existing discrepancies, with improved internal consistency.
- Additional analyses for soil data (1978, 1998) and plot-level data confirmed feasibility of consistent estimates across scales, supporting adoption for 2007 CS.

## Limitations and Implications
- Bootstrapped, model-based (AR1) estimates are computationally demanding; full parameterization is slow for large variable sets.
- A balance is struck by using AR1 with bootstrap for standard errors, enabling automated application to many variables.
- Performance checks show fixed-effect estimates (stock/change) are robust to reasonable model variation; variance/covariance parameters are more sensitive to distributional assumptions.
- Non-normal data (e.g., standing water) may lead to convergence or estimation issues; in such cases, older methods may be retained for those variables.
- Adopting a consistent modelling framework means past estimates may be updated as new surveys are added, causing small revisions to previous findings; this reflects improved use of information rather than errors.

## Implications for Monitoring Frameworks
- Consistency across time and data levels is achievable by modelling incomplete data rather than relying on disparate, ad-hoc methods.
- Using AR1-like random-effects structures and bootstrapped SEs provides robust, scalable estimates for large, hierarchical environmental datasets.
- When data evolve (new survey rounds, expanded classifications), estimates for earlier periods can be updated, improving overall coherence.
- The approach requires careful metadata management, transparent reporting of model assumptions, and computational resources for automated, large-scale analyses.

## References (selected)
- Barr et al. (1993); CS1990 methodology
- Dempster, Laird, Rubin (EM algorithm for incomplete data)
- Efron, Tibshirani (Bootstrap)
- Haines-Young et al. (2000) on habitat accounting
- Scott (2002) on maximum likelihood with empirical Fisher information