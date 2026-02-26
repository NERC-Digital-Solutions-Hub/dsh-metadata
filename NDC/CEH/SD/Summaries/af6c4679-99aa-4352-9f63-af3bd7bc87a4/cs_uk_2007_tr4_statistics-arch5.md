# Statistical methodology for the analysis of Countryside Survey data

## Executive context for data stewardship
- Transition from earlier, inconsistent stock/change estimation to a modelling-based, consistent estimation framework for CS data (CS2007).
- Aims to use all available information, improve precision, and provide coherent estimates across surveys.
- Recognition of higher computational demands and the need for robust validation and documentation.

## What was changed for CS2007
- Move to modelling techniques (mixed effects/repeated measures) to produce consistent estimates of stock and change across surveys.
- Use of AR1-based reduced-parameter models to manage complexity and ensure stability across many land classes and surveys.
- Adoption of bootstrapping to obtain robust standard errors and significance without heavy reliance on normality.
- Estimation now leverages data from all surveys; past estimates may be revised as new information becomes available.

## Data structure and sampling context
- CS data come from a stratified sample of 1 km squares across GB, with measurements at two levels: square-wide and within-square plots.
- Land Classification (ITe) used to define strata, evolving from 32 classes (GB) to 45 classes (CS2007) with national adaptations (England, Wales, Scotland).
- Measurements vary from binary to continuous; estimates are combined across Land Classes weighted by land area.

## Modelling approach (square and plot level)
- Square-level data:
  - Treated as repeated-measures within Land Classes.
  - Basic fixed effects model for mean values by survey, with square-level random effects to capture within-square variation across surveys.
  - Stock estimates derived from fixed effects; change estimates are differences of fitted stock values and are thus automatically consistent.
- Plot-level data:
  - Acknowledges within-square heterogeneity; prior methods either aggregated plots or treated plots as independent, risking biased SEs.
  - Extended models include plot-level random effects in addition to square-level effects; both square and plot-level models can be bootstrapped.
- Model specification and reduction:
  - General y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects (land-class means by survey), s_ij are square random effects, e_ijk are repeated-measures residuals.
  - Random effects: aim to reduce parameters (e.g., AR1 structure) so random variance/covariance parameters do not explode with more surveys.
  - AR1 (first-order autoregressive) assumptions reduce random parameters to a small, stable set per land class.
- Distributional considerations:
  - Fixed effects are robust to some mis-specification of random-effect distributions.
  - Bootstrapping provides robust SEs when parametric SEs may be unreliable due to distributional issues.

## Model testing and validation (Broad Habitats)
- Re-analysis of Broad Habitats across 1984, 1990, 1998 to compare old methods with modelling approach.
- Old method produced inconsistencies between stock and change estimates; new modelling approach yielded consistent estimates with no results outside prior error bounds.
- Differences between old and new methods were generally small relative to existing inconsistencies, supporting adoption.
- Additional checks extended to soil data (1978, 1998) and plot-level data, confirming feasibility and consistency across data types.

## Limitations and implications
- Computational intensity: AR1 modelling with bootstrapping is slower than previous methods; full automation is necessary for large variable sets.
- Model dependence: fixed-effect estimates are robust, but variance/covariance estimates are sensitive to distributional assumptions; bootstrapping mitigates this.
- Non-normal data challenges: some variables (e.g., standing water) can cause convergence or local maxima issues; in such cases, older methods may be preferred for those specific metrics.
- Data updates across surveys: as new surveys add information, past survey estimates may be revised; this reflects improved information use rather than errors in earlier reporting.
- Practical takeaway: the modelling approach increases precision and consistency but requires careful documentation, metadata, and automated workflows for routine analyses.

## Practical implications for data governance and reuse
- Improved data provenance: clear documentation of modelling choices (AR1, bootstrapping, survey structure) enhances reproducibility and auditability.
- Consistent reporting framework: stock and change estimates derived from the same modelling basis across surveys support comparability over time.
- Metadata and lineage: records should capture data hierarchy (square vs plot level), land-class definitions, sampling designs, and covariance assumptions.
- Update strategy: plan for iterative re-estimation as new CS surveys are completed, with transparency about how past results may shift.
- Resource planning: allocate computational resources for modelling pipelines and bootstrap procedures to maintain timeliness.

## Bottom-line takeaways for Data Stewards
- For large, multi-survey datasets, modelling-based, consistent estimation can significantly improve precision and coherence of long-term trends.
- Mixed-effects models with AR1 covariance offer a practical balance between statistical rigor and computational feasibility across many land classes and survey waves.
- Bootstrapping provides robust uncertainty quantification in the presence of non-normal data and complex data structures.
- Comprehensive documentation, automation, and metadata are essential to support reproducibility, data sharing, and governance of evolving survey datasets.