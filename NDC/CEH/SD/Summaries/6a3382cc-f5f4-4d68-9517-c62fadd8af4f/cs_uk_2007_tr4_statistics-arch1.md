# Countryside Survey in 2007: Statistical Methodology

- Purpose: Provide an overview of the sampling and analysis procedures used for Countryside Survey (CS) data, summarise previous CS methodology, and detail the changes implemented for CS in 2007, including modelling-based consistent estimation.

## Executive highlights

- Previous methods were robust but produced inconsistencies between stock (total) estimates and change estimates because stock used all survey data while change used only repeated measurements.
- Modelling approaches for consistent estimation were found feasible and robust using CS Broad Habitat data; differences from old methods were generally within existing inconsistencies.
- CS 2007 adopts a modelling-based, consistent estimation framework, which uses all available information and yields more precise estimates.
- The new approach requires more assumptions about data distributions and more computational effort; results are validated by comparing with the old method.
- Adoption of modelling for CS2007 implies that estimates for earlier surveys may be revised as new data inform previous estimates; this updating is expected to be small but present.
- The work involved significant methodological and computational challenges, but results provide a more coherent and efficient analysis framework.

## Sampling design

- CS field data come from a stratified sample of 1 km squares located at the intersections of a GB-wide 15 km grid.
- Each selected square is mapped and detailed measurements are taken, including within-square plots for vegetation, soils, etc.
- Two levels of sampling: square-level data (covering the whole square) and plot-level data (within squares).
- Land Classification (ITE) used to stratify squares; classifications have evolved (GB 32 → 42 → 45 classes) to accommodate country-specific reporting (England, Wales, Scotland).

## Estimation approach (pre-2007 context)

- Stock estimates: means and standard errors computed for each Land Class, then combined by area weighting to yield national/regional estimates.
- Change estimates: based on repeated measurements across survey pairs; used with stricter distributional assumptions.
- Result: stock estimates and change estimates could be inconsistent due to differing data subsets used.

## Bootstrapping and significance

- To address non-normality and obtain reliable confidence intervals, bootstrap methods (e.g., 1000–10,000 resamples) were used for square-level data.

## Reasons for methodological modifications

- To produce consistent estimates across time, CS2010/2007 shifted toward modelling stock and change jointly rather than treating them separately.
- Several potential approaches were considered; modelling stock and change together provides consistency and efficiency but requires more complex modelling and distributional assumptions.
- The goal was to move from inconsistency-prone methods to a framework that utilises all available data and respects the data hierarchy.

## Modelling basics

- Incomplete-data techniques (e.g., EM-like ideas) underpin the modelling approach, allowing data from all surveys to inform estimates despite missing values.
- Mixed-effects/repeated-measures models are used, with fixed effects representing Land Class means across surveys and random effects capturing between-square and within-square (repeated) variability.
- The approach requires specifying distributions for random and repeated effects and their covariances; these specifications can be challenging with many Land Classes.

## Data levels and model structure

- Square-level data:
  - Treated as a repeated-measures problem within Land Classes.
  - Basic model: y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (land-class means per survey)
    - s_ij: square-level random effects
    - e_ijk: repeated-measures residuals
  - Random effects (s and e) have normal distributions with class-specific variances; covariances across surveys are modelled.
- Plot-level data:
  - Within-square plots offer richer data but require careful handling of hierarchical structure.
  - Models can include an additional plot-level residual; bootstrapping can incorporate this structure.
  - Embedded in bootstrap procedures to obtain robust SEs.

## Model specification and AR1 simplification

- Enhanced general model: y_ijk = a_ik + s_ij + e_ijk with distributions for s and e.
- Full model includes many random parameters (variances and covariances), which can be unstable given CS’s limited per-class sample sizes.
- Practical reduction (AR1 approach):
  - Assume random effect variances do not vary with surveys; common variance across surveys for each Land Class.
  - Assume covariances follow an autoregressive AR1 structure across successive surveys.
  - This reduces random-effect parameters to a manageable number (three per survey, irrespective of the number of surveys).
- Bootstrap is still used for standard errors because fixed effects are relatively robust, but variance/covariance estimates may be sensitive to distributional assumptions.

## Model testing: Broad Habitats

- Historical data (1984, 1990, 1998) were analyzed to test modelling against traditional methods.
- AR1-based models produced consistent stock and change estimates; differences from old methods were generally small and within prior inconsistencies.
- Results for stock and change under the new approach were broadly in line with historical discrepancies, and projections showed improved internal consistency.

## Limitations and implications

- Computational demands: full parameterised models are slow; AR1 with bootstrap offers a practical balance.
- Fixed effects are robust to moderate distributional mis-specification; variance/covariance estimates are more sensitive.
- Some non-normal data (e.g., standing water) can cause convergence issues; in such cases, older methods may be preferred for those variables.
- Adoption of a fully model-based approach means estimates for any given survey may be updated as new data are added; cross-survey consistency is achieved, but previous reporting may shift slightly with new information.
- Overall, the modelling approach promises more precise estimates by using all information and properly reflecting data hierarchy, at the cost of additional computation and model checking.

## References

- Barr et al. (1993), CS1990 Main Report
- Dempster, Laird, Rubin (1977), EM algorithm
- Efron, Tibshirani (1993), Bootstrap
- Haines-Young et al. (2000), Accounting for nature: assessing habitats in the UK countryside
- Scott (2002), Maximum likelihood via empirical Fisher information

## Data and dissemination

- The CS methodology report is intended to accompany Countryside Survey data and to inform analyses and interpretation; results may lead to updated prior-year estimates as new surveys are incorporated.
- Contact: Countryside Survey Project Office, CEH Lancaster, for further information and data access.