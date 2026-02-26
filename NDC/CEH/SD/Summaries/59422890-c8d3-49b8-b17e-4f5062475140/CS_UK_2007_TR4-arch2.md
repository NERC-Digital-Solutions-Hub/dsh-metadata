# STATISTICAL METHODOLOGY FOR COUNTRYSIDE SURVEY DATA

## Executive Summary
- Provides description of the statistical methodology used to analyse Countryside Survey (CS) data, summarising previous methods and detailing changes adopted for CS in 2007.
- Previous estimation separated stock (all data in a survey) from change (repeat measurements only), leading to inconsistencies between stock and change estimates.
- Modelling for consistent estimation is feasible and robust; outputs differ from old methods by small amounts relative to the inherent inconsistencies in the earlier approach.
- The 2007 CS adopts the modelling approach, which uses all available data and yields more precise estimates; new data can improve past survey estimates.
- The modelling approach is computationally intensive, requiring iterative model fitting and navigating CS’s complex sampling; nevertheless it delivers a substantially improved product.
- To ensure validity, results from the new method are checked against the old method, especially for small subsets of data.
- The approach leverages bootstrapping to obtain standard errors and confidence intervals, accommodating non-normal data distributions.
- Because analyses incorporate data from all surveys, estimates for a given survey can be revised as new surveys are added, introducing updating rather than strict cross-report consistency.

## 1. Introduction
- The technical report outlines sampling and analysis procedures for CS data, reviewing the previous methodology and explaining the changes introduced for CS2007, along with limitations and implications.
- Fuller prior details are documented in Barr et al. (1993).

## 2. Overview of Previous CS Methodology
- 2.1 Sampling
  - CS field data come from a stratified sample of 1 km squares within a 15 km GB grid.
  - Two levels of sampling: square-level measurements (covering the whole square) and within-square plot-level measurements.
  - Land Classification (ITE) used for stratification; classifications expanded over years to accommodate separate reporting for England, Wales, and Scotland (45 classes in CS2007, with country-specific sub-classifications).
- 2.2 Estimation
  - Regional/national estimates derived by calculating means and standard errors for each Land Class and then combining them, weighted by land area within each class.
  - Minimal distributional assumptions; means are unbiased; independence across Land Classes assumed due to the sampling design.
- 2.3 Bootstrapping
  - Significance testing uses bootstrap rather than assuming normality, addressing skewness in some features.
  - Resampling (typically 1000–10,000 resamples) provides empirical distributions for stock and change estimates, yielding robust standard errors and confidence intervals.

## 3. Reasons for Modifications to CS Methodology
- Reporting inconsistency: past point estimates of stock and change were often inconsistent because stock used all data from a survey while change used only repeated measurements.
- Missing information across survey pairs (unrecorded or unrepeated squares) caused discrepancies when comparing adjacent and non-adjacent surveys.
- Several potential consistent approaches were identified; modelling (consistent estimation) was chosen because it uses data from all surveys, provides consistency between stock and change, and can be applied to both square and plot data.
- Modelling approach introduces additional distributional assumptions but is justifiable given robustness checks and improved efficiency.

## 4. Consistent Estimation
- The modelling approach aims to produce consistent and more precise estimates by using all available data and properly accounting for data hierarchy and missing information.
- Key modelling decisions focus on reducing the number of random-effect parameters to keep models stable and computationally feasible.

### 4.1 Square Level Data
- Data for complete 1 km squares are treated as a repeated-measures problem, using mixed effects models with:
  - Fixed effects: land-class means across successive surveys.
  - Random effects: square-level deviations and survey-to-survey residuals, including covariances.
- A basic fixed-effects model regresses the land-class mean on survey year; stock estimates come from scaling by land-class area; change estimates are differences between fitted stock values.
- Random effects capture variation among squares within land classes and correlations across surveys.
- As the number of random parameters grows with the number of surveys, simplifications are used to maintain tractability.

### 4.2 Plot Level Data
- Plot-level measurements (e.g., vegetation, soils) within squares require careful handling of hierarchical structure.
- Previous methods either collapsed to square level or treated plots as independent, risking bias or inefficiency.
- CS2000–CS2007 adopted mixed models that include both square-level and plot-level residuals, with bootstrapping for robust standard errors.

### 4.3 Model Specification
- General square-level model: y_ijk = a_iK + s_ij + e_ijk
  - a_iK: fixed effects (land-class means across surveys)
  - s_ij: square-level random effect within land class
  - e_ijk: repeated-measures residuals
- Random effects are assumed normally distributed with land-class-specific variances; residuals may have covariances that vary by land class and survey.
- A large number of random-effect parameters can be unstable; practical reductions include:
  - Common residual variance across surveys within a land class.
  - Autoregressive AR(1) structure for covariances across successive surveys.
- AR1 model with bootstrap standard errors is favored for stability, speed, and robustness, particularly when dealing with many variables.

### 4.4 Model Testing – Broad Habitats
- Broad Habitat analyses (1984, 1990, 1998; including seven habitat types) showed inconsistencies with the old method.
- Models incorporating AR1 and two-stage consistency (stock differences equal to changes derived from consecutive periods) provided consistent estimates without the prior discrepancies.
- Differences between old and new methods generally fell within prior inconsistencies; some estimates shifted modestly but remained within error bounds.
- Additional consistency checks extended to soil data (1978, 1998) and a plot-level dataset, confirming feasibility of consistent estimation across data types and scales.

### 4.5 Limitations and Implications
- AR1 modelling with bootstrap is computationally intensive but workable; fixed-effect estimates (stock/change) are robust to some mis-specifications of random effects.
- Fully parameterised models are slow for large-scale CS analyses; AR1 offers a practical balance between accuracy and computational feasibility.
- Model selection must be automated for large numbers of analyses; the AR1 approach provides a stable, scalable solution.
- Distributional assumptions for random effects can affect variance/covariance estimates; bootstrap mitigates potential biases.
- Some highly non-normal data (e.g., standing water) may converge poorly; in such cases, old methodologies may be preferred for those variables.
- Adopting a consistent modelling framework means estimates for a survey can be revised as new data are collected (updating), which differs from previously static reporting approaches.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P. et al. (1977). Maximum likelihood from incomplete data via the EM algorithm.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.