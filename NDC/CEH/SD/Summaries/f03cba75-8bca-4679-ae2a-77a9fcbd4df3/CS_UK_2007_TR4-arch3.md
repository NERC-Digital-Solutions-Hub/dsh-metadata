# Countryside Survey in 2007: Statistical methodology

## Executive purpose
- Describes the statistical methodology for analyzing Countryside Survey (CS) data.
- Summarises previous methods and details the changes implemented for CS in 2007.
- Discusses limitations, implications, and validation of the modelling approach.

## Core aims and approach
- Move from robust but non-consistent stock/change estimates to a consistent, model-based estimation framework.
- Use all available information across surveys to improve precision.
- Provide a framework that works for both square level and plot level data, with explicit data hierarchy.
- Ensure results are interpretable on the original measurement scale and are produced within a bootstrap-based uncertainty framework.

## Data structure and sampling
- Data come from a stratified sample of 1 km squares on a 15 km GB grid.
- Two sampling levels per square: square-level measurements (covering the whole square) and within-square plot-level measurements.
- Land Classification (LC) categories provide the basis for weighting and aggregation; classifications have expanded over time (GB: 32 → 42 → 45 classes, country-specific breakdowns).

## Estimation: old vs new
- Old method: stock estimates used all data from a survey; change estimates used only repeated measurements across survey pairs, causing inconsistencies between stock and change.
- New method (CS2007): modelling approach (mixed/RE models) produces consistent estimates of stock and change and uses all available data, improving precision.
- Old-and-new comparison shows most differences are within the existing level of uncertainty; the new method is more efficient and robust.

## Modelling framework: basics
- Consistent estimation achieved via mixed effects/repeated measures models fitted to data from all surveys.
- Fixed effects: represent land-class means across surveys; random effects: capture square-level and plot-level variation and their correlations across surveys.
- Requires distributional assumptions for random effects; bootstrap is used to obtain robust standard errors.

## Square level data (2-stage sampling)
- Model: y_i_j_k = a_i_k + s_i_j + e_i_j_k
  - a_i_k: fixed effects (LC means in survey k)
  - s_i_j: square-level random effect
  - e_i_j_k: repeated-measures residuals
- Variance components: differ by LC; random effects and covariances are estimated, with potentially many parameters as the number of surveys grows.
- To keep the model stable and computationally feasible, simplifications are made (e.g., AR1 structure for covariances and assuming common variance components across surveys).

## Plot level data
- Plot data within squares can be integrated by extending the square-level model with a plot-level residual/random effect.
- Two main approaches historically: aggregating to square level (robust but not fully efficient) or treating plots as independent (potential bias if hierarchy is ignored).
- The modelling framework can incorporate plot-level residuals and be embedded in bootstrap procedures for uncertainty.

## Model specification and practical considerations
- General square-level model: y_ijk = a_ik + s_ij + e_ijk with distributions for s and e.
- AR1 simplification reduces random parameters to three per LC per survey, aiding stability and speed.
- Fixed effects (stock/change) remain robust to moderate mis-specification of random-effects distributions.
- Bootstrap is preferred for SEs due to potential misspecification in parametric SEs, especially for complex models.

## Model testing: Broad Habitats
- Reassessed stock and change for Broad Habitats using old and new methods across 1984, 1990, and 1998 data.
- Old method showed inconsistencies between stock-derived change and repeated-squares change.
- AR1-based modelling provided consistent estimates; differences with the old method generally fell within old-method uncertainty, supporting adoption.
- Confirmed feasibility of consistent, cross-survey analyses at both square and plot levels.

## Limitations and implications
- Computational intensity: full parameterised models are slow; AR1 with bootstrap offers a practical balance.
- Results can update past estimates as new surveys add information, which is conceptually different from the previous, more static inconsistencies.
- Model assumptions matter for variance/covariance estimates; fixed-effect estimates are robust, but standard errors require bootstrap or careful diagnostics.
- If data are highly non-normal (e.g., standing water), convergence or estimation can be problematic; in such cases, older methods may be preferred for that variable.
- Emphasises the need for a standard, automated modelling approach for large-scale monitoring to maintain consistency across many variables.

## Implications for monitoring framework authors
- Demonstrates how to achieve consistency across time-series environmental monitoring by modelling data hierarchies and missingness, rather than relying solely on pairwise, survey-by-survey calculations.
- Highlights the value of using all available data to improve precision and to produce coherent stock/change estimates.
- Shows the trade-offs between modelling complexity and operational feasibility, advocating for a standard AR1-based modelling approach with bootstrap SEs for large-scale applications.
- Underlines the importance of validating new methods against existing data and transparently communicating any updates to past results.

## References and provenance
- Cites foundational CS reports and statistical methodology literature (e.g., EM algorithm for incomplete data, bootstrapping, mixed models, and AR1 covariance structures).
- Indicates ongoing use and evolution of Countryside Survey methodologies, with CS2007 representing a shift to consistent, model-based estimation.