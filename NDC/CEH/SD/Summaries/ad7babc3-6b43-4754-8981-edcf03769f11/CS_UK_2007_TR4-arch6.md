# Countryside Survey in 2007

## Executive Summary
- Describes the statistical methodology used for analyzing Countryside Survey (CS) data and the changes implemented for CS in 2007.
- Previous methods were robust but inconsistent: stock used all data from a survey, while change used only repeated measurements, causing mismatches between stock and change estimates.
- Modelling (consistent estimation) via data from all surveys is feasible and robust; differences from old methods are generally small.
- Adoption of modelling methods for CS2007 yields more precise estimates by utilizing all available information and the data’s hierarchical structure.
- Modelling is computationally more demanding; results require checks against the previous method, but implemented AR1 mixed-effects models with bootstrap for robust standard errors.
- For Broad Habitats (and plot-level data in CS2000) modelling produced consistent estimates; CS2007 extends this to plot-level data, enabling consistent analysis across scales.
- Conclusion: the new modelling approach is adopted for CS2007, with emphasis on consistency, precision, and the ability to update previous surveys as new data become available.

## 1. Introduction
- Provides an overview of CS sampling and analysis procedures; reviews previous CS methodology; explains reasons and details of changes for 2007; discusses limitations and implications.
- Full prior detail available in CS1990 report.

## 2. Sampling
- CS Field Survey uses a stratified sample of 1 km squares on a 15 km GB grid.
- Two sampling levels: squares (whole-square measures) and plots/quadrat within squares (within-square features).
- Measurements span binary to continuous variables.
- Land Classification (ITE) used for stratification; classifications have expanded over time to England, Wales, Scotland (45 classes in 2007, country-specific classifications).

## 3. Estimation
- Original method: compute means/standard errors per Land Class, then combine via area-weighted sums to get regional/national estimates.
- Minimal assumptions about data distribution; stock estimates assumed independent across Land Classes; change estimates based on repeated measurements.
- Inconsistencies arise because stock uses all data while change uses repeated measurements only.

## 4. Bootstrapping
- Significance testing uses bootstrap due to concerns about non-normality, especially for square-level data.
- Bootstrapping resamples data to approximate the distribution of stock/change estimates, providing robust standard errors and confidence intervals.

## 4. Reasons for Modifications to CS Methodology
- Previous reporting emphasized current survey and changes since the last survey; this created apparent inconsistencies across non-adjacent survey intervals.
- New approach aims for consistency across multiple surveys by using modelling to produce stock and change jointly.
- Three potential consistent-estimation approaches were considered; modelling emerged as the most robust and transferable across square and plot-level data, despite requiring more assumptions.

## 4.2 Modelling Basics
- Modelling incomplete data uses mixed-effects/repeated-measures models to produce consistent stock and change estimates across surveys.
- Models incorporate fixed effects (stock/change values by Land Class/year) and random effects (survey, square, plot-level variation, and their covariances).
- Incomplete data techniques rely on correlation structures from repeated measurements rather than imputing missing values.

## 4.3 Square Level Data
- Data treated as a random sample of squares within each Land Class; a repeated-measures (mixed) model is used.
- Fixed effects: mean values within Land Classes across surveys (stock estimates when scaled by area).
- Random effects: square-level deviations and within-square repeated-measure deviations; correlations across surveys are modeled.

## 4.4 Plot Level Data
- Plot data within squares were previously summarized or treated as independent, which could bias results.
- Mixed models now accommodate square-level variation and plot-level residuals, with bootstrapping used for standard errors.
- Models can embed both square-level and plot-level random effects; bootstrapping accounts for complex variance structures.

## 4.5 Model Specification
- General model for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (Land Class i, survey k)
  - s_ij: square random effect
  - e_ijk: repeated-measures error
- Random effects assumed normal with land-class-specific variances; repeated-measure covariances vary by land class and survey pair.
- To keep models tractable with many surveys, random-effect parameters are constrained:
  - Variances (σ_i) do not vary with survey.
  - Autoregressive AR1 structure reduces repeated-measures covariance parameters to one per land class.
- AR1 model combined with bootstrap for standard errors provides robust, consistent estimation.
- Full parameterization is slow; AR1 with bootstrap is chosen for practical large-scale analyses.

## 4.6 Model Testing – Broad Habitats
- Past CS outputs included stock and changes for Broad Habitats; data from 1984, 1990, 1998 were reanalyzed.
- Old method inconsistencies (stock vs. change) were evident; modelling produced consistent estimates without the discrepancies.
- Comparing old vs. new methods showed differences generally within the existing inconsistency range; many changes were small or negligible.
- Results from modelling and old methods were broadly concordant when considering inherent old-method inconsistencies.
- Additional analyses showed the approach also feasible for plot-level data and soil data, supporting adoption for 2007.

## 5. Limitations and Implications
- Bootstrapped, model-based inference is computationally intensive; fully parameterized models are slow for large variable sets.
- AR1 model offers a good balance of stability, speed, and robustness; fixed-effect estimates are relatively robust to distributional mis-specification.
- Model selection and checking are important; in practice, an automated standard model (AR1 with bootstrap) is used for large-scale analyses.
- Distributional assumptions affect variance/covariance estimates; bootstrap estimation mitigates reliance on exact distributional forms.
- Very non-normal data (e.g., standing water) can lead to convergence to local maxima; in such cases, older methods may be preferred for those variables.
- Model-based analysis yields more precise estimates by using all information and correctly representing data hierarchy; results for any one survey are influenced by all surveys, leading to updates when new data arrive.
- This updating is conceptually different from prior inconsistencies; it reflects the continual incorporation of new information.

## 6. References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002) – foundational methodological works referenced.
- Countryside Survey documentation and related publications cited for context and methodology.

## Data Support Takeaways (for Archetype Alignment)
- Objective alignment: shift from isolated survey snapshots to a consistent, model-based framework that uses all available data across surveys to produce stock and change estimates.
- Data handling: two-tier sampling (square and plot levels) with a hierarchical structure; land-class-based weighting; handling missing data through modelling rather than ad-hoc imputation.
- Methods: AR1-based mixed-effects modelling with bootstrap for robust standard errors; explicit attention to keeping outputs on the original measurement scale.
- Practical implications: more precise and up-to-date estimates as new surveys are added; outputs can be updated retrospectively, reflecting new information; increased computational demands with automated, scalable modelling approach.
- Limitations and risk: reliance on distributional assumptions for random effects; non-normal data can challenge convergence; some variables (e.g., very non-normal freshwater data) may revert to earlier methods for reliability.