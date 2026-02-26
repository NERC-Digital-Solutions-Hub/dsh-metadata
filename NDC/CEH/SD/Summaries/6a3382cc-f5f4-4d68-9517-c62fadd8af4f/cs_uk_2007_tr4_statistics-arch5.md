# Statistical Methodology for Countryside Survey Data Analysis (CS2007)

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data, summarize previous approaches, and detail the changes introduced for CS in 2007 to enable consistent estimation of stock and change.

- Core motivation: Previous methods estimated stock using all data from a survey but change from repeated measurements only, leading to inconsistencies between stock and change estimates. Modelling-based, consistent estimation was investigated and adopted for 2007 CS data.

- Key shift in approach: Move from separate, inconsistent methods to a modelling framework that jointly estimates stock and change using all available data across surveys, improving precision and interpretability.

- Data structure and sampling:
  - Data come from a stratified sample of 1 km squares within a 15 km grid covering Great Britain.
  - Two levels of sampling: square-level measurements (whole square) and plot-level measurements within squares.
  - Land Classification (LC) stratifies squares; classifications have expanded over time (GB → England/Wales/Scotland country-specific classes).

- Estimation approach (pre-2007 vs 2007 onward):
  - Previous: Stock estimates used all data from a survey; change estimates used repeated measurements only.
  - New modelling approach: Estimate stock and change consistently via statistical models that use data from all surveys and account for missing information.

- Modelling basics:
  - Incomplete data techniques (e.g., EM algorithms) are used to handle missing information across surveys.
  - Mixed effects/repeated measures models separate fixed effects (stock and change parameters) from random effects (variation across squares and plots and inter-survey correlations).

- Square-level data modelling:
  - Treat square-level measurements as repeated measures within Land Classes across surveys.
  - Model structure: y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (LC i at survey k)
    - s_ij: square-level random effect (within LC)
    - e_ijk: repeated-measures error, with correlations across surveys
  - Random effects are typically assumed normal with LC-specific variance components.
  - Objective: obtain consistent stock estimates (via fixed effects) and change estimates (differences across surveys) while accounting for within-square and between-square variability.

- Plot-level data modelling:
  - Plots within squares are incorporated to better exploit within-square heterogeneity.
  - Previously, plot data were sometimes aggregated or treated as unrelated; the modelling framework can include an additional plot-level random effect and a plot-level residual, enabling full hierarchical treatment.
  - Bootstrapping can be used to obtain robust standard errors for plot-level analyses.

- Model specification and parameter reduction (AR1 approach):
  - Full mixed models can be highly parameter-heavy (many random effects), which can be unstable with sparse data per LC.
  - Practical reduction: assume common variance components across surveys and employ an AR1 (autoregressive order 1) structure for survey-to-survey covariances.
  - AR1 model reduces random-effect parameters to a small, fixed number (three per LC, regardless of the number of surveys), improving stability and computational tractability.
  - Fixed effects (stock and change) remain the primary targets, with estimation robust to some distributional mis-specification of random effects.

- Estimation of uncertainty:
  - Bootstrap is used to obtain standard errors and confidence intervals, especially when data are non-normal or the distributional form is uncertain.
  - Bootstrap is robust to the distribution assumptions of the random effects and is applied to provide reliable interval estimates.

- Validation and testing (Broad Habitats):
  - Re-analysis of Broad Habitat data (1984, 1990, 1998) showed that the modelling approach eliminated inconsistencies between stock and change observed under older methods.
  - Stock and change estimates from the model aligned with the aggregated, multi-survey information, and differences from the old method were generally within previous inconsistency bounds.
  - For plot-level soil data and freshwater data with non-normal distributions, the approach was tested, with some variables (e.g., standing water) continuing to rely on the older method due to convergence issues.

- Limitations and implications:
  - Computational intensity: AR1 modelling with bootstrapping is more time-consuming; however, it is feasible for large numbers of analyses when automated.
  - Model selection: While fixed effects are robust to some mis-specification, variance/covariance parameters are more sensitive; bootstrap SEs mitigate some risks.
  - Non-normal data can affect convergence and parameter estimates; transformation is possible but complicates interpretation on the original measurement scale.
  - With the integrated, multi-survey approach, estimates of any single survey may be revised as new data are added, reflecting updated information across the time series (i.e., results are not static across reporting occasions).

- Practical implications for data governance and stewardship:
  - Versioning and provenance: New surveys can update past estimates; maintain clear version history of models, data, and code to ensure reproducibility.
  - Documentation: Thorough documentation of model structure (AR1 assumptions, random effects, bootstrap procedures) and data hierarchy (square vs. plot level) is essential for auditability.
  - Automation and reproducibility: Adopt standard, automated modelling pipelines to ensure consistent analysis across many variables and surveys.
  - Metadata and lineage: Capture detailed metadata about data sources, missing data mechanisms, and modelling choices to support data user needs and governance.
  - Transparency: Provide both traditional (previous method) and model-based outputs where feasible to help users understand differences and uncertainties.
  - Data sharing and interoperability: The modelling approach depends on hierarchical data and repeated measures; ensure data stores preserve survey year, land class, square/plot identifiers, and hierarchical relationships for reproducible analyses.