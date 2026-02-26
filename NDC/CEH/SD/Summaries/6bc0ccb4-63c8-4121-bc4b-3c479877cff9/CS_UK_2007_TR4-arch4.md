# Countryside Survey 2007: Statistical Methodology for the Analysis of Countryside Survey Data

- Purpose: Describe the statistical methodology used to analyse Countryside Survey (CS) data, outlining changes from previous methods and the adoption of a modelling approach for consistent estimation in 2007.
- Core shift: Move from stock/change estimates derived from different data subsets to consistent estimation using modelling across all surveys, leveraging all available information.
- Key benefit: More precise estimates by utilizing the full dataset and the hierarchical structure of CS data; improved robustness to missing data and non-normal distributions via bootstrap.
- Important caveat: Modelling introduces additional distributional assumptions; results are validated by comparing with the previous methodology, especially for small data subsets.
- Implications for reporting: Estimates for any given survey may be updated as new surveys are added; cross-survey consistency is achieved through the modelling framework rather than ad hoc adjustments.

## Introduction
- The report provides an overview of CS sampling and analysis procedures, reviews the previous methodology, and explains changes introduced for CS2007, along with limitations and implications.

## Sampling
- Data come from a stratified sample of 1 km squares on a 15 kmGB grid.
- Two sampling levels: square level (whole-square measures) and within-square plots (plot level) with both binary and continuous variables.
- Land Class stratification uses the ITE Land Classification, which evolved from 32 to 45 classes to support country-specific reporting (England, Wales, Scotland).

## Estimation
- Historically, regional/national estimates were obtained by:
  - Means/SEs for each Land Class, then
  - Weighted combination by land area to get regional means or totals.
- This approach assumed independence between Land Classes and across data, with minimal distributional assumptions.

## Bootstrapping
- To assess significance without normality assumptions, bootstrap methods (1000–10,000 resamples) are used for square-level data, providing robust SEs and CIs.

## Reasons for Modifications to CS Methodology
- Inconsistencies: Stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.
- Different reporting focus: Shifting from adjacent-survey changes to long timelines highlighted inconsistencies; modelling offered a path to consistency.
- Modelling vs traditional methods: Modelling yields consistent and efficient (more precise) estimates for both stock and change, valid for square and plot data, but relies on distributional assumptions that require validation.

## Modelling Basics
- Incomplete data are common due to survey design; modelling uses mixed effects/repeated-measures frameworks to incorporate data from all surveys.
- Fixed effects capture stock/change values; random effects capture sampling-related variability.
- Requires specifying distributions for random effects; models are chosen to balance complexity and stability, especially with many Land Classes and limited squares per class.
- AR1-style reductions are used to limit the number of random parameters and make nationwide automated analyses feasible.

## Square Level Data
- Treat CS as a repeated-measures design within Land Classes.
- Basic model: y_ijk = a_iK + s_ij + e_ijk
  - a_iK: fixed effects for Land Class i across surveys (stock)
  - s_ij: square-level random effect within Land Class i
  - e_ijk: repeated-measures error
- Random effects (variances/covariances) are reduced via AR1 assumptions to enable stable, automated analyses.

## Plot Level Data
- Plot data within squares can be integrated by extending the square-level model with an additional plot-level random effect.
- Correlated survey residuals are modeled at the plot level, embedded in bootstrapping to maintain robust SEs.

## Model Specification
- General form for square data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: square random effect
  - e_ijk: repeated-measures error
- Distributional assumptions are simplified to enable robust fixed-effect estimates; variance/covariance parameters are more sensitive to mis-specification, hence bootstrap is used for SEs.

## Model Testing – Broad Habitats
- Historically, Broad Habitats were analyzed using stock/change from different methods, revealing inconsistencies.
- Modelling with AR1 and bootstrap produced consistent stock and change estimates across 1984–1998 data.
- New approach yielded estimates within old-method error margins, validating the modelling method as reasonable.

## Limitations and Implications
- AR1 modelling is computationally heavier but provides stable, robust fixed-effect estimates; full parameterisation is slow for large variable sets.
- Automated, standard modelling (AR1 with bootstrap) is favored for large-scale CS analyses.
- Non-normal distributions can affect variance estimates; bootstrap mitigates this risk, though extreme non-normality may still pose challenges (e.g., freshwater standing water case).
- Using data from all surveys means previous survey estimates may be revised as new data are added; this is considered a natural consequence of incorporating new information.
- The approach improves precision and consistency but requires careful interpretation when comparing across reporting occasions.

## References
- Key foundational sources and methodological guides cited for sampling, estimation, bootstrapping, and mixed-model approaches.