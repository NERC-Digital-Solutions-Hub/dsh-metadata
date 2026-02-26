# Countryside Survey 2007: Statistical Methodology for Analysis of Countryside Survey Data

- Purpose: Describe the statistical methodology used to analyse Countryside Survey (CS) data and document changes made for CS data in 2007 to achieve consistent estimation of stock and change.
- Motivation: Previous methods estimated stock and change with different data subsets, causing inconsistencies between stock and change estimates; modelling-based consistent estimation was explored and adopted for CS2007.
- Key outcome: Adoption of a modelling approach (mixed effects/repeated measures with AR1 structure) that uses all available data, provides more precise estimates, and yields consistent stock and change estimates across surveys.

## Executive Summary (core points)

- Earlier CS estimation used all data for stock but only repeated data for change, causing inconsistencies between stock and change estimates.
- Modelling approaches using broad habitat data showed consistent estimation is feasible and robust; differences from old methods were generally small within existing error bounds.
- CS2007 adopts consistent estimation via modelling, which utilizes all information and improves precision; future estimates for past surveys may be slightly revised as new data inform the model.
- Modelling requires stronger distributional assumptions, so results are validated by comparison with previous methods; bootstrap is used to obtain robust standard errors and confidence intervals.
- While modelling is more computationally intensive, it provides a unified framework for square- and plot-level data and supports automated application across many variables.
- For Broad Habitats, soils, and plot-level data, modelling demonstrated feasibility and improved consistency, leading to adoption of the new methodology for CS2007.

## Introduction

- This technical report describes sampling and analysis procedures for Countryside Survey data.
- Reviews previous CS methodology and details changes for 2007, with a emphasis on consistency of stock and change estimation.
- Prior literature and methodological foundations: CS1990 method, mixed effects models, and bootstrap techniques.

## Sampling and Estimation (CS data structure)

- Sampling design: stratified sample of 1 km squares on a GB-wide 15 km grid; two levels of sampling within each square (square-level and within-square plots/quadrats).
- Land Classification: ITE Land Classification; country-specific adjustments (England, Wales, Scotland) resulting in 45 classes overall (21 England, 8 Wales, 16 Scotland).
- Estimation (old approach outline): means and standard errors for each Land Class, then aggregated by area weighting to regional/national estimates; assumed independence between Land Classes.
- Bootstrapping (for significance): used since normality assumptions for estimates were questionable, particularly for square-level data; resampling provides distributional insight without strict normality.

## Reasons for Modifications to CS Methodology

- Inconsistencies observed when comparing stock and change across survey pairs due to missing information and differing data subsets used for stock vs change.
- Exploration of three consistency options (stock from all squares, change from repeated squares, or change from stock differences) showed inconsistencies when not using a unified approach.
- Modelling approach (consistent estimation) offered improved robustness and efficiency, applicable to both square and plot level data, though it introduces distributional assumptions.

## Modelling Basics

- Core idea: use incomplete data techniques via mixed effects/repeated measures models to obtain consistent stock and change estimates across surveys.
- Fixed effects: yearly means (per Land Class) treated as parameters to be estimated.
- Random effects: square-level and, for plots, plot-level deviations to capture hierarchical sampling and repeated measures structure.
- Emphasis on using complete data information and proper handling of missing data through model-based inference rather than ad hoc imputation.

## Square Level Data

- Model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (Land Class i at survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Distributional assumptions: s_ij ~ N(0, τ_i^2); e_ijk ~ N(0, σ_ik^2) with covariances between surveys, varying by Land Class i.
- Practical considerations: number of random parameters grows with the number of surveys; large numbers of land classes and limited squares per class make full models unstable and slow.
- Solution: reduce random-effect parameter count with parsimonious structures (e.g., AR1 for covariances) to keep models tractable while preserving fixed-effect estimates.

## Plot Level Data

- Plot data within squares adds complexity due to hierarchical structure.
- Previous methods treated plots variably (summarised to square level or treated plots as independent), risking inefficiency or bias.
- Current approach extends square-level modelling to include plot-level residuals, with the potential to embed these within bootstrapping to account for hierarchical variance.

## Model Specification (conceptual)

- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - Fixed effects: a_ik (land class means across surveys)
  - Random effects: s_ij (square deviations), e_ijk (survey deviations)
- Distributional framework: s_ij ~ N(0, τ_i^2); e_ijk ~ N(0, σ_ik^2) with covariances among surveys
- AR1 simplification: assume common random-effect variances across surveys and autoregressive structure for covariances, reducing parameter load (three random-effect parameters per Land Class, regardless of number of surveys)
- Bootstrap: used to obtain robust standard errors since variance-covariance parameters are difficult to estimate precisely

## Model Testing – Broad Habitats

- Historical validation: compared old methods (stock from full data vs change from repeated squares) with modelling (AR1) on seven Broad Habitats across 1984, 1990, 1998.
- Findings: modelling produced consistent stock and change estimates; differences with old methods generally fell within old method error bounds; changes between adjacent surveys did not necessarily sum to longer-interval changes under old methods, which modelling addresses.
- Overall implication: consistent estimation via modelling is feasible and preferable for broad habitats; supports adoption for CS2007; similar consistency observed for soil data and plot-level analyses.

## Limitations and Implications

- Computational demands: AR1 modelling with bootstrap is slower than old methods but feasible for CS-scale analyses; fully parameterised models are often impractical for large variable sets.
- Model selection: fixed-effects estimates (stock/change) are robust to some mis-specification, but variance/covariance parameters are sensitive; bootstrap mitigates this.
- Non-normal data: certain variables (e.g., standing water) displayed non-normality causing convergence to local maxima; in such cases, old methodology results may be preferred for those variables.
- Data integration across surveys: incorporating data from all surveys means past estimates may be revised as new data are added; this is conceptually different from the older, more static inconsistencies and is deemed reasonable with accumulation of information.
- Practical takeaway: a standard AR1-based modelling approach with bootstrap offers robust, efficient, and scalable estimation, enabling automated application across many variables while acknowledging some limitations and the need for occasional exceptions.

## References and Data Access

- References to CS methodology literature and foundational statistical sources (EM algorithm, bootstrap, mixed models, etc.).
- Data and project information available through Countryside Survey project offices and official website; CS2007 was funded by Defra and NERC, with data management and portals described.