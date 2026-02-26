# Statistical methodology for Countryside Survey data

- This report describes the statistical methodology used to analyse Countryside Survey (CS) data, with a focus on the changes implemented for CS in 2007.
- Previous CS estimates of stock (area or extent) used all data from a survey, while change estimates used only repeated measurements, leading to inconsistencies between stock and change.
- Modelling approaches (consistent estimation) were investigated and found to be feasible and robust, producing estimates that align stock and change and are generally more precise than the old methods.
- The new methodology uses all available information and accounts for the hierarchical survey design, improving precision but requiring more computation and additional distributional assumptions.
- The AR1 (autoregressive of order 1) mixed-effects model, combined with bootstrapping for standard errors, was selected as a practical, robust modelling framework for CS2007.
- Validation against earlier methods showed that differences between old and new estimates typically fall within the existing inconsistencies of the old approach; broad habitat analyses supported adopting the modelling approach.
- The new approach was applied to both square-level and plot-level data, enabling consistent estimation across data types and across time.
- Key implications: estimates for any given survey may be updated as new surveys contribute information; results are more precise but depend on distributional assumptions and model specification. Computational demands are higher, and model selection is simplified for large-scale automated analyses.

## Executive summary of methodology and rationale

- Problem: Inconsistencies between stock and change estimates due to using different data subsets for stock vs. change.
- Solution: Shift to modelling-based, consistent estimation that uses data from all surveys and handles missing information through mixed-effects/repeated-measures models.
- Data structure: CS data are hierarchical, with square-level data (1 km squares) and within-square plot-level data.
- Modelling goals: Obtain stock and change estimates that are internally consistent across time and data levels, with improved precision.
- Methods: Use AR1 mixed-effects models to reduce the number of random-variance parameters; employ bootstrap to obtain robust standard errors due to potential non-normality.
- Validation: Compare with old methods and across Broad Habitats data; ensure results are within previous inconsistencies and are robust to model choice.
- Outcome: Adoption of the new modelling approach for CS2007, with explicit acknowledgment of computational and data-distribution considerations.

## 1. Introduction and context

- The report outlines sampling and analysis procedures for CS data, contrasts previous methodology with the 2007 changes, and discusses implications and limitations.
- Prior documentation and methods are detailed in earlier CS reports.

## 2. Previous methodology and motivation for change

- Stock estimates were based on all data from a survey; change estimates were based on repeated measurements only.
- This mismatch caused inconsistencies between stock and change estimates, especially when comparing non-adjacent surveys.
- New methods aim to produce consistent estimates by modelling data across all surveys and imputing missing information through appropriate statistical techniques.

## 3. Modelling approach for consistent estimation

- Modelling via mixed effects and/or repeated measures allows simultaneous estimation of stock and change using all available data.
- This approach relies on distributional assumptions for random effects and requires more complex computation than the old methods.
- To keep the analysis practical for CS’s large number of variables, simplifications to the random-effects structure are proposed and tested.

## 4. Data levels and model structures

- Square level data (1 km squares): treated as repeated measures within land classes; a mixed model with fixed effects (land-class means over surveys) and random effects (square-level and within-square repeated measures) is used.
- Plot level data: data within squares are more complex; models extend by adding plot-level residuals to account for within-square variation.
- Model types:
  - AR1 (autoregressive) model reduces random effects parameters by assuming constant variance within land classes across surveys and first-order autocorrelation between successive surveys.
  - Alternative specifications are discussed, but AR1 provides a practical balance of robustness and computational efficiency.

## 5. Model specification and estimation

- General square-level model: y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land class means over surveys), square random effects s_ij, and repeated-measures residuals e_ijk.
- Variance/covariance structures are defined per land class, with covariances between surveys modeled (e.g., AR1).
- Random effects are constrained to keep the model identifiable and computationally tractable; the AR1 model is favored for stability and efficiency.
- Bootstrap is used to obtain standard errors robust to potential non-normality in data, especially when variance-covariance estimates are uncertain.

## 6. Model testing and application to Broad Habitats

- Broad Habitat data (from 1984, 1990, 1998, and later) were reanalyzed with the modelling approach.
- Previously observed inconsistencies between stock and change estimates disappeared under the modelling approach; differences between old and new estimates remained within the level of historical inconsistency.
- The modelling approach was also validated on soil (plot-level) data, supporting a consistent treatment across square and plot levels.
- Conclusion: adopt the modelling approach for CS2007 analyses.

## 7. Limitations, implications, and practical considerations

- Limitations:
  - Results depend on distributional assumptions for random effects; mis-specification can affect variance estimates.
  - Fully parameterised models can be computationally slow; AR1 offers a practical alternative.
  - Very non-normal data can cause convergence issues (e.g., freshwater standing water data) leading to occasional retention of older methods for those variables.
- Implications:
  - Analyses use data from all surveys; estimates for earlier surveys may be revised as new data become available.
  - The approach provides more precise estimates and consistent interpretation across time, but with a conceptual shift in reporting (updates to past estimates as new information arises).
- Practicalities:
  - Implementations rely on automated procedures to handle large numbers of analyses; bootstrap-based standard errors provide robustness.
  - The need to balance model complexity with computational feasibility drives the choice of AR1 as the standard specification.

## 8. References

- Barr et al. 1993; CS1990 main report
- Dempster, Laird, Rubin 1977; EM algorithm
- Efron, Tibshirani 1993; Bootstrap
- Haines-Young et al. 2000; Accounting for nature: UK habitats
- Scott 2002; Maximum likelihood estimation with empirical Fisher information