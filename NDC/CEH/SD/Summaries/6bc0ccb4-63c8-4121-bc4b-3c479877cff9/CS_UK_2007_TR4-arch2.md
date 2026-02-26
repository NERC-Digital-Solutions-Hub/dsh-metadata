# Countryside Survey 2007 Methodology

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data and document changes implemented for the 2007 CS analysis to improve consistency and precision over previous surveys.

## Executive summary (key takeaways)

- Previous CS estimation mixed stock and change using different data sets (stock from all squares; change from repeated measurements), causing inconsistencies between stock and change estimates.
- Modelling for consistent estimation is feasible and robust; it yields estimates similar to old methods within existing uncertainty but uses all available data to improve precision.
- The new modelling approach has been adopted for CS 2007, though it relies on additional distributional assumptions; results are validated by comparisons with the older method.
- The modelling approach provides more precise estimates and can update prior results with new information, though it may slightly revise previous findings as data accumulates.
- Implementation is computationally intensive but has been made tractable (notably via AR1 mixed-effects models and bootstrap for standard errors).
- The approach has been tested on Broad Habitat data (and other data types, including soil and plot-level data), demonstrating feasibility and improved consistency.
- A balance is struck between model complexity and practicality, enabling automated application across many variables.

## Introduction

- This technical report outlines sampling and analysis procedures for CS data, reviews the previous methodology, and explains the reasons and details for changes adopted in CS 2007.
- References to earlier CS methodology are provided for context.

## Sampling

- CS data come from a stratified sample of 1 km squares at the intersection of a 15 km GB grid.
- Two levels of sampling: whole squares and features within squares (plots/quadrats) to capture broad and within-square characteristics.
- Stratification is based on the ITE Land Classification; national adaptations increased the class count (GB 32 -> 45 Land Classes; England, Wales, Scotland have country-specific classifications).

## Estimation

- Old method: compute means and standard errors for each Land Class, then combine (weight by land area) to estimate region-wide means/totals.
- Assumptions: means across Land Classes are independent; minimal distributional assumptions; robustness but potential inconsistencies between stock and change estimates.

## Bootstrapping

- Significance testing moved from assuming normality to bootstrap methods due to skewness and non-normality in some features.
- Bootstrapping (typical 1000–10,000 resamples) provides distribution-accurate standard errors and confidence intervals without strict distributional assumptions.

## Reasons for modifications to CS Methodology

- Inconsistencies: Previous point estimates appeared inconsistent because stock was estimated from all data while change used repeated measurements only.
- The report emphasizes that inconsistencies are due to estimation methods, not data errors, and can be addressed by consistent estimation approaches.
- Two main candidate approaches were considered:
  - Estimating change as the difference between stock estimates (consistent but potentially less efficient, especially with covariance between surveys; difficult to apply to plot-level data).
  - Modelling with mixed effects to jointly estimate stock and change (consistent and efficient; applicable to both square and plot data but requires more assumptions and computational resources).
- CS 2007 adopts modelling for consistency, with verification against older methods.

## Modelling basics

- Incomplete data techniques (e.g., mixed effects/repeated measures models) are used to handle missing information across surveys.
- Models include fixed effects (stock/change means by Land Class and survey) and random effects (to capture variation among squares and repeated measures across surveys).
- Distributions and variance-covariance structures are specified, but full parameterization can be complex; robustness of fixed effects is emphasized.

## Square level data

- Data treated as repeated measures within Land Classes.
- Basic model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: random square effect for square j in land class i
  - e_ijk: random within-square (repeated measures) error
- Random effects account for square-level variation and correlation of measurements across surveys.

## Plot level data

- Plot-level data within squares require extending the square-level model to include plot-level residuals.
- Two approaches:
  - Treat plots within squares as additional observations with square-level variation accounted for.
  - Include plot-level random effects to reflect within-square heterogeneity.
- Both approaches can be embedded within bootstrap procedures to obtain robust standard errors.

## Model specification

- General square-level model: y_ijk = a_ik + s_ij + e_ijk
- Distributional assumptions: s_ij ~ N(0, τ_i^2) varying by land class; e_ijk ~ N(0, σ_ik^2) varying by land class and survey; covariances of repeated measures vary by land class and survey pair.
- For multiple surveys (K): a_ik (fixed effects) for each Land Class and survey; random effects include variances and covariances (potentially many).
- Practical challenge: full model becomes unstable with many random parameters; reduces dimension via simplifying assumptions.

## Model reduction and AR1 approach

- To manage parameter complexity, several reductions are used:
  - Equalizing certain random effects across land classes (where appropriate); more realistic: variance parameters do not vary across surveys.
  - Autoregressive AR1 structure for repeated-measures covariances: assumes constant within-class correlation between successive surveys; reduces repeated-measures covariances to a single parameter per land class.
- AR1 plus bootstrap is adopted to achieve consistent estimation with feasible computation.

## Model testing – Broad Habitats

- Prior CS outputs used Broad Habitats (stock and change) across 1984, 1990, 1998 surveys.
- Old methodology produced inconsistencies between stock and change; modelling with AR1 produced consistent estimates.
- Differences between old and new methods were generally small relative to existing uncertainties; most changes remained within old error bounds.
- Additional testing showed feasibility for plot-level and soil data, supporting the adoption of the new methodology for 2007 CS.

## Limitations and implications

- Bootstrap-based standard errors with the AR1 model provide robustness, but fully parameterized models can be slow; AR1 offers a practical balance between speed and accuracy.
- Model selection and checking are necessary but time-consuming when analyzing many variables; hence a standard, automated AR1 approach is favored.
- Distributional assumptions influence variance estimates; robustness of fixed effects is generally good, but variance/covariance estimates can be sensitive.
- Some non-normal data (e.g., very skewed freshwater standing water) may converge to local maxima; in such cases, old methods may be preferred for that variable.
- A key implication: analyses utilize data from all surveys; as new surveys are added, prior estimates may be revised upward or downward, which is a natural consequence of incorporating more information.

## References

- Summaries and technical details of past CS methodology and statistical foundations are cited (various Barr et al., Dempster et al., Efron & Tibshirani, Haines-Young et al., Scott).