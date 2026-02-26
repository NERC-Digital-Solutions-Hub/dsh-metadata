# Countryside Survey 2007 Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for CS2007.
- Previous methods: stock estimates used all survey data; change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling for consistent estimation (using all available information across surveys) is feasible and generally robust; differences from old methods are small relative to existing inconsistencies.
- Adopts consistent estimation for CS2007, with careful validation against older methods to guard against incorrect conclusions from distributional assumptions.
- Modelling yields more precise estimates by leveraging all information; past estimates may be updated slightly as new surveys add information.
- Implementation is technically challenging and more computationally intensive due to iterative fitting and complex CS sampling; AR1-based modelling with bootstrapped standard errors is chosen for practicality and robustness.
- Demonstrations with Broad Habitat data and other datasets supported moving to the new, consistent methodology.

## Introduction
- This technical report provides an overview of CS sampling and analysis procedures, reviews the previous CS methodology, explains the rationale for changes in 2007, and discusses limitations and implications.
- Full methodological details of CS sampling and estimation are available in prior reports.

## Overview of Previous CS Methodology
- Sampling: CS used a stratified sample of 1 km squares within a 15 km GB grid; two sampling levels within each square (square-level and plot-level measurements) with varied data types (binary and continuous).
- Land Classification: National classifications (ITE) expanded from GB to country-specific schemes, culminating in 45 land classes for CS2007 (21 England, 8 Wales, 16 Scotland) to support separate reporting.
- Estimation: Regional/national estimates built by calculating means and standard errors for each Land Class and then area-weighting these estimates to form totals or means; independence assumed between Land Classes.
- Bootstrapping: For square-level data, significance testing uses bootstrap due to concerns about non-normality, providing robust standard errors and confidence intervals.

## Reasons for Modifications to CS Methodology
- Inconsistencies: Stock estimates (all data) and change estimates (repeat measurements) could diverge, especially as unrepeated squares appeared in later surveys, leading to apparent mismatches over time.
- Approaches considered for consistency:
  - Use stock estimates from all data and compute change as the difference between stock estimates (simple but potentially inefficient and not directly applicable to plot-level data).
  - Use repeated squares only for change (robust but less data-efficient and not applicable to all data types).
  - Modelling (consistent estimation) to derive stock and change jointly from all data, applicable to both square and plot level data, yielding consistent and more efficient estimates.
- Decision: Adopt modelling for consistent estimation (with an understanding of added distributional assumptions and the need for validation).

## Consistent Estimation
- Modelling approach relies on mixed effects/repeated measures models to handle incomplete data and the hierarchical CS sampling design.
- Objectives: produce stock and change estimates that are simultaneously consistent across sources and surveys; use all available data to improve precision.
- Trade-offs: requires assumptions about data distributions and random effects; more computationally intensive; results may be influenced by additional data across surveys.

### Square Level Data
- treated as a repeated-measures problem within land classes.
- Fixed effects: land-class means across surveys (stock).
- Random effects: square-level deviations and within-square survey residuals, with correlations across surveys.

### Plot Level Data
- Plot data within squares can be integrated by extending the model to include plot-level residuals, while maintaining square-level structure.
- Bootstrapping can be applied to account for the hierarchical data structure.

## Model Specification
- General model for square-level data: y_ijk = a_i_k + s_ij + e_ijk
  - a_i_k: fixed effects (land-class means per survey)
  - s_ij: square random effects
  - e_ijk: repeated-measures residuals
- Random effects: assumed normal with land-class-specific variances; residuals have land-class and survey-specific variances and covariances.
- Complexity: full model has many random-effect parameters (scales with number of surveys), which can be unstable with many land classes.
- Practical reduction: assume common variance components across surveys or land classes where appropriate; adopt AR1 (autoregressive) structure to constrain covariances, reducing parameters to a manageable level (three random parameters per survey under AR1).
- Bootstrap: used to obtain robust standard errors since variance/covariance estimates are less precise than fixed effects; particularly important for complex models.

## Model Testing - Broad Habitats
- Historical Broad Habitat data (1984, 1990, 1998) analyzed to test modelling approach.
- Old method produced inconsistencies between stock and change; modelling via AR1 produced consistent estimates with differences generally within prior inconsistency bounds.
- Change estimates from modelling aligned with the sum of consecutive inter-survey changes, as expected.
- Results for stock and change under modelling were largely within the uncertainty of old methods, supporting adoption.
- Additional consistency checks extended to soil data (1978, 1998) and plot-level data, confirming feasibility.

## Limitations and Implications
- Computational demands: AR1 modelling with bootstrap is slower than old methods but still feasible for large numbers of analyses; automated modelling pipelines are essential for consistency.
- Fixed-effects robustness: estimates are robust to reasonable model variation; variance/covariance parameters are more sensitive and Bootstrap helps preserve reliability.
- Non-normal data: some variables with highly non-normal distributions (e.g., standing water) can cause convergence or bias; in such cases, older methods might be preferred for those variables.
- Updating past results: analyses use data from all surveys, so past survey estimates may be revised as new data are incorporated; this reflects the incorporation of new information rather than inconsistency in earlier reporting.
- Overall benefits: more precise and coherent estimates by fully utilizing data hierarchy and all available information; improved comparability across survey years and data types (square and plot level).

## References
- Barr et al. (1993), Countryside Survey 1990 Main Report.
- Dempster, Laird, and Rubin (1977), EM algorithm for incomplete data.
- Efron and Tibshirani (1993), Bootstrap methods.
- Haines-Young et al. (2000), Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002), Maximum likelihood estimation using the empirical Fisher information matrix.