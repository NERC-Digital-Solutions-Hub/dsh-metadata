# Countryside Survey 2007: Consistent Estimation

## Executive Summary
- The report describes the statistical methodology used for Countryside Survey (CS) data analysis and details changes introduced for CS in 2007 to achieve consistent stock and change estimates.
- Previous methods were robust but produced inconsistencies: stock used all survey data while change used only repeated measurements, causing mismatches between stock and change estimates.
- Modelling approaches using data from all surveys (consistent estimation) were found feasible and robust, generally yielding estimates close to those from old methods but with greater precision.
- The new modelling approach requires additional distributional assumptions and more computing time; results are validated by comparing with previous methods, especially for small data subsets.
- The approach uses all available information and better reflects data hierarchy, improving efficiency and precision. It also facilitates analysis across surveys but means past estimates may be revised as new data are incorporated.
- Implementation is technically challenging; to deploy at scale, an automated AR1-based modelling approach with bootstrap for standard errors was adopted, balancing robustness and practicality.

## 1. Introduction
- This technical report outlines CS sampling and analysis procedures, reviews the previous CS methodology, and explains the rationale and details of the 2007 estimation changes.
- References to previous CS methodology are provided (e.g., Barr et al., 1993).

## 2. Overview of previous CS methodology
- CS field data come from a stratified sample of 1 km squares on a 15 km GB grid, with two levels of sampling: square-level measurements and within-square plot measurements.
- Land Classification stratifies squares; classifications evolved for England, Wales, and Scotland.
- Estimation in the old approach involved:
  - Means and standard errors for each Land Class, then weighting by land area to obtain regional estimates.
  - Stock (total) estimates used all data from a survey; change estimates used only repeated measurements, leading to potential inconsistencies.

## 2.3 Bootstrapping
- Significance testing under non-normal data used bootstrap methods (1000–10,000 resamples) to estimate standard errors and confidence intervals, addressing skewness and distribution concerns.

## 3. Reasons for modifications to CS methodology
- Inconsistencies arose because stock and change were derived from different data subsets.
- Several approaches to achieve consistency were considered; modelling consistently estimating both stock and change from all data was selected for its robustness and efficiency.
- The modelling approach uses data from all surveys, enabling consistent estimation across time, though it introduces reliance on distributional assumptions and greater computational demands.
- The 2007 reporting shift emphasizes timelines spanning from the first survey to the present, which highlighted the need for consistency across time and data integration.

## 4. Modelling basics
- Incomplete data techniques (e.g., mixed effects/repeated measures models) are employed to produce consistent estimates of stock and change.
- These models require assumptions about data distributions; fixed effects capture Land Class means across surveys, while random effects capture hierarchical data structure and repeated measures.
- The approach uses bootstrapping to obtain robust standard errors, mitigating sensitivity to distributional form.

### 4.1 Possible approaches
- Three potential pathways to consistency:
  - Use stock estimates from all measurements and derive change as the difference between stock estimates (robust and simple but potentially inefficient for some data types and not ideal for plot-level data).
  - Use change estimated from repeated squares, ensuring consistency but potentially larger errors and inconsistency with plot-level data.
  - Use modelling to estimate both stock and change, providing consistent and efficient estimates across data types (recommended). The AR1 model is a practical variant balancing complexity and performance.

### 4.2 Modelling basics (relevant themes)
- Mixed effects/repeated measures models handle two types of parameters: fixed effects (stock/change values) and random effects (sampling variation).
- The fixed effects reflect Land Class means over surveys; random effects capture square-level and plot-level variability and their correlations over time.
- Full models with many random parameters are unstable given CS’s many land classes; simplifications are needed (e.g., AR1 assumptions).

### 4.3 Square level data
- For complete squares, data are treated as repeated measures within Land Classes.
- A typical fixed-effects model treats land-class means across surveys as fixed effects; random effects model square-level deviations and within-square survey deviations, with within-class correlations over time.
- An AR1-like structure reduces the number of random parameters and stabilizes estimation.

### 4.4 Plot level data
- Plot data within squares add complexity; previous analyses either aggregated to square level or treated plots as independent, risking bias.
- The modelling framework can incorporate an additional plot-level random effect (with square-level variance) and still be embedded within bootstrap procedures.

### 4.5 Model specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures error
- Distributions: s_ij ~ N(0, τ_i^2); e_ijk ~ N(0, σ_ik^2) with covariances for squares across surveys; variance/covariance structures vary by land class.
- With multiple surveys, there are many random-effect parameters; to keep the model tractable, common-variance and AR1 covariance structures are used, reducing parameters substantially (AR1 model).

### 4.6 Model testing – Broad Habitats
- Historic CS outputs for Broad Habitats (1984, 1990, 1998) were re-examined with modelling to produce consistent stock and change estimates.
- Compared old methods (stock from all data, change from repeated squares) with AR1-based models; results generally aligned within the old method’s error bounds.
- The modelling approach also produced consistent estimates for plot-level and soil data, supporting adoption for the 2007 CS.

## 5. Limitations and implications
- Bootstrapping with square-level data is computationally demanding; AR1 modelling was selected for a balance of robustness and practicality.
- Fixed-effect estimates (stock/change) are robust to some mis-specification of random-effects distributions, but variance/covariance parameters are more sensitive; bootstrap mitigates this.
- Some very non-normal data can challenge convergence; in CS freshwater data, old methods were retained for standing water due to convergence issues with the new approach.
- Overall, modelling utilises all available information and the data hierarchy, producing more precise estimates.
- Data from all surveys influence any single survey’s estimates; as new data arrive, past estimates may be slightly revised, which is conceptually different from previous inconsistencies but expected with updating information.

## 6. References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Dempster, A.P. et al. (1977). Maximum likelihood from incomplete data via the EM Algorithm.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.

Disclaimer and contact information, project office details, and funding acknowledgments.