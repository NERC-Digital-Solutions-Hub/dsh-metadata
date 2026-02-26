# Countryside Survey 2007 Methodology

- This technical report describes the statistical methodology used to analyse Countryside Survey (CS) data, detailing prior methods, changes made for CS in 2007, and implications.
- It compares old robust, minimal-assumption estimation with a new modelling approach aimed at producing consistent estimates of stock and change across surveys.
- The shift to a modelling framework improves precision by using all available information, but introduces distributional assumptions and greater computational demands.

## 1) Scope and aims

- Objective: describe sampling and analysis procedures for CS data and explain changes implemented for CS2007.
- Key shift: move from separate stock and change estimates (with inconsistencies) to consistent estimation via modelling.
- Benefit: more precise estimates by exploiting information from all surveys and the data hierarchy.
- Trade-off: introduced model assumptions; results validated against older methods, especially for small subsets.

## 2) Data structure and sampling design

- Data come from a stratified sample of 1 km squares at the intersection of a 15 km GB grid.
- Two levels of sampling within each square:
  - Square-level measurements (covering the whole square).
  - Plot-level measurements within each square (e.g., vegetation, soils) for finer detail.
- Land Classification (ITE) strata define squares; classification expanded over time (GB to England/Wales/Scotland-specific classes; 32 → 42 → 45 classes).
- Measurements include binary and continuous variables (areas, lengths, etc.).
- The sampling design aims to cover country-specific reporting while maintaining comparability across surveys.

## 3) From old methods to consistent estimation

- Old approach:
  - Stock estimates used data from the entire survey set.
  - Change estimates used data only from repeated measurements (between survey pairs).
  - This produced inconsistencies: stock and change did not align for the same habitat across surveys.
- Causes of inconsistencies:
  - Missing information due to new/excluded squares between surveys.
  - Stock and change drawn from different data subsets.
- Modelling-based approach (CS2007):
  - Use modelling to jointly estimate stock and change with consistent data usage.
  - Investigate several approaches; adopt modelling for consistency and efficiency.
  - Ensure results remain plausible by validating modelling outputs against older methods.

## 4) Modelling framework (basics)

- Core idea: fit mixed effects and/or repeated measures models to data from all surveys; fixed effects relate to stock/change, random effects capture data hierarchy and missingness.
- Benefits: consistent and more precise estimates for both stock and change; ability to incorporate data from all surveys, including partial data.
- Drawbacks: requires distributional assumptions; more computationally intensive than formula-based methods.

### 4.1 Square-level data

- Data treated as a repeated measures problem within land classes.
- Basic model: y_ijk = a_iK + s_ij + e_ijk
  - a_ik: fixed effects (land-class means across surveys).
  - s_ij: square-level random effect (variation of squares within a land class).
  - e_ijk: repeated-measures residual (within-square, across surveys).
- Assumes normality for random effects; within-class variances differ by land class; covariances across surveys can be modeled.

### 4.2 Plot-level data

- Plot-level measurements within squares add complexity; previous analyses varied (summarised at square level or treated plots as independent).
- Extended model includes an additional plot-level random effect (in addition to square-level) to capture plot-to-plot variation within a square.
- Both square- and plot-level models can be embedded within bootstrapping to obtain robust SEs.

### 4.3 Model specification (illustrative)

- General form for square-level data:
  y_ijk = a_iK + s_ij + e_ijk
- Distributional assumptions:
  - s_i j ~ N(0, τ_i^2) (square random effect, varying by land class)
  - e_ijk ~ N(0, σ_ik^2) with covariances between surveys
- For K surveys, fixed effects: K parameters; random effects: many (variances/covariances) but reduced in practice for stability.

### 4.4 Reducing model complexity (AR1 approach)

- To keep fitting feasible with many land classes and surveys, reduce random-effect parameters.
- Assumptions:
  - Random effect variances do not vary across surveys (σ_i common across surveys).
  - Covariances across surveys follow an autoregressive (AR1) structure: correlations decay with time, reducing covariance parameters to one per land class.
- Result: AR1 model with bootstrap SEs offers a practical, robust approach (three random-effect parameters per survey).

### 4.5 Bootstrap and standard errors

- Because variance-covariance parameters can be sensitive to distributional assumptions, bootstrapping is used to obtain standard errors.
- Bootstrap leverages the fixed effects and accommodates non-normality without fully specifying the random-effects distribution.

## 5) Model testing and Broad Habitats

- Focused testing on Broad Habitats using data from 1984, 1990, and 1998.
- Previous method produced discrepancies: stock vs. change estimates differed; differences persisted when aggregating over time.
- Modelling (AR1 mixed-effects) produced consistent stock and change estimates, with changes computed from the difference of stock estimates (or via summed inter-survey changes) that matched across periods.
- Results:
  - Comparisons showed differences between old and new methods generally within old method uncertainty.
  - New method eliminated major inconsistencies and aligned with the concept of reporting consistency over time.
- Extended checks also confirmed feasibility for soil and plot-level data, supporting adoption of the modelling approach in 2007 CS.

## 6) Limitations and implications

- Computation:
  - AR1 modelling plus bootstrapping is slower than old methods; full model fitting can be slow for large variable sets.
  - A balance between model complexity and practicality led to adopting AR1 with bootstrap as the standard.
- Robustness and distribution:
  - Fixed effects are robust to moderate mis-specification of random-effects distributions.
  - More complex models or highly non-normal data may challenge estimation; transformations are problematic due to back-conversion to the original measurement scale.
- Data updates and reporting:
  - Because analyses use data from all surveys, estimates for any given survey can be updated as new data arrive.
  - This means consistency across reporting occasions is different from previous practice; updates are expected and reflect new information.
- Practical takeaway:
  - The modelling approach leverages all available information and the data hierarchy to produce more precise, consistent estimates, at the cost of increased computation and reliance on distributional assumptions.

## 7) Practical implications for GIS and data products

- Enables more precise mapping of stock and change across Habitat classes and time, using all survey data.
- Produces consistent estimates that can be mapped over time, improving visualization of trajectories and trends.
- Supports integration of square- and plot-level data within a unified modelling framework, enhancing spatial detail in map-based outputs.
- Updated estimates as new surveys are added allow users to see revised baselines and change extents, with quantified uncertainty via bootstrap SEs.

## 8) References

- Barr et al. (1993), Countryside Survey 1990 Main Report
- Dempster et al. (1977), EM algorithm
- Efron & Tibshirani (1993), The Bootstrap
- Haines-Young et al. (2000), Accounting for nature: UK habitats assessment
- Scott (2002), Maximum likelihood with empirical Fisher information
- Additional CS2000 and related methodological reports