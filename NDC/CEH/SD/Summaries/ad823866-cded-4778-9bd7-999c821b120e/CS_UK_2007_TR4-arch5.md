# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data, detailing changes made for CS2007.
- Critique of previous methods: stock was estimated using all data from a survey, while change relied on repeated measurements, causing inconsistencies between stock and change estimates.
- Demonstrates that modelling for consistent estimation is feasible and robust, with CS2007 adopting this modelling approach.
- Modelling yields more precise estimates by using all available information; past survey estimates may be slightly revised as new data inform earlier periods.
- Implementation is technically challenging and computationally intensive, but results in a significantly improved product.

## What the document covers
- Overview of CS sampling, estimation, and bootstrapping methods.
- Rationale for modifying methodology to achieve consistent stock and change estimates.
- Detailed description of the modelling approach, including square-level and plot-level data.
- Model specification, testing (Broad Habitats), limitations, and implications.
- References to prior CS work and relevant statistical methodology.

## Data structure and collection
- CS data come from a stratified sample of 1 km squares on a 15 km GB grid; measurements occur at two levels:
  - Square level: data aggregate to the whole square (stock estimates per Land Class).
  - Plot level: within-square plots provide additional, hierarchical data.
- Land Classification: Land Classes expanded to 45 (England, Wales, Scotland have country-specific classifications) to support separate reporting; examples include the Broad Habitats framework.
- Data types range from binary to continuous measures (areas, lengths).

## Estimation: old vs. new approaches
- Old approach:
  - Stock: uses all data from a survey.
  - Change: uses repeated measurements across surveys.
  - Result: inconsistencies between stock and change estimates; potential mis-match when comparing adjacent and non-adjacent survey intervals.
- New approach (CS2007 modelling):
  - Use modelling (mixed effects/repeated measures) to obtain consistent stock and change estimates across all surveys.
  - Benefits: leverages all available information; typically more precise estimates; changes can be decomposed consistently over multiple intervals.
  - Trade-offs: requires additional distributional assumptions about data; results must be validated, especially for small subsets.

## Modelling approach: basics
- Incomplete data handling through modelling rather than ad-hoc data imputation, enabling consistent stock and change estimates.
- Models involve fixed effects (land class means across surveys) and random effects (variation by square, plot, and survey-associated residuals).
- For square-level data, a repeated measures mixed model is used.
- For plot-level data, models are extended to include plot-level random effects; both can be embedded within bootstrap procedures for uncertainty estimation.

## Square-level data modelling
- General model: y_ijk = a_i_k + s_ij + e_ijk
  - a_i_k: fixed effects (land class i, survey k)
  - s_ij: random square effect within land class i
  - e_ijk: repeated-measures residual
- Random effects are assumed normal with land-class-specific variances; correlations across surveys are modeled.
- The model scales fixed effects to stock estimates per survey by land-class area; changes are differences between successive stock estimates.

## Plot-level data modelling
- Plot-level data extend the square-level model by adding a plot-level residual to capture within-square, within-land-class variation.
- Allows for correlations of survey residuals at the plot level, improving efficiency and accuracy over treating plots as independent.

## Model specification and practical considerations
- Full model: many random-effect parameters (variances and covariances) would be required, which is impractical with CS’s many land classes and limited squares per class.
- Reduction strategies:
  - Assume random-effect variances do not vary across surveys (common σ_i).
  - Use an AR1 (first-order autoregressive) structure for covariances to reflect correlation between successive surveys, reducing random parameters to a manageable few per land class.
- Bootstrapping remains essential for robust standard errors, particularly given potential non-normality and complex variance structures.
- AR1 model with bootstrap standard errors was evaluated as a robust, practical solution for CS data.

## Model testing: Broad Habitats
- Analyses of habitat data (1984, 1990, 1998) using old methods showed inconsistencies between stock and change estimates.
- Modelling with AR1 mixed effects provided consistent stock and change estimates; changes between adjacent surveys aligned with sums across intervals, improving interpretability.
- Comparisons indicate that modelling changes did not produce estimates outside the old method’s error bounds and often reduced discrepancies.

## Limitations and implications
- Computationally intensive; AR1 modelling is slower than the old approach but feasible for large CS analyses.
- Fixed-effect estimates are robust to moderate distributional mis-specifications; variance components are more sensitive.
- Very non-normal data (e.g., standing water in freshwater data) can lead to convergence issues or bias; in such cases, old methods may be preferred for that variable.
- Because the modelling uses data from all surveys, past survey estimates can be revised as new data are added, which is conceptually different from prior practice of isolated, static reporting.
- The approach offers improved precision and consistent interpretation but requires comprehensive metadata, automated workflows, and clear documentation to support governance and reproducibility.

## Data governance and stewardship implications
- Provenance and versioning: past estimates may change with new data; maintain clear versioned datasets and model specifications.
- Metadata: document modelling choices (AR1 structure, variance assumptions, bootstrap procedures) and their rationale.
- Reproducibility: automated, scalable analysis pipelines are essential to apply the standard modelling approach across many variables.
- Transparency: provide diagnostics comparing old and new methods, and report both fixed effects estimates and bootstrap-based uncertainty.
- Data quality: improved handling of missing data and hierarchical structure enhances data quality but requires careful interpretation when communicating results to stakeholders.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P. et al. (1977). Maximum likelihood from incomplete data via the EM Algorithm.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for Nature: Assessing Habitats in the UK Countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.