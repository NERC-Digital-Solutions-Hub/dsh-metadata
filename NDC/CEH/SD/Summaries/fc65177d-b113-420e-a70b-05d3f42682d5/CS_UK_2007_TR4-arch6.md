# Statistical Methodology for Countryside Survey Data (CS2007)

- Objective: Describe the statistical methodology used to analyse Countryside Survey (CS) data, summarise previous methods, and detail the changes implemented for CS in 2007; discuss limitations and implications.

## Data and Sampling
- Data come from a stratified sample of 1 km squares on a 15 km GB grid.
- Two sampling levels: square-level measurements (whole square) and plot-level measurements within squares.
- Land Classification (ITE) governs strata; classifications expand to 45 classes by CS2007 with country-specific naming (England, Wales, Scotland).

## Estimation and Consistency
- Old approach: stock estimates used all data from a survey; change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Inconsistencies arise because different data subsets are used for stock and change, complicating interpretation.
- 2007 shift: adopt modelling methods to produce consistent and more efficient (precise) stock and change estimates that use information from all surveys.

## Modelling Approach
- Modelling aims to provide consistent estimates for stock and change across both square and plot level data.
- Mixed effects and repeated measures models are used to handle incomplete data and hierarchical sampling.
- Fixed effects capture land class means across surveys; random effects capture square-level and plot-level variation and correlations across surveys.

## Square-Level Modelling (CS2007)
- General model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means at each survey)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Random effects assumed normal with land-class specific variances; residuals have covariances that vary by land class and survey.
- Practical challenge: many random parameters; full model becomes unstable with increasing surveys.

## Reducing Model Complexity: AR1 Approach
- To keep models tractable, assume:
  - Random effects variances do not vary by survey (common across surveys).
  - Repeated-measures covariances follow an AR(1) process (constant correlation between successive surveys; non-adjacent surveys conditionally independent given intervening surveys).
- Result: AR1 model with bootstrap for standard errors (three random-parameter structure per land class, independent of number of surveys).
- Benefits: more stable, faster to fit, robust fixed-effect estimates to distributional mis-specification; suitable for automated, large-scale analyses.

## Plot-Level Data
- Plot data within squares are extended to include a plot-level residual, enabling a more complete representation of data hierarchy.
- Two modelling options:
  - Include square-level variation and a plot-level residual (correlated survey residuals at plot level).
  - Use bootstrapping to obtain standard errors, accommodating the hierarchical structure.

## Bootstrapping
- Used to obtain significance tests and confidence intervals without relying on normality assumptions.
- Particularly valuable when distributions are skewed or complex (non-normal data).

## Model Specification (Concept)
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
- Distributions:
  - s_ij ~ N(0, τ_i^2) varying by land class i
  - e_ijk ~ N(0, σ_ik^2) with covariances between squares
- Parameters:
  - Fixed effects: K survey means per land class
  - Random effects: many variance/covariance parameters (set is reduced under AR1 to a small, stable set)

## Model Testing: Broad Habitats
- Re-analysis of Broad Habitats for 1984, 1990, 1998 to assess stock and change.
- Old method produced inconsistencies between stock-derived change and repeat-square change; modelling approach produced consistent estimates.
- Differences between old and new methods generally small relative to old method’s own uncertainty; new approach validated against prior discrepancies.
- Extension to soil (1978 and 1998) and plot-level data supported feasibility of consistent estimation across data types.

## Practical Implications and Limitations
- Benefits:
  - Uses all available information, improves precision, and aligns stock and change estimates.
  - Provides a consistent framework across survey years and data types (square and plot level, Broad Habitats, soils).
  - Outputs are accompanied by bootstrap-based standard errors, supporting robust inference.
  - New estimates for earlier surveys can be updated as new surveys are added (reflecting new information).
- Limitations and challenges:
  - Computationally intensive; full parameterised models are slow for large variable sets.
  - AR1 approach balances model complexity with practicality; may still be slower than old methods.
  - Fixed-effect estimates are robust to some mis-specification, but variance/covariance estimates are sensitive to distributional assumptions.
  - Very non-normal data may converge to local maxima (e.g., standing water variable in freshwater data); in such cases older methods may be retained for those variables.
  - Results for any given survey can be revised as new data from subsequent surveys become available.

## Implementation and Outcomes for CS2007
- Adoption of the modelling approach implemented with AR1 and bootstrap provides robust, consistent estimates across stock and change.
- Automated, scalable analysis suitable for large numbers of variables; cross-survey coherence achieved.
- Outputs facilitate clearer interpretation and self-serve data products while enabling iterative updates as new CS data are collected.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).