# Countryside Survey 2007 Statistical Methodology

- Purpose and scope
  - Describes the statistical methodology used to analyze Countryside Survey (CS) data.
  - Explains changes implemented for CS in 2007 to achieve consistent estimation of stock and change, using all available data and data hierarchy.

- Why changes were needed
  - Earlier methods computed stock using all data from a survey but change from repeated measurements only, causing inconsistencies between stock and change estimates.
  - Modelling approaches showed that consistent estimation was feasible and broadly robust, with differences from old methods generally within existing inconsistencies.

- Modelling approach adopted
  - Replace previous gap between stock and change estimation with a modelling framework that yields consistent and more efficient estimates.
  - Use mixed effects and/or repeated measures models (AR1 variant) to handle data from all surveys, accounting for hierarchical structure (land classes, squares, plots).

- Data structure and levels
  - Two-level sampling: 1 km squares across GB, stratified by Land Classification; measurements at square level and within-square plots.
  - Land Classification adapted over time for country reporting (England, Wales, Scotland).

- Estimation methodology
  - Stock estimates come from fixed effects across surveys scaled by land class area; change estimates derived from model-based stock and/or repeated measurements, ensuring internal consistency.
  - Weighting by Land Class area remains essential for regional estimates.
  - Prior methods assumed independence across Land Classes; modelling introduces dependence structure via random effects and repeated measures.

- Square level data modelling
  - Repeated measures mixed model: fixed effects for land-class means per survey; random square effects; correlations across surveys within squares.
  - Provides consistent stock and change estimates after model fitting.

- Plot level data modelling
  - Extends square-level models to include plot-level residuals, capturing within-square plot variation.
  - Models can embed within bootstrapping procedures to obtain robust SEs.

- Model specification and simplification
  - General form: y_ijk = a_ik + s_ij + e_ijk, with a_ik fixed effects for land-class means, s_ij square random effects, e_ijk repeated-measures residuals.
  - Random effects variances and covariances are constrained to reduce parameter counts (e.g., AR1: common variance per land class, one covariance parameter per land class).
  - AR1 model reduces random parameters to three per land class, balancing fit quality with computational practicality.

- Distributional assumptions and robustness
  - Fixed effects are robust to moderate mis-specification of random-effect distributions; bootstrap estimation of standard errors remains robust for complex models.
  - Complex, fully parameterized models are slow; AR1 with bootstrap is favored for large-scale analyses.

- Model testing and validation (Broad Habitats)
  - Re-analysis of historic Broad Habitat data (1984, 1990, 1998) shows consistent estimates without the prior stock-change discrepancies.
  - Differences between old and new methods generally fall within old method’s error bounds.

- Implications and updating results
  - Results for any survey can be updated as new data arrive; past estimates may shift slightly, reflecting additional information.
  - Analyses involve data from all surveys, making cross-occasion consistency different from earlier reporting, but more statistically coherent.
  - Strong preference for a standard, automated modelling approach to enable consistent analyses across many variables.

- Practical considerations and limitations
  - Computationally intensive; AR1 bootstrap approach is robust but slower than older methods.
  - Model choice is crucial; fixed effects are robust, but variance/covariance estimates are more sensitive to distributional assumptions.
  - Very non-normal data (e.g., standing water) may require alternative handling; in some cases, older methodologies were retained for specific variables.
  - Outputs are on the original measurement scale; transformations for modeling would complicate back-transformations.

- Data products and for data support
  - Produces stock and change estimates with bootstrap-based standard errors and confidence intervals.
  - Uses all available information and the hierarchical structure to deliver more precise estimates.
  - Encourages automated, repeatable analyses across variables and surveys to facilitate data exploration and end-user self-service.

- References and funding
  - Builds on prior CS methodologies and statistical techniques (e.g., mixed models, bootstrap, EM/maximum likelihood foundations).
  - CS2007 analyses funded by Defra and NERC, with methodology detailed in the report.