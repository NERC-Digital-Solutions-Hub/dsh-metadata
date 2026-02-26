# Countryside Survey 2007: Statistical Methodology

- Purpose and scope
  - Describes the statistical methodology used to analyze Countryside Survey (CS) data, focusing on modifications made for CS2007.
  - Aims to provide consistent, efficient estimates of stock and change across surveys, with robust handling of incomplete data.

- Executive summary of methodological shift
  - Previous methods: robust but inconsistent, estimating stock using all data from a survey and change from repeated measurements, causing mismatches between stock and change.
  - Modelling approach: demonstrates that consistent estimation via modelling is feasible and robust, generally aligning with old methods but with greater precision.
  - Adoption: CS2007 adopts modelling for consistent estimation; results are generally within the previous error bounds, with improved precision.
  - Caveats: modelling requires distributional assumptions; results validated against old methods, especially for small subsets.
  - Computational demand: modelling is more computationally intensive; AR1 model chosen for balance between accuracy and practicality, with bootstrap for robust standard errors.

- Data structure and sampling
  - Field data from a stratified sample of 1 km squares on a GB-wide 15 km grid; two sampling levels within each square (square-level and within-square plots).
  - Land Classification: CS-appropriate stratification by ITE Land Classification, with country-specific refinements (England, Wales, Scotland) to 45 classes in CS2007.
  - Data types: varied (binary to continuous); estimates weighted by land class area to produce regional/national stock or mean estimates.

- Estimation approaches
  - Old approach: stock estimates use all data from a survey; change estimates use repeated measurements; leads to inconsistencies between stock and change.
  - Modelling approach: uses data from all surveys in a unified model to produce consistent stock and change estimates; more efficient (precise) by borrowing strength across surveys.
  - Significance testing: bootstrap is used to obtain standard errors and confidence intervals due to potential non-normality, replacing earlier normality assumptions.

- Modelling framework and components
  - General idea: fitting a mixed effects/repeated measures model to data across surveys; fixed effects capture land-class means over time; random effects capture square-level or plot-level variation.
  - Square-level data (complete squares): treated as repeated measures within land classes; fixed effects model of survey year; random effects include square-level deviations and survey-to-square correlations.
  - Plot-level data: within-square plots added complexity; models can include an additional plot-level random effect; both square and plot level analyses can be embedded in bootstrap.
  - Model specification (square level):
    - y_ijk = a_ik + s_ij + e_ijk
      - a_ik: fixed effects (land class i, survey k)
      - s_ij: square random effect
      - e_ijk: repeated measures residual
  - Variance-covariance structure
    - Random effects: s_ij ~ N(0, τ_i^2) (land-class specific)
    - Residuals: e_ijk ~ N(0, σ_ik^2), with covariances between surveys
    - Practical issue: full model with all variances/covariances is often unstable due to many random parameters; adopt simplified AR1 (autoregressive order 1) structure to reduce parameters (common σ_i across surveys; AR1 for covariances).

- AR1 modelling approach and bootstrapping
  - AR1 model reduces random effect parameters to a manageable number (three per survey per land class), enabling automated analyses across many variables.
  - Bootstrap: used to obtain standard errors and confidence intervals because variance/covariance parameters in the full mixed model can be unstable; bootstrapping relies only on fixed effects.

- Model testing and validation
  - Broad Habitats: reanalyzed data from 1984, 1990, 1998 using both old methods and AR1 modelling; finding consistent estimates between approaches and resolving previous stock-change inconsistencies.
  - Results indicate:
    - Differences between old and new methods are generally small relative to existing inconsistencies.
    - Modelling yields consistent stock and change estimates that align with the prior data, with improved precision.
  - Extends to plot-level data (soil, biomass, etc.) demonstrating feasibility of consistent estimation beyond square level.

- Limitations and implications
  - Model selection trade-offs: AR1 offers stability and efficiency but relies on distributional assumptions; bootstrap helps mitigate uncertainty in standard errors.
  - Non-normal data concerns: some variables (e.g., standing water) exhibited non-normal distributions leading to convergence or estimation issues; in such cases, older methods may be preferred for those variables, while other variables benefit from modelling.
  - Updating and reporting: because analyses use data from all surveys, estimates for any given survey may be updated as new surveys are added; this is conceptually different from the older, static reporting but reflects increased use of all available information.
  - Practicality: fully parameterised models are slow for large variable sets; AR1 with bootstrap provides a workable, robust solution for large-scale CS analyses.

- Practical outcomes for data support
  - Improved data utilization: all available information across surveys is incorporated, increasing precision of stock and change estimates.
  - Consistent estimation across survey timelines: eliminates mis-match issues between stock and change across adjacent and non-adjacent surveys.
  - Automated, scalable methodology: standardized AR1 modelling with bootstrap supports large-scale analyses with a reproducible workflow.
  - Documentation and validation: extensive checks against old methodology, supplementary analyses for specific datasets (e.g., Broad Habitats) to ensure robustness.

- References and provenance
  - Key methodological foundations sourced from early CS reports and statistical literature (EM algorithm for incomplete data, bootstrap methods, AR1 modelling concepts).
  - Emphasis on robust validation against prior methods and transparent discussion of limitations and assumptions.