# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- The report describes the statistical methodology used for Countryside Survey (CS) data analysis and details changes made for CS data from 2007.
- Previous stock estimates used all data from a survey but changes used only repeated measurements, causing inconsistencies between stock and change estimates.
- Modelling to achieve consistent estimation (stock and change) is feasible and generally robust; differences from old methods are small compared with existing inconsistencies.
- The 2007 approach adopts consistent estimation via modelling, using all available information to produce more precise estimates.
- Modelling requires additional distributional assumptions; results, especially for small subsets, are validated by comparing with the previous methodology.
- The modelling approach is more data-efficient and yields tighter confidence intervals; future surveys can improve past estimates as new data become available.
- Implementation is technically demanding, requiring more computer time due to iterative model fitting; automated checks compare old and new methods to ensure robustness.
- For Broad Habitat data, modelling demonstrated consistent estimates across 1984, 1990, and 1998, supporting adoption of the new methodology in 2007.
- Limitations include potential sensitivity to distributional assumptions, slower computation, and the possibility of updated past estimates when new data are added; some variables (e.g., standing water) may require sticking to older methods if non-normality causes convergence issues.
- Overall, the AR1 mixed-effects modelling approach, with bootstrap standard errors, provides robust, consistent, and more precise estimates across square and plot level data.

## 1. Introduction
- This technical report gives an overview of CS sampling and analysis procedures, reviewing the previous CS methodology and detailing changes for CS2007, along with limitations and implications.

## 2. Sampling
- CS field data come from a stratified sample of 1 km squares on a GB-wide 15 km grid.
- Each selected square is mapped and measured, with two sampling levels: square-wide measures and within-square plot-level features (e.g., vegetation, soils).
- Land Classification (ITE) used for stratification has expanded over time (GB → 42 classes in CS2000 → 45 classes in CS2007), with separate national classifications for England, Wales, and Scotland.

## 2.2 Estimation
- Initial estimates of means and standard errors are calculated for each Land Class and then combined (weighted by land area) to produce region-wide means or totals.
- The method makes minimal distributional assumptions; estimates are unbiased and the Land Class estimates are treated as independent.

## 2.3 Bootstrapping
- Significance testing uses bootstrap rather than normal-theory standard errors due to potential non-normality, especially for square-level data.
- Typical bootstraps use 1,000–10,000 resamples to approximate the distribution of stock or change estimates.

## 3. Reasons for Modifications to CS Methodology
- Past reporting showed inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements.
- Missing information (e.g., unrepeated squares in newer surveys) caused discrepancies when comparing stock and change across survey pairs.
- Three potential approaches to consistency were considered; modelling (a form of consistent estimation) was found to be feasible and robust, and applicable to both square and plot-level data.
- The modelling approach uses data from all surveys, yielding consistent and more efficient estimates, though it requires more assumptions about data distributions.

## 4. Modelling

### 4.2 Modelling Basics
- Incomplete data techniques (e.g., EM, mixed effects) enable consistent estimation across survey waves but require distributional assumptions.
- For CS, mixed effects/repeated measures models are fitted to data from all surveys, with fixed effects for stock/change and random effects reflecting sampling structure.

### 4.3 Square Level Data
- Square-level measurements within each Land Class are modeled as a repeated measures (mixed) model.
- Fixed effects: Land Class means across surveys.
- Random effects: Square-level deviations and within-square, across-survey correlations.

### 4.4 Plot Level Data
- Plot-level measurements within squares can be modeled with either simple square-level summaries or more complex hierarchical models.
- Plots can be treated as independent (robust but potentially biased SEs) or included with square-level variation; both can be embedded in bootstrap procedures.
- A model extension adds a plot-level random effect to capture within-square plot variation, with correlations across surveys.

### 4.5 Model Specification
- General model for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (Land Class means per survey)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Random effects (s and e) are normally distributed with land-class-specific variances and covariances that may vary by survey.
- With multiple surveys, the number of random parameters can become large; practical reduction via AR1 assumptions (parameters constant across Land Classes; covariances follow first-order autoregression across surveys) yields a manageable model (AR1).
- Bootstrap standard errors are recommended when variability assumptions are uncertain, ensuring robust SEs for fixed effects.
- In practice, CS adopted AR1 with bootstrap SEs for stability and efficiency, validating results against the full modelling approach.

### 4.6 Model Testing – Broad Habitats
- Analyses of Broad Habitat data (1984, 1990, 1998) showed that the modelling approach removed the stock-change discrepancies seen with older methods.
- Stock estimates and changes derived from the AR1 model matched the sum of period changes and did not exhibit the inconsistencies of prior approaches.
- Comparisons indicated that, on average, new modelling changes were within the previous method’s error bounds, supporting the transition in 2007.

## 5. Limitations and Implications
- The AR1 model with bootstrap SEs is robust and reasonably fast, but fully parameterised models can be slow; AR1 provides a practical balance for large analyses.
- Model choice influences variance/covariance estimation; fixed-effect estimates are robust to some mis-specifications, but variance parameters are more sensitive.
- Non-normal data can complicate estimation; for very non-normal data, transforming to a different scale can help but complicates interpretation and back-conversion.
- In some variables with highly non-normal distributions (e.g., standing water in CS freshwater data), the old methodology may yield more reliable results; the new approach may converge to local likelihood maxima in such cases.
- Adopting a modelling approach means past survey estimates may be revised as new surveys add information; this is a natural consequence of incorporating all data and updating estimates with new information.

## 6. References
- Barr et al. (1993). Countryside Survey 1990 Main Report, DETR.
- Dempster, Laird, and Rubin (1977). Maximum likelihood from incomplete data via EM.
- Efron and Tibshirani (1993). An introduction to the bootstrap.
- Haines-Young et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002). Maximum likelihood estimation using the empirical Fisher information matrix.