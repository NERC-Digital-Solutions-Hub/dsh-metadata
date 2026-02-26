# Statistical methodology for analysis of Countryside Survey data

- Purpose: Describes the statistical methodology used to analyze Countryside Survey (CS) data, summarises prior methods, and details changes implemented for CS in 2007 to achieve consistent estimation of stock and change.

## Why changes were needed

- Previous methods: stock estimates used data from an entire survey, while change estimates used only repeat measurements, causing inconsistencies between stock and change and across survey intervals.
- The goal: obtain consistent, robust estimates for stock and change across time using all available data; improve precision; reduce mismatches between related estimates.
- Demonstrated feasibility: modelling approaches could provide consistent, efficient estimates across square and plot levels, and across Broad Habitat data.

## Modelling approach and key concepts

- Modelling vs. formula-based methods: move from minimal-assumption estimates to mixed effects/repeated-measures models that incorporate data from all surveys and the sampling hierarchy.
- Consistency: estimates of stock and change derived from the model are intrinsically aligned (e.g., change equals differences of stock estimates or sums of inter-survey changes).
- Efficiency and robustness: models utilize more information, yielding more precise estimates; fixed effects are relatively robust to distributional mis-specification; standard errors for complex models can be obtained via bootstrapping.

## Data structure and modelling details

- Data levels:
  - Square level: complete 1 km squares; treated with repeated-measures models (mixed effects) that include land-class fixed effects and square-level random effects.
  - Plot level: measurements within squares; models extended to include plot-level residuals (random effects) to capture within-square variation.
- AR1 (first-order autoregressive) structure: used to model covariances across successive surveys within each land class, reducing the number of random parameters and improving stability.
- Parameter reduction: to keep models tractable, assumptions are made to keep random-effect parameters manageable (e.g., common variance across surveys, AR1 covariances). This preserves robustness of fixed effects while simplifying estimation.

## Model specification (high-level)

- General form for square-level data:
  - y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means across surveys)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Distributions:
  - s_ij ~ N(0, τ_i^2) varies by land class
  - e_ijk ~ N(0, σ_ik^2) with covariances between surveys
- Extensions:
  - Plot-level residuals added to capture within-square variation
  - Bootstrapping used to obtain standard errors, ensuring robustness to distributional assumptions

## Model testing and validation

- Broad Habitats: re-analysis of 1984, 1990, 1998 data showed old methods produced inconsistencies; the AR1 modelling approach produced consistent stock and change estimates that aligned with differences across periods.
- Comparison findings: differences between old and new methods generally fell within old method’s error bounds; no substantial or systematic distortions introduced.
- Implication: modelling provides consistent estimates across time, with improved precision by using all available information.

## Limitations and practical implications

- Computation: model fitting is more time-consuming than traditional methods; full parameterised models can be slow, but AR1 models with bootstrap are practical for large numbers of analyses.
- Model choice: fixed effects are robust to moderate mis-specification; variance/covariance estimates are more sensitive to distributional assumptions; bootstrap mitigates some risks.
- Non-normal data: certain highly non-normal variables (e.g., standing water) may not converge well under the new method; in some cases, older methods were retained for those variables.
- Updating and reporting: because analyses use data from all surveys, estimates for earlier surveys can be revised when new data become available; this is a different kind of updating than the prior inconsistencies.

## Implications for data leadership and strategy

- Consistency across time: adopt modelling-based, consistent estimation to align stock and change, enhancing confidence in trend reporting.
- Data governance: ensure metadata and documentation reflect the hierarchical data structure (square and plot levels), the modelling assumptions, and the bootstrap procedures.
- Resource planning: allocate computational resources and automation for large-scale model fitting and automated checks against older methods.
- Transparency and communication: document assumptions, model choices (e.g., AR1), and the impact of updates on historical results; communicate uncertainties through bootstrap-based confidence intervals.
- Cross-survey integration: the approach supports incorporating information across multiple CS surveys, enabling more accurate retrospective estimates.

## Limitations and cautions for implementation

- Distributional assumptions: fixed effects are robust, but variances and covariances depend on distributional assumptions; bootstrap helps, but model validation remains essential.
- Automation risk: while a standard AR1 model is practical for large-scale deployment, careful checks are still required when adding new variables or data types.
- Scope of applicability: methods were validated on Broad Habitats and soil/plot-level data; some data types may require additional validation or alternative modelling.

## Outcome and conclusion

- Adoption: CS2007 adopts the consistent, model-based estimation approach, improving precision and coherence across stock and change estimates.
- Trade-offs: greater computational demand and reliance on modelling assumptions, but with systematic checks showing results remain within previous uncertainty bounds.
- Overall aim achieved: a more informative, efficient, and unified analysis framework for Countryside Survey data, with explicit acknowledgement of limitations and implications for ongoing data management and reporting.

## References and acknowledgments

- References include prior CS reports and methodological works on mixed models, bootstrapping, and handling incomplete data.
- Project context: Countryside Survey data analysis funded and conducted with collaboration among CEH and Defra/NERC partners; outcomes published with explicit caveats and guidance for users.