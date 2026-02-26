# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and the changes implemented for CS 2007.
- Highlights limitations of previous methods (stock vs. change estimates not using identical data), and demonstrates that modelling can provide consistent, more robust estimates by using all available data.
- Introduces a modelling approach (mixed effects/repeated measures, AR1) that yields more precise stock and change estimates across surveys, with bootstrap used for robust standard errors.
- Notes that the modelling approach requires stronger distributional assumptions and more computation, but includes validation against older methods to ensure results remain within previous uncertainty bounds.
- Indicates that results for 2007 and prior surveys may be updated as new data become available, due to using information from all surveys.

## 1. Introduction
- Technical report describing sampling and analysis procedures for Countryside Survey data.
- Reviews previous CS methodology and explains the motivation and details for changes in 2007.
- Full prior methodology details are documented in Barr et al. (1993).

## 2. Overview of Previous CS Methodology (and Issues)
- CS field data come from a stratified sample of 1 km squares across GB, with measurements at square level and within-square plots.
- Estimation combined land class-specific means with area-based weights to produce regional/national estimates.
- Previous approach estimated stock using all data from each survey and change from repeated measurements only, causing inconsistencies between stock and change estimates.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies between stock and change estimates were common and not easily interpretable.
- Three potential consistent-estimation approaches discussed; one (modelling) found feasible and robust, suitable for both square and plot level data.
- The goal: produce consistent estimates across surveys and improve precision by leveraging all available information.

## 4. Modelling Approach for Consistent Estimation
- Modelling uses incomplete-data techniques (mixed effects/repeated measures) to handle missing information due to uneven survey participation and new squares.
- Two main data levels: square-level data and plot-level data, each requiring appropriate modelling to reflect data hierarchy.

### 4.1 Square Level Data
- Treat CS as a repeated-measures design within land classes.
- Fixed effects: land-class means across surveys (regression of the variable on year/survey).
- Random effects: square-level variation within land classes; correlated survey deviations.
- Outcome: stock estimates from fixed effects; change estimates are differences in fitted stock estimates, ensuring automatic consistency.

### 4.2 Plot Level Data
- Plot data within squares can be analysed with extended models.
- Approaches include summarising to square level (robust but less efficient) or modelling plots within squares (more efficient but requires accounting for hierarchical structure).
- A combined approach allows for a plot-level residual in addition to the square-level random effect, with bootstrapping to obtain standard errors.

### 4.3 Model Specification
- General square-level model: y_ijk = a_i_k + s_i_j + e_i_jk
  - y_ijk: observation for survey k, square j, land class i
  - a_i_k: fixed effects (land class means across surveys)
  - s_i_j: square-level random effect
  - e_i_jk: repeated-measures residual
- Random effects assumed normally distributed with land-class specific variances; correlations across surveys captured via covariances.
- For multiple surveys, the model includes fixed effects for each survey and a set of random-effect variances/covariances, which can be large. To keep the model practical, simplifications are used.

### 4.4 Reducing Random-Effect Complexity (AR1 Modelling)
- To manage parameter explosion, several simplifications are adopted:
  - Random effects (variances) do not vary across surveys (common per land class).
  - Repeated-measures covariances follow an autoregressive AR1 structure (covariances depend on adjacency of surveys), reducing parameters to a small set per land class.
- Resulting model (AR1) uses three random-effect parameters per land class, regardless of the number of surveys.
- Fixed effects estimation is robust to some mis-specification; bootstrap is used for standard errors to maintain robustness.

### 4.5 Model Testing – Broad Habitats
- Used Broad Habitat data (stock and change estimates) from 1984, 1990, 1998 for testing.
- Old methodology produced inconsistencies between stock and change estimates; modelling (AR1 with bootstrap) produced consistent estimates with no results outside previous error bounds.
- The switch to modelling improves consistency between stock and change across time periods and produces closer alignment with information from all surveys.

### 4.6 Model Testing – Results and Practicalities
- When comparing old vs. new methods, most changes were small relative to old method uncertainty; a few exceptions existed but often within prior error bounds.
- Consistent estimation produced by modelling tends to yield more precise results and can update prior estimates as new data become available.
- Implementation is computationally demanding, especially for large variable sets; AR1 with bootstrap offers a practical balance between accuracy and feasibility.

## 5. Limitations and Implications
- Bootstrapped standard errors for square-level data are robust, but fully parameterised models can be slow; AR1 offers a practical compromise.
- Distributional assumptions affect variance/covariance estimates; fixed-effect estimates are robust, but standard errors from parametric calculations may be misleading for complex models.
- Non-normal data (e.g., very skewed freshwater standing-water data) can cause convergence issues; in some cases, older methods may be preferred for those variables.
- Analyses using data from all surveys mean previous survey estimates can be revised as new data become available; this is conceptually different from previous inconsistent reporting but is not unreasonable.
- The modelling approach increases data usage and consistency, enabling more precise maps and spatial analyses, but may require broader computational resources and automated modelling workflows.

## 6. Implications for GIS and Data Visualization
- Produces more precise, consistent estimates of stock and change across habitats and land classes, improving map-based representations.
- Enables integration of data across multiple survey years, improving temporal map series and trend visualizations.
- Demonstrates a robust framework for combining square- and plot-level measurements into coherent spatial outputs.
- Encourages joint consideration of data quality, sampling design, and modelling when creating map products for policy, clients, or public audiences.

## 7. References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P. et al. (1977). EM algorithm for incomplete data.
- Efron, B. and Tibshirani, R.J. (1993). Bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.