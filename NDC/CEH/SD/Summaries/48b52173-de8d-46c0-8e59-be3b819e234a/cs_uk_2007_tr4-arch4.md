# Countryside Survey in 2007

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data and explain the changes implemented for CS in 2007 to achieve consistent estimation of stock and change.

## Why a methodological shift was needed

- Previous CS reporting used stock estimates from all data in a survey and change estimates from repeated measurements, leading to inconsistencies where stock and change did not align.
- Inconsistencies arose because different data subsets were used for stock versus change, complicating interpretation.
- The aim was to obtain consistent, robust estimates that use all available information and reflect the data hierarchy.

## Core methodological changes

- Move to modelling-based consistent estimation (applies to both square-level and plot-level data) rather than solely relying on simple means and paired differences.
- Modelling approach leverages data from all surveys simultaneously, providing more precise estimates and enabling updates to past survey estimates as new data arrive.
- Implemented a robust bootstrap framework to obtain standard errors and confidence intervals, accommodating non-normal data distributions.

## Modelling framework and data structure

- Data hierarchy:
  - Square level: 1 km squares across Land Classes, with measurements per survey and possible missing observations.
  - Plot level: within-square plots provide additional vegetation/soil data.
- Square-level modelling (mixed effects/repeated measures):
  - y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects representing land-class means by survey.
  - s_ij: square-level random effects (vary by land class).
  - e_ijk: repeated-measures residuals with survey-to-survey correlations.
  - Normality assumptions for random effects; fixed effects robust to some mis-specification.
- Plot-level modelling:
  - Extends the square-level model by including an additional plot-level random effect (and corresponding residual structure) to capture within-square plot variation.
  - Both square- and plot-level models can be embedded in bootstrap procedures.
- Practical model design:
  - To keep models tractable with many land classes and surveys, random-effect parameter counts are reduced.
  - AR1 (autoregressive of order 1) structure is used for covariances to keep the number of random parameters small and stable across multiple surveys.
  - Two reductions commonly applied: common variance across surveys for each land class; AR1 covariances across successive surveys.
- Model specification highlights:
  - Use of fixed effects for land-class means by survey to derive stock estimates (scaled by land-class area).
  - Change estimates derived as differences between stock estimates, ensuring consistency under the model.
  - Bootstrap standard errors used for all fixed-effect estimates to avoid reliance on strict distributional assumptions.

## Testing, validation, and results

- Broad Habitats testing:
  - Compared old methods (stock vs. change inconsistencies) with modelling approach across 1984, 1990, 1998 data.
  - Modelling produced consistent stock and change estimates; differences with old methods were within the historical inconsistencies and generally small.
  - Stock and change estimates from modelling aligned when summed across adjacent survey periods.
- Additional checks:
  - Analyses extended to soil data and plot-level data to confirm feasibility of consistent estimates beyond square-level data.
  - Confirmed that the modelling approach could yield consistent estimates across data types, enabling a unified reporting framework.
- Outcome:
  - The modelling approach was deemed feasible and advantageous, providing more precise estimates without compromising interpretability or comparability.

## Limitations and implications

- Computational intensity:
  - Model fitting (especially fully parameterised models) can be slow; AR1 models offer a practical balance of speed and robustness.
  - Automation and standardized model choices are important for handling large numbers of variables.
- Distributional assumptions:
  - Fixed-effect estimates are robust to some mis-specification of random-effects distributions, but variance-covariance estimates are sensitive; bootstrap mitigates this.
- Reporting implications:
  - Estimates for any given survey are influenced by information from all surveys, so historical estimates may be revised as new data are added.
  - This updating is conceptually different from prior inconsistencies and is justified by the improved use of information.
- Practical considerations:
  - Non-normality (e.g., freshwater standing water) can cause convergence issues; in some cases, earlier (older) methodology results were retained for those variables.
- Overall stance:
  - Despite limitations, the AR1 modelling approach with bootstrap offers a robust, efficient, and scalable method for producing consistent stock and change estimates across CS surveys.

## Practical takeaways for data leaders

- Embrace a system-wide modelling approach to ensure consistency between stock and change across time, leveraging data from all surveys.
- Use hierarchical (square and plot-level) mixed models with a parsimonious random-effects structure (e.g., AR1) to balance accuracy and computational feasibility.
- Apply bootstrap methods to derive robust standard errors and confidence intervals in the presence of non-normal data.
- Expect updates to past survey estimates as new data become available; design reporting processes that communicate these refinements clearly.
- Validate new methods against existing benchmarks (e.g., prior habits like Broad Habitats) to confirm that improvements are within historical uncertainty and improve precision.
- Plan for computational resources and automation when applying complex modelling to large numbers of variables.