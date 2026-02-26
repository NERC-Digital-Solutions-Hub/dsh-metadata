# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical approach used to analyse Countryside Survey (CS) data, with a focus on changes introduced for CS2007 to achieve consistent estimates of stock and change across surveys.
- Previous methods were robust but produced inconsistencies because stock used all data from a survey while change used only repeated measurements; modelling provides consistency and greater precision by using all available information.
- Modelling (AR1 mixed-effects/repeated-measures approach) is applied to square- and plot-level CS data, producing more precise estimates but requiring stronger distributional assumptions and greater computational effort.
- Extensive validation showed the new modelling approach yields estimates within the uncertainty of the old method, while offering improved efficiency; results for small data subsets are carefully checked against prior methods.
- Adoption of the modelling framework means past survey estimates can be updated as new data arrive, reflecting overall information growth; this can slightly revise earlier results.
- Practical considerations include the complexity of implementation, need for automated analyses across many variables, and reliance on bootstrap methods for robust standard errors.

## 1. Introduction (overview)
- Purpose: outline sampling and analysis procedures for CS data, review prior methodology, explain changes for CS2007, discuss limitations and implications.
- Reference to fuller descriptions in earlier CS reports.

## 2. Overview of Previous CS Methodology
- Sampling: two-level design—measurements within 1 km squares on a 15 km GB grid; Land Classification (ITE) stratification evolved from 32 to 42 to 45 classes (England, Wales, Scotland reported separately).
- Estimation (old approach): stock estimates used all data from a survey; change estimates used only repeated measurements; this caused inconsistencies between stock and change.
- Bootstrapping: used to estimate confidence intervals and significance due to concerns about normality, especially for square-level data.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies between stock and change arose from using different data subsets for stock vs. change.
- New methods aimed to provide consistent estimates over time by integrating data across surveys; modelling also allows using all available information and addressing hierarchical data structure.
- Considered alternative approaches (e.g., relying solely on repeated squares or using stock differences) but found modelling to be the most robust and efficient path, despite its complexity.

## 4. Consistent Estimation
### 4.1 Possible Approaches
- Stock and change can be estimated via different strategies; modelling offers consistency and robustness, but requires stronger assumptions and computational resources.

### 4.2 Modelling Basics
- Uses mixed-effects/repeated-measures models to integrate data across surveys, enabling consistent stock and change estimates.
- Fixed effects: functions of stock/change across surveys.
- Random effects: reflect sampling structure (square-level residuals, plot-level residuals as needed); data are hierarchical and correlated across time.

### 4.3 Square Level Data
- Data treated as a random sample of squares within each Land Class; a repeated-measures (mixed) model is used.
- Fixed effects: land-class means over time (surveys).
- Random effects: square-level deviations and survey-to-survey correlations.

### 4.4 Plot Level Data
- Plot data within squares added complexity; earlier analyses either aggregated to square level or treated plots as independent, risking bias.
- Models can include an additional plot-level random effect; bootstrapping can be applied to either square- or plot-level analyses.

### 4.5 Model Specification
- General form: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square random effects
  - e_ijk: repeated-measures errors
- Distributional assumptions specify normality for random effects and residuals; variance/covariance structures are complex and can be reduced via simplifying assumptions.

### 4.6 Model Testing – Broad Habitats
- Analyses of Broad Habitats (1984, 1990, 1998) showed previous stock/change inconsistencies; modelling (AR1) yielded consistent estimates with comparable results to the old approach within uncertainty.
- Compared changes derived from stock estimates vs. repeat-squares; inconsistencies reduced or eliminated under the modelling framework.
- Confirmed feasibility of consistent analyses for soil data and plot-level data as well, supporting adoption of the new methodology for CS2007.

## 5. Limitations and Implications
- AR1 modelling with bootstrap is robust for fixed effects but more data- and time-intensive; full parameterised models are slow for large variable sets.
- To keep analyses practical for CS’s large variable set, the AR1 approach provides a balance of stability, speed, and robustness.
- Model assumptions (distribution of random effects, covariances) affect variance estimates; bootstrap can mitigate some risks.
- Some data (e.g., freshwater standing water) exhibited non-normality that challenged the modelling approach; in such cases, older methodologies were retained for those variables.
- Moving to a model-based framework means past estimates can be revised as new data arrive, reflecting new information; this is conceptually different from the prior inconsistent reporting but is not deemed unreasonable.

## 6. References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird & Rubin (1977); Efron & Tibshirani (1993); Scott (2002).