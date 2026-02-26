# Countryside Survey 2007: Consistent Estimation and Modelling Methodology

## Executive Summary
- The report describes the statistical methodology for Countryside Survey (CS) data analysis and details changes made for CS in 2007 to achieve consistent estimation.
- Previous methods were robust but produced inconsistencies: stock estimates used all data from a survey while change estimates used only repeated measurements, leading to mismatches between stock and change.
- Modelling approaches using Broad Habitat data showed that consistent estimation via modelling was feasible and robust; differences from old methods were generally within existing inconsistencies.
- The 2007 methodology adopts modelling for both stock and change, improving precision by utilizing all available information and properly reflecting data hierarchy.
- The modelling approach requires additional distributional assumptions; results are checked against the old method, especially for small subsets.
- While more computationally intensive, the new approach yields more precise estimates and can update past estimates as new data become available.
- Implementation highlighted practical challenges, but the AR1 modelling approach with bootstrap was found to be a practical, robust solution for CS data.

## 1. Introduction
- This technical report provides an overview of CS sampling and analysis procedures, reviewing the previous methodology and detailing the 2007 changes.
- The aim is to describe how estimation procedures were modified to improve consistency and efficiency.

## 2. Overview of Previous CS Methodology
- CS field data come from a stratified sample of 1 km squares over a GB grid; measurements occur at two levels: square-level and within-square plot-level.
- Land Classes (from ITE classification) are used to define strata; over time, classifications were adjusted for country reporting (England, Wales, Scotland).
- Estimation involved computing means and standard errors for each Land Class and combining them (weighted by land area) to produce regional/national estimates.
- Bootstrapping was introduced in CS2000 to estimate significance due to non-normal data distributions.

## 3. Reasons for Modifications to CS Methodology
- Point estimates of stock and change were perceived as inconsistent because stock used all survey data while change used repeated measurements only.
- Missing information (e.g., unrepeated squares) creates discrepancies between stock and change estimates across surveys.
- Several approaches to consistency were considered; modelling was found to be feasible and advantageous, producing consistent and more efficient estimates across square and plot data.

## 4. Modelling Basics
- Consistent estimation uses incomplete data techniques (mixed effects/repeated measures models) with fixed effects (stock/change values) and random effects (sampling variation).
- Models incorporate distributional assumptions; the fixed effects provide robust stock and change estimates, while random effects capture variance/covariance structure.

### 4.1 Possible Approaches
- Approaches include using stock estimates from all measurements with change as the difference between stock estimates, or using only repeated squares for change. These have pros and cons (consistency vs. efficiency, applicability to plot-level data).
- Modelling stock and change together offers consistency and efficiency but requires more assumptions.

### 4.2 Modelling Basics (Square-Level Data)
- Square-level data are treated as a repeated measures problem within Land Classes.
- A two-component model: fixed effects (land-class means over surveys) and random effects (square-level deviations and within-square repeated measures).
- Random components account for square-level variation and correlations of successive surveys.

### 4.3 Plot-Level Data
- Plot-level data within squares require extending the model to include plot-level residuals in addition to square-level random effects.
- Different modelling choices exist (treat plots as independent within squares vs. incorporating hierarchical structure), and both can be embedded in bootstrap procedures.

### 4.4 Model Specification
- General model for square-level data: y_ijk = a_iK + s_ij + e_ijk, with fixed effects a_iK (land-class means per survey), square random effects s_ij, and repeated-measures errors e_ijk.
- Random effects are typically AR1 (first-order autoregressive) with parameters that may vary by land class.
- Reducing the number of random-effect parameters (e.g., common variance across surveys, AR1 covariance) improves model stability and fitting speed.
- Bootstrap remains a robust method for standard errors due to potential mis-specification of variance components.

### 4.5 Model Testing – Broad Habitats
- Historically, Broad Habitats (stock and change) were estimated separately; inconsistencies were evident when using old methods.
- Modelling (AR1) applied to 1984, 1990, and 1998 data showed consistent estimates, with changes derived from differences between stock estimates aligning with sums of inter-survey changes.
- Comparisons between old and new methods generally fell within existing error bounds, supporting adoption of the modelling approach.

## 5. Limitations and Implications
- While bootstrapped estimates with AR1 models are robust, fully parameterised models are slow; AR1 provides a balance of robustness, speed, and a small parameter set.
- Distributional mis-specification can affect variance/covariance estimates; bootstrap mitigates some risk.
- Very non-normal data (e.g., standing water) may cause convergence issues; in such cases, older methods may be preferred for specific variables.
- The modelling approach uses information from all surveys, meaning past survey estimates may be revised as new data are added.
- Overall, the approach should produce more precise estimates and represent the data hierarchy more accurately.

## 6. References
- Includes key CS methodological reports and foundational statistical texts (e.g., Barr et al., 1993; Dempster et al., 1977; Efron & Tibshirani, 1993; Scott, 2002).