# Countryside Survey 2007 Methodology

- Purpose: Describe the statistical methodology for Countryside Survey (CS) data analysis, summarize previous methods, and detail the changes implemented for CS in 2007 to achieve consistent stock and change estimates using all available data.

- Core shift: Move from robust but inconsistent conventional estimates (stock from all data vs. change from repeated data) to a modelling approach that provides consistent, more precise estimates by jointly estimating stock and change across all surveys.

- Why changes were needed: Previous reporting could show inconsistencies where changes between surveys did not equal differences in stock estimates due to using different data subsets for stock and change. Modelling addresses missing information and uses all data, reducing inconsistency and improving efficiency.

- Modelling approach: Use mixed-effects/repeated-measures models to estimate stock (land-class means per survey) and change (differences in estimated stock) with a consistent framework across square and plot data. This requires additional assumptions about data distributions but yields more precise estimates and updates past estimates as new data become available.

- Data structure:
  - Two-level sampling: 1 km squares (stratified by Land Classification) and within-square plots.
  - Data types range from binary to continuous; land classifications are country-specific (England, Wales, Scotland) with a unified framework.

- Bootstrapping: Employed to obtain standard errors and confidence intervals for square-level data due to non-normal distributions, avoiding reliance on normality assumptions.

- Modelling basics:
  - General idea: y_ijk = a_i_k + s_ij + e_ijk, where:
    - a_i_k are fixed effects (land-class means by survey),
    - s_ij are square-level random effects,
    - e_ijk are repeated-measures (plot/survey) residuals.
  - Random effects capture variability across squares and surveys; fixed effects capture mean levels by Land Class and survey year.

- Square-level data:
  - Treated as repeated-measures within land classes.
  - Simple fixed-effects regression for land-class means over surveys; stock estimates come from scaling by land-class area.
  - Random effects account for square-to-square variability and within-square correlations across surveys.

- Plot-level data:
  - Data are hierarchical (plots within squares); earlier CS analyses treated plots inconsistently.
  - Modelling includes square-level variation and can incorporate an additional plot-level random effect with correlated survey residuals.
  - Bootstrapping can be used to obtain robust standard errors for these models.

- Model specification and simplification:
  - Full model includes many random parameters; to maintain practicality, several simplifications are used:
    - Assume constant random effect spread across surveys within a land class (σ_i).
    - Use an AR1 structure for covariances (first-order autocorrelation) to reduce parameters to three per survey.
  - This AR1 model with bootstrap standard errors provides a balance of robustness, efficiency, and computational feasibility.

- Model testing and Broad Habitats:
  - Reanalysis of Broad Habitat data (1984, 1990, 1998) showed that modelling methods eliminates stock-change discrepancies seen with old methods.
  - Consistency: changes derived from stock estimates equal sums of inter-survey changes; results generally align with, and often lie within, previous inconsistency ranges.
  - Additional checks extended to soil and plot-level data, supporting feasibility of consistent estimation across data types.

- Implementation and practical considerations:
  - AR1 model is stable, relatively fast to fit, and yields robust fixed-effect estimates; however, fully parameterised models are slow and impractical for large variable sets.
  - Analyses for large CS datasets are automated using the AR1 framework; fixed effects are robust to some distributional mis-specifications, but variance/covariance estimates require bootstrap.
  - Results from new models update past estimates as new surveys are added, which can lead to small revisions to earlier findings.

- Limitations and implications:
  - Model assumptions matter; non-normal distributions can affect variance estimates, though bootstrap mitigates this for fixed effects.
  - Certain non-normal data (e.g., standing water) may converge to local maxima; in such cases, older methods may be preferred for those variables.
  - Updating past results with new data means reported estimates are not strictly fixed across reporting occasions; this reflects better use of information and is considered acceptable.
  - The shift to modelling increases precision and consistency but requires more computation and automated quality checks.

- References and validation:
  - Validation against old methods shows most changes are small and within previous error bounds; staff emphasize the improvement in precision and consistency, not the introduction of errors.
  - Methods cross-validated with established CS literature and bootstrap-based inference, ensuring robustness of fixed-effect estimates.

- Practical takeaway for data leaders:
  - Adopt a modelling framework to ensure consistency between stock and change estimates across surveys.
  - Use mixed-effects/repeated-measures models to leverage hierarchical data and all available observations.
  - Employ AR1-like simplifications to manage parameter complexity while preserving robust fixed effects.
  - Utilize bootstrapping to obtain reliable standard errors under non-normal data distributions.
  - Plan for iterative updates: new data will refine past estimates; implement automated pipelines for recalculation and verification.
  - Ensure clear documentation of assumptions and provide checks against legacy methodologies to communicate interpretability and limitations to stakeholders.