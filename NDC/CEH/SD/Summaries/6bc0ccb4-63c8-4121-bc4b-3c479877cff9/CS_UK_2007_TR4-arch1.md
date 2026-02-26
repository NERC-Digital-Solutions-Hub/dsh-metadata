# COUNTRYSIDE SURVEY 2007 METHODOLOGY

## Executive Summary
- Describes the statistical methodology for Countryside Survey (CS) data and outlines the 2007 changes to estimation and analysis.
- Old methods were robust but produced inconsistencies: stock used all survey data while change used only repeated measurements, leading to mismatches between stock and change estimates.
- Modelling with consistent estimation (via mixed effects/repeated measures) is feasible and generally robust; results align with previous methods within the context of existing inconsistencies.
- The 2007 CS adopts the modelling approach, which uses all available information to produce more precise estimates, with past survey estimates updated as new data become available (usually small changes).
- Implementing modelling is technically demanding and slower than previous methods, but the AR1-based modelling approach is fast enough for practical use and suitable for automation across many variables.
- Bootstrapping is used to obtain standard errors and confidence intervals, accommodating non-normal data.
- For Broad Habitats, testing with 1984–1990–1998 data showed that modelling eliminated stock/change discrepancies; the approach was extended to plot-level data and soils, leading to adoption of the new methodology for the 2007 CS.

## Sampling and Data Structure
- Field data come from a stratified sample of 1 km squares on a 15 km GB grid.
- Two sampling levels: whole squares and features within squares (plots/quadrats); measurements include binary and continuous variables.
- Land Classification (ITE) strata underpin square selection; classifications have expanded to 45 classes (country-specific: England, Wales, Scotland) to support separate reporting.

## Estimation and Consistency
- Previous estimation combined land-class means weighted by land area to obtain region-wide stock or change; stock used all data, change used repeated measurements, causing inconsistencies.
- Three potential consistent approaches exist; CS moved to modelling to achieve consistent stock and change estimates across all data.
- Consistency is achieved by modelling stock and change jointly across all surveys, rather than deriving change only from repeated squares.

## Modelling Basics
- Incomplete data techniques (e.g., EM-type approaches) underpin consistent estimation, using information from all surveys and their correlations.
- Mixed effects models (fixed effects for stock/change by land class and survey; random effects for squares and within-square repeated measurements) are used.
- Assumptions about data distribution and random effects are required; fixed effects remain robust to some misspecifications, while variance/covariance parameters are more sensitive.

## Square Level Data
- Data treated as repeated measures within land classes; a mixed model is used with:
  - Fixed effects: land-class means for successive surveys.
  - Random effects: square-level deviations and survey-to-survey correlations.
- A simple yet effective approach models fixed effects as functions of survey year; stock estimates come from scaling by land-class area, and change estimates are differences of fitted stock values.

## Plot Level Data
- Plot data within squares previously analyzed with varying methods; current approach extends the square-level model to include plot-level residuals (random plot effects) and possibly correlations within plots across surveys.
- Models can be embedded within bootstrap procedures to obtain robust standard errors.

## Model Specification and Parameters
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Random effects distributions:
  - s_ij ~ N(0, τ_i^2) varies by land class
  - e_ijk ~ N(0, σ_ik^2) with covariances across surveys
- With K surveys, the model includes K fixed-effect parameters per land class and many random-effect parameters; to keep it tractable, the AR1 (order-1 autoregressive) structure is used for covariances, reducing random parameters to three per land class.
- Bootstrap is used to obtain standard errors, providing robustness to non-normality.

## Model Testing – Broad Habitats
- Analyses of Broad Habitats using old (stock vs. repeat-squares change) vs. new (consistent modelling) methods showed that inconsistencies largely disappear under the modelling approach.
- Differences between methods generally fell within the old method’s error bounds; the new approach provided consistent estimates and, for plotting, extended to soil data and plotting-level analyses.
- Result: adoption of the modelling approach for CS2007 across broad habitat data.

## Limitations and Implications
- Modelling with bootstrapped envelopes is computationally intensive; fully parameterised models are slow for large variable sets, but AR1-based modelling balances speed and reliability.
- Fixed-effects estimates are robust to some distributional mis-specifications; variance/covariance estimates are more sensitive, though bootstrap SEs mitigate this.
- Some non-normal data (e.g., standing water, freshwater) caused convergence issues; in such cases, older methods were retained for those variables.
- Using data from all surveys means past survey estimates get updated as new data arrive, which is consistent with acquiring new information, though it reduces cross-reporting consistency across reporting occasions.

## Practical Implications for Analysts
- The new methodology provides more precise, consistent stock and change estimates by leveraging all available data and properly accounting for data hierarchy (square and plot levels) and missing data.
- Analyses are updated as new surveys are added; expect small revisions to past estimates.
- An automated AR1-based modelling framework with bootstrap SEs is suitable for large-scale analyses across many variables, though computational planning is essential.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (1977); Efron & Tibshirani (1993); Scott (2002).