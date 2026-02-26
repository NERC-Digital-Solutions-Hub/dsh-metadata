# Statistical methodology for Countryside Survey data

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data, summarising past methods and detailing changes for CS in 2007.
- Previous methods were robust but produced inconsistencies: stock was estimated using all survey data, while change used only repeated measurements, leading to mismatches between stock and change estimates.
- Modelling with consistent estimation for Broad Habitat data demonstrated feasibility and robustness; differences from old methods were generally small.
- The 2007 CS adoption implements modelling-based, consistent estimation, using information from all surveys to improve precision; new data can improve past estimates, though changes are expected to be small.
- The modelling approach requires distributional assumptions; results, especially for small subsets, were validated by comparison with the previous methodology.
- Implementation is technically challenging and computationally intensive, as it fits iterative models rather than applying formulaic means; nonetheless it yields a substantially improved product.
- Adoption of the modelling approach enables more precise estimates and a unified treatment across square and plot-level data, with results stored and shared via appropriate portals.

## 1. Introduction
- The report provides an overview of CS sampling and analysis procedures, reviewing the previous methodology and explaining the 2007 changes.
- CS uses a two-level sampling framework: 1 km squares across GB on a 15 km grid, with additional plot-level measurements within squares.
- Strata for square selection are defined by Land Classification, with country-specific refinements (England, Wales, Scotland) for reporting.

## 2. Overview of Previous CS Methodology
- Regional/national estimates were formed by combining land-class means, weighted by land-area within each class.
- Stock estimates used all data from a survey; change estimates used only repeated measurements, causing potential inconsistencies between stock and change.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock and change were derived from different data subsets.
- Several approaches to achieve consistency were considered; modelling was identified as feasible and advantageous for producing consistent and efficient estimates across both square and plot data.
- The 2007 reporting shift emphasises timelines spanning from the first survey to the present, making consistency across all periods more critical.

## 4. Modelling Approach (Consistent Estimation)

### 4.1 Modelling basics
- Incomplete data techniques (mixed effects/repeated measures models) allow stock and change to be estimated consistently using data from all surveys.
- Models require distributional assumptions for random effects and residuals; fixed effects estimate stock/change, while random effects capture sampling variation.
- Two common model forms are used for square- and plot-level data, with bootstrapping providing robust standard errors.

### 4.2 Square-level data
- Treats CS square-level data as repeated measures within land classes.
- Fixed effects: land-class means across surveys.
- Random effects: square-level deviations; correlations across surveys modeled (often via AR1 structure) to reflect repeated-measures variance.
- The model yields stock estimates from fixed effects and change estimates from differences in fitted stock across surveys.

### 4.3 Plot-level data
- Plot-level data within squares are richer but more complex; prior analyses either summarized to square level or treated plots as independent, risking biased SEs.
- Modelling can include a plot-level residual in addition to the square-level random effect, with bootstrapping applied to obtain SEs that reflect the full data hierarchy.

### 4.4 Model specification
- General square-level model: y_ijk = a_iK + s_ij + e_ijk, where a_iK are fixed effects (mean values per land class across surveys), s_ij are square random effects, and e_ijk are repeated-measures residuals.
- random effects: typically assume normality with land-class-specific variances; repeated-measures covariances modeled across surveys.
- To keep the model tractable, random-parameter counts are reduced (e.g., AR1 structure with common variance across surveys) without substantially sacrificing fixed-effect accuracy.

### 4.5 Model testing – Broad Habitats
- Analyses of 1984, 1990, 1998 Broad Habitats showed old methods produced inconsistencies between stock and change.
- Fitting AR1 models to the three surveys yielded consistent stock and change estimates; changes over longer periods aligned with sums of interval changes.
- Comparisons between old and new methods indicated differences generally small and within old method error bounds.

### 4.6 Practical considerations
- AR1 with bootstrap SEs provides robust, consistent estimates while remaining computationally feasible for large numbers of analyses.
- Full parameterization can be slow; AR1 offers a practical balance between accuracy and run-time.
- Analyses across all surveys mean past estimates can be updated with new data, which may revise earlier results slightly.
- A dual-reporting approach (new modelling vs. old method) was used to verify improvements and ensure comparability.

## 5. Limitations and Implications
- Bootstrapping is robust to non-normality but is computationally demanding; fixed-effect estimates are robust to moderate mis-specification of random effects.
- Some variables with highly non-normal distributions (e.g., standing freshwater) may converge to local maxima; in such cases, old method results may be preferred.
- The modelling approach is more data-hungry and sensitive to distributional assumptions; for large-scale CS analyses, a standard, automated AR1-based model with bootstrap SEs is recommended.
- Results are inherently updated as new surveys are added; estimates for earlier surveys may change slightly to reflect additional information.
- The approach enhances precision and consistency but requires careful interpretation when comparing results across reporting occasions.

## 6. References
- Barr et al. (1993), CS1990 Main Report
- Dempster, Laird, Rubin (1977), EM Algorithm
- Efron, Tibshirani (1993), Bootstrap
- Haines-Young et al. (2000), Accounting for nature: assessing habitats in the UK countryside
- Scott (2002), Maximum likelihood estimation using the empirical Fisher information matrix