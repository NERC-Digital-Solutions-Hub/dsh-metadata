# Statistical Methodology for Countryside Survey Data

- This report describes the statistical methodology used to analyse Countryside Survey (CS) data and details the changes made for CS in 2007, following a review of the previous approach.
- Previous methods were robust but produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.
- Modelling-based, consistent estimation was found feasible and robust for Broad Habitat data; results were generally close to those from the old methods.
- The 2007 CS adopted a modelling approach that uses all available information to produce more precise (efficient) estimates of both stock and change.
- The modelling approach requires additional distributional assumptions and greater computational effort, but includes validation checks by comparing new results with the old method.
- Implementation is technically challenging, involving iterative model fitting rather than simple formulae, and required addressing CS’s complex sampling design.

- CS sampling framework
  - Information collected from a stratified sample of 1 km squares on a 15 km GB grid.
  - Two levels of sampling within each square: whole-square measurements and within-square plot measurements.
  - Land Classification (ITE) is used to stratify squares, with country-specific refinements (England, Wales, Scotland) leading to 45 Land Classes in CS2007.

- Old estimation approach
  - Stock estimates: all data from a survey.
  - Change estimates: only repeated measurements across survey pairs.
  - This led to inconsistencies where stock changes did not align with measured changes.

- Modelling approach for consistency
  - Uses complete data across surveys to estimate stock and change consistently via statistical models.
  - Applies incomplete-data techniques (mixed effects/repeated measures models) to handle missing data and correlations.
  - Requires assumptions about data distribution and random effects; these are mitigated by robust estimation and bootstrap for inference.

- Square-level data modelling
  - Core model: y_ijk = a_i_k + s_ij + e_ijk
    - a_i_k: fixed effects (land class i, survey k)
    - s_ij: square-level random effect
    - e_ijk: repeated-measures residual
  - Random effects modeled with normal distributions; variances/covariances differ by land class.
  - Full model has many random parameters; to keep it tractable, simplifications are used (e.g., AR1 structure).

- Plot-level data modelling
  - Extends square-level models to include plot-level residuals, capturing within-square plot variation.
  - Mixed models can incorporate both square and plot-level random effects, embedded in bootstrapping procedures.

- Model specification and simplifications
  - To reduce parameter burden, assumptions include:
    - Random effect variances not varying with land class (often true).
    - Random effect variances do not vary across surveys (common σ_i).
    - Autoregressive AR1 structure for covariances across surveys (one covariance parameter per land class).
  - Reduces random parameters to a manageable number (three per survey under AR1), enabling automated, large-scale application.
  - Bootstrap methods provide robust standard errors, especially when distributional assumptions are uncertain.

- Model testing: Broad Habitats
  - Analysed 1984, 1990, 1998 Broad Habitat data to compare old and new methods.
  - Old method showed stock and change inconsistencies; modelling produced consistent estimates.
  - Differences between methods were small and typically within the prior inconsistencies of the old approach.
  - Results for stock and change from the new method aligned with the summed changes across adjacent periods.

- Limitations and implications
  - Modelling is computationally intensive; large-scale analyses require automation and standardization.
  - Fixed effects estimates are robust to some mis-specifications; variance/covariance estimates are more sensitive.
  - Some very non-normal data (e.g., standing water) can challenge convergence; in such cases, old methods may be retained for those variables.
  - Analyses using data from all surveys mean that estimates for earlier surveys may be revised as new data arrives; this reflects the incorporation of additional information and represents updating rather than inconsistency.
  - Overall, the modelling approach utilises all available information and better represents the data hierarchy, yielding more precise estimates and enabling consistent estimation of stock and change.

- Practical outcomes
  - The AR1 model with bootstrap estimation is adopted for CS2007 due to its balance of stability, efficiency, and robustness.
  - Aims to provide a standard, repeatable modelling framework for large numbers of variables, improving data usability and comparability across surveys and data types (square and plot level).
  - Adoption facilitates consistent estimation across time, improved precision, and integration of cross-level data, albeit with ongoing checks and validation.