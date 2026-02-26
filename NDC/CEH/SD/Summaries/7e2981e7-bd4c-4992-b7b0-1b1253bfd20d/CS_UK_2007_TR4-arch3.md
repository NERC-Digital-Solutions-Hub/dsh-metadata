Countryside Survey 2007 Statistical Methodology

 Executive Summary
- Describes the statistical methods used to analyse Countryside Survey (CS) data and the changes implemented for CS2007.
- Old methods were robust but produced stock and change estimates that could be inconsistent because stock used all data from a survey while change used only repeated measurements.
- Modelling approaches demonstrated that consistent estimation is feasible and typically more precise, with differences from old methods generally small.
- The new modelling approach leverages all available data, improving precision and allowing estimation of both stock and change in a unified framework.
- Implementation is computationally demanding and technically challenging; AR1 mixed-effects models with bootstrap were adopted to balance robustness, efficiency, and automation for large numbers of analyses.
- For Broad Habitats, soil, and plot-level data, modelling provided consistent estimates across surveys and did not exhibit the inconsistencies seen with the previous methods.
- Limitations include dependence on distributional assumptions for variance/covariance parameters; bootstrap can mitigate some risks, but non-normal data can still affect results. In some non-normal freshwater cases, the old method was retained for that variable.
- Adopting a consistent, model-based approach improves use of hierarchical data, but estimates for any single survey may be updated as new surveys add information.

 1. Introduction
- This technical report outlines CS sampling and analysis procedures, reviews the previous CS methodology, and explains the rationale and details of the CS2007 changes.
- Full prior methodology details are in Barr et al. (1993).

 2. Sampling and Estimation (Overview)
- CS uses a stratified sample of 1 km squares within a 15 km GB grid; two sampling levels per square (square-wide and within-square plots) capture varied data types (binary to continuous).
- Land Class strata are defined by the ITE Land Classification, with country-specific adaptations (England, Wales, Scotland) to support separate reporting.
- Estimation originally involved combining land-class means and standard errors, weighted by land-class area to produce regional means or totals.
- The original approach made minimal distributional assumptions but assumed independence between land classes and between estimates within and across classes.

 3. Bootstrapping
- To address non-normality, especially for square-level data, CS2000 introduced bootstrap methods (1000–10,000 resamples) to derive standard errors and confidence intervals, improving inference for skewed data.

 4. Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock estimates used all survey data while change estimates used only repeats; this could cause stock and change to appear inconsistent across surveys.
- The report discusses three consistent estimation options and highlights the advantages of modelling: consistency, robustness, and efficiency, while noting potential drawbacks (more assumptions, computational load).
- The modelling approach, if implemented, would provide identical stock and change estimates based on the same data and be applicable to both square- and plot-level data.

 4.1 Modelling Basics
- Incomplete data techniques (e.g., EM-like mixed effects models) can produce consistent stock and change estimates across surveys by using data from all surveys together, but require distributional assumptions.
- Mixed-effects/repeated-measures models separate fixed effects (stock/change means by Land Class across surveys) from random effects (square-level and survey-to-survey variation). After fitting, fixed effects are transformed into stock and change estimates.
- The modelling approach needs careful handling of variance/covariance parameters (random effects), especially given many land classes and limited per-class sample sizes.

 4.2 Square Level Data
- For complete 1 km squares, data are treated as repeated-measures within Land Classes; a mixed model with fixed effects for land-class means by survey and random effects for squares and within-square repeated measures is used.
- The fixed-effects part yields stock estimates; changes are differences of stock estimates, ensuring consistency.

 4.3 Plot Level Data
- Plot-level measurements within squares can be analyzed via extended mixed models that include an additional plot-level random effect, allowing correlations within plots and squares.
- Bootstrapping can be applied to these models to obtain robust standard errors.

 4.4 Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Random effects assumed normal with land-class-specific variances; residuals vary by land class and survey with possible covariances between surveys.
- To keep models tractable with many surveys, random-effects parameterization is reduced (e.g., AR1: common variance across surveys and first-order autocorrelation of covariances) to minimize parameters while preserving essential structure.
- Bootstrap is recommended for standard errors due to potential mis-specification of variance-covariance distributions.

 4.5 Model Testing – Broad Habitats
- Analyses of Broad Habitat data from 1984, 1990, and 1998 show old methods produced inconsistencies between stock and change estimates.
- AR1 modelling with bootstrap yields consistent stock and change estimates that align with differences across adjacent survey periods; changes over longer periods (e.g., 1984–1998) become sums of adjacent changes as expected.
- Comparisons show differences between old and new methods are typically small and within old method error bounds.

 5. Limitations and Implications
- AR1 with bootstrap is computationally intensive but manageable; fixed-effect estimates tend to be robust to some mis-specification of random-effects distributions.
- Fully parameterised models can be very slow; AR1 provides a practical balance for large-scale CS analyses.
- Non-normality can affect variance estimates; bootstrap mitigates this risk for fixed effects but not entirely for all parameters.
- Very non-normal data (e.g., standing water) can cause convergence to local maxima; in such cases, old methods may be retained for that variable.
- The modelling approach uses information from all surveys, so estimates for earlier surveys can be revised when new data are added; this reflects increasing information rather than simple retroactive corrections.
- The goal is to produce more precise, coherent estimates across the survey series, while maintaining transparent reporting and comparability with previous years where possible.

 6. References
- Barr et al. (1993), CS1990 Main Report; Haines-Young et al. (2000) on UK habitat assessment; Dempster, Laird, and Rubin (1977) on EM algorithm; Efron and Tibshirani (1993) on bootstrap; Scott (2002) on maximum likelihood with empirical Fisher information.