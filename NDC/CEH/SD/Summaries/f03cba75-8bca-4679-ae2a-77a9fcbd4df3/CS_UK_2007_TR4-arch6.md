# Countryside Survey 2007: Statistical Methodology

- This report describes the statistical methods used to analyse Countryside Survey (CS) data, reviews the previous methodology, and explains the changes implemented for CS 2007 to achieve consistent estimation of stock and change.
- It demonstrates that modelling-based, consistent estimation is feasible and often more robust and precise than the previous approach, albeit requiring more assumptions and computational effort.
- The methodology is designed to utilise all available information (across surveys and the hierarchical data structure) to produce more precise estimates, with bootstrap-based measures of uncertainty to accommodate non-normal data distributions.

## Data and Sampling Design

- CS data come from a stratified sample of 1 km squares on a 15 km GB grid; each selected square is mapped and measured at two levels:
  - Square level: overall habitat/feature measurements for the entire square.
  - Plot level: detailed measurements within plots inside each square (e.g., vegetation, soils).
- Land Classification (LC) defines strata for square selection; classifications have expanded over time (GB 32 → 42 → 45 LC classes), with country-specific classifications (England, Wales, Scotland) closely related.
- Estimates are traditionally weighted by land area within each LC to produce regional/national figures.

## Estimation Approach (Old vs New)

- Previous approach:
  - Stock estimates used all data within a survey; change estimates used only repeated measurements across survey pairs.
  - This could yield inconsistencies between stock and change estimates (differences not equal to observed changes).
- New modelling approach (CS 2007):
  - Uses consistent estimation via modelling (mixed effects/repeated measures models) across both stock and change, for square and plot level data.
  - More efficient (often more precise) because it utilises all information and the data hierarchy.
  - Requires additional distributional assumptions; results checked against the old methodology to ensure validity, especially for small subsets.

## Modelling Basics and Data Levels

- Square-level data:
  - Treated as repeated measures within each LC; modeled with fixed effects for LC means across surveys and random effects for squares.
  - Aims to produce stock estimates per LC per survey and derive change estimates as differences, ensuring consistency.
- Plot-level data:
  - Acknowledges within-square plot variation; models are extended to include plot-level residuals to reflect additional hierarchical structure.
  - Both square-level and plot-level analyses can be embedded in bootstrapping procedures.

## Model Specification and Parameters

- General square-level model:
  - y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (LC i, survey k)
    - s_ij: square-level random effect for square j in LC i
    - e_ijk: repeated-measures error
- Distributional assumptions:
  - Random effects s_ij ~ N(0, τ_i^2) varying by LC
  - Repeated measures e_ijk ~ N(0, σ_ik^2) with covariances between surveys
- Parameter reduction (to keep models tractable):
  - Variances are assumed constant across surveys within a LC (σ_i for all surveys)
  - Covariances between surveys are modeled with an AR(1) structure, reducing per-LC random parameters to a small, stable set (three per LC when using AR1)
- Estimation and inference:
  - Fixed effects (stock/change) are estimated robustly; variances/covariances are less stable, so bootstrap standard errors are used for robust uncertainty.

## AR1 Modelling and Bootstrapping

- AR1 model (constant within-LC variance, first-order autocorrelation across surveys) provides a practical balance of robustness and computational efficiency.
- Bootstrapping is used to obtain standard errors and confidence intervals because it remains robust under non-normality and when distributional assumptions are imperfect.
- The combination of AR1 with bootstrap was investigated as a method to deliver consistent, robust estimates for CS data.

## Model Testing: Broad Habitats

- Historical habitat analysis (Broad Habitats) used data from 1984, 1990, and 1998 to compare old vs new methods.
- Old method: stock and change estimates could be inconsistent; new modelling approach produced consistent estimates where stock minus change matched inter-survey differences.
- Findings: differences between old and new estimates were generally small relative to existing uncertainties; the modelling approach resolved the inconsistencies without producing major, unjustified shifts.
- Extension to plot- and soil-level data (including 1978/1998 soil data) confirmed feasibility and consistency, supporting adoption for CS 2007.

## Limitations and Implications

- Computational demands are high; fully parameterised models are slow, so AR1 with bootstrap was chosen for practicality and automation across many variables.
- Fixed-effect estimates are robust to moderate mis-specification of random-effect distributions; variance/covariance estimates are more sensitive.
- Some variables with highly non-normal distributions can pose convergence issues (e.g., standing water in freshwater data); in such cases, legacy (old) methods may be preferred for that variable.
- Adoption of a fully model-based approach means that estimates for any one survey can be updated as new data become available, reflecting information from all surveys; this makes cross-reporting consistency over time more dynamic.
- The approach prioritises using all information and the data hierarchy to improve precision, at the cost of requiring model checks and robust automation.

## Practical Takeaways for Data Support

- When supporting data users, emphasise that CS 2007 introduces a consistent, model-based framework for stock and change across square and plot data, improving precision by leveraging all available data.
- Communicate the role of bootstrapped uncertainty estimates to accommodate non-normal data distributions.
- Highlight the hierarchical structure and the AR1 simplification as key to feasible, automated analysis across many variables.
- Note that results for past surveys may be updated slightly as new information from CS 2007 is integrated; this reflects a more optimal use of all data rather than an error correction.
- Acknowledge limitations and variable-specific decisions (e.g., retaining older methods for highly non-normal or problematic variables) to maintain reliability.

## References (key works)

- Barr et al. (1993), Countryside Survey 1990 Main Report
- Dempster, Laird, Rubin (1977), EM algorithm for incomplete data
- Efron & Tibshirani (1993), Bootstrap
- Haines-Young et al. (2000), Accounting for nature: assessing habitats in the UK countryside
- Scott (2002), Maximum likelihood estimation and empirical Fisher information
- CS2007 methodology adoption and validation within the Countryside Survey program