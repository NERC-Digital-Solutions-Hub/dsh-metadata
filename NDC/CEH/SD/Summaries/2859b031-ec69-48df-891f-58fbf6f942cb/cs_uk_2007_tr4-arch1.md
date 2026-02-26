# Description of the statistical methodology used for the analysis of Countryside Survey data

## Executive Summary
- The report describes the statistical methodology for Countryside Survey (CS) data analysis and details changes implemented for CS in 2007.
- Previous methods used minimal assumptions and were robust but produced inconsistencies: stock estimates used all data, while change estimates used repeated measurements only.
- Modelling methods for consistent estimation using CS Broad Habitat data showed they are feasible and generally robust; differences from old methods were small.
- A modelling approach (consistency-focused) has been adopted for CS 2007, utilizing more information and yielding more precise estimates.
- Modelling requires additional distributional assumptions; results for small subsets are validated against the previous methodology to check validity.
- The new approach uses all available information, improving precision and potentially updating past surveys as new data arrive.
- Implementation is computationally intensive, especially due to iterative model fitting and CS’s complex sampling; AR1 modelling with bootstrapped standard errors was selected for practicality and robustness.
- The approach was tested against Broad Habitat data and plot-level data, showing close alignment with-old results within stated uncertainties, and was adopted for 2007 CS.

## 1. Introduction
- CS data come from a stratified sample of 1 km squares on a 15 km GB grid; measurements occur at two levels: square-wide and within-square plots; data types range from binary to continuous.
- Land Classification (ITE) strata evolved: 32 classes (GB), then 42 for CS2000, and 45 for CS2007 due to country reporting needs (England, Wales, Scotland with related sub-classifications).
- The basic estimation approach aggregates land-class means (with areas as weights) to obtain regional or national estimates; this method makes minimal distributional assumptions and assumes independence of Land Class estimates.

## 2. Overview of Previous CS Methodology
- Estimation involved means and standard errors by Land Class, then combining them to regional/national estimates weighted by land area.
- Means and standard errors were unbiased; however, stock estimates used all data from a survey while change estimates used only repeated measurements, causing inconsistencies between stock and change.

### 2.1 Sampling
- Two-level sampling: squares and within-square plots; data include varied variable types; country-specific land classifications affect stratification.

### 2.2 Estimation
- Stock and change estimates derived from Land Class means, with area-based weighting; assumption of independence across Land Classes.

### 2.3 Bootstrapping
- Significance testing shifted from normality assumptions to bootstrap due to skewness concerns, enabling non-normal distributions for square-level data.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies in past reporting (stock vs. change discrepancies) were recognized as arising from different data usage (stock from all squares vs. change from repeats).
- Emphasis shifted in CS2007 from adjacent-survey changes to timelines spanning from the first survey to the present; this highlighted potential inconsistencies and motivated consistent estimation.
- Modelling-based, consistent estimation was explored and found to be feasible and robust, leading to adoption for 2007 CS.

## 4. Consistent Estimation

### 4.1 Possible approaches
- Three potential consistent-estimation options from survey pair data:
  - Use stock estimates from all data and compute change as the difference between stock estimates (robust and easy to implement but potentially inefficient for some variables and not directly applicable to plot data).
  - Use change from repeated squares (consistent but potentially less efficient).
  - Modelling approach to jointly estimate stock and change (consistent and efficient; applicable to square and plot data but requires distributional assumptions).

### 4.2 Modelling basics
- Missing data in CS are handled via mixed effects/repeated measures models; data are analyzed with a combination of fixed effects (survey/stock estimates) and random effects (squares, plots) reflecting the sampling design.
- Fixed effects capture Land Class means across surveys; random effects model square-level and plot-level variation and their correlations across surveys.
- Estimation yields stock and change from model parameters; requires careful handling of variance/covariance structures.

### 4.3 Square level data
- For complete squares across surveys, repeated-measures mixed models are used.
- Fixed effects: Land Class means by survey; Random effects: square-level deviations and survey-to-survey residuals.
- Increasingly large numbers of random parameters with more surveys can destabilize fits; model simplifications help maintain robust estimates.

### 4.4 Plot level data
- Plot-level data within squares can be modeled with an additional plot-level random effect, allowing correlations to vary within squares.
- Models for square-level and plot-level data can be embedded in bootstrapping to obtain robust standard errors.

### 4.5 Model specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square random effect
  - e_ijk: repeated-measures random effect
- Distributional assumptions: random effects assumed normal with land-class-specific variances; repeated effects have variances and covariances that vary by land class and survey.
- Complexity grows with the number of surveys; reducing random parameters is necessary for practicality.

### 4.6 Model testing – Broad Habitats
- Broad Habitat data (from 1984, 1990, 1998) were used to test modelling against old methods.
- Old method inconsistencies (stock vs. change) were evident; modelling (AR1) produced estimates equal to the difference of stock estimates and changes from consecutive periods, eliminating the discrepancies.
- Comparisons showed most differences between old and new methods were within old-method error bounds; changes were generally small.
- Partial checks indicated consistency improvements without large deviations; data from 2007 CS adopt this modelling approach.

## 5. Limitations and Implications
- AR1 modelling with bootstrap is robust for fixed effects but introduces more computation, especially with large numbers of variables.
- A standard AR1 model was chosen for automation across many analyses; checks confirm performance but full parameterization can be slow.
- Model is sensitive to distributional assumptions; non-normal data may affect parameter estimates more than fixed effects.
- For highly non-normal data (e.g., standing water), convergence issues led to retaining the old method for that variable.
- Benefits include using all available information, representing data hierarchy, and potentially more precise estimates.
- A notable implication: as new surveys are added, past survey estimates can be updated; thus estimates are not fixed across reporting occasions but expected to shift slightly with new data.
- Automated application across many analyses is emphasized to ensure robustness and consistency.

## 6. References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P. et al. (1977). Maximum likelihood from incomplete data via the EM Algorithm.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.