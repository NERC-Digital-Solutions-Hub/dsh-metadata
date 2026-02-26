# Countryside Survey 2007 Statistical Methodology

## Executive Summary
- Describes the statistical methodology used for Countryside Survey (CS) data analysis, summarising previous methods and detailing changes introduced for CS in 2007.
- Highlights problems with earlier approaches: stock and change were estimated from different data subsets, causing apparent but not fundamental inconsistencies.
- Presents a modelling-based approach that provides consistent and typically more precise estimates by using all available data and modelling data hierarchies across surveys.
- Finds that modelling yields estimates that are broadly in line with previous results but with improved precision; discrepancies with earlier methods are generally within existing uncertainty.
- Notes that implementing the modelling approach is technically demanding and slower, but the AR1 mixed-effects framework with bootstrap provides robust standard errors.
- Demonstrates feasibility of consistent estimation using Broad Habitat data and extends validation to plot and soil data, leading to adoption of the new methodology for CS 2007.
- Implications for data leaders: greater data efficiency, improved cross-survey comparability, and a need for automated, scalable modelling pipelines; estimates for older surveys may update as new data are incorporated.

## 1. Introduction
- This technical report outlines the sampling and analysis procedures for CS data, reviewing the old methodology and detailing changes for 2007, including limitations and implications.
- Restates that fuller methodological expositions exist in earlier CS reports.

## 2. Overview of Previous CS Methodology
### 2.1 Sampling
- Information collected from a stratified sample of 1 km squares at the intersection of a 15 km GB grid.
- Two levels of sampling: whole squares and features within squares; measurements span binary to continuous variables.
- Stratification is based on the ITE Land Classification; country-specific adaptations have produced 21 England, 8 Wales, and 16 Scotland classes (with related derivations from a GB classification).

### 2.2 Estimation
- Regional/national estimates computed by combining land-class means (weighted by land area) to produce regional means or totals.
- Means and standard errors are calculated per land class with minimal distributional assumptions; independence is assumed between land classes and total land.

### 2.3 Bootstrapping
- Prior to CS2000, significance was assessed assuming normality. With skewed features, bootstrap methods (thousands of resamples) estimate standard errors and confidence intervals without relying on normality.

## 3. Reasons for Modifications to CS Methodology
- Past results showed inconsistencies: stock estimates used all data from a survey, while change used only repeated measurements, causing mismatches.
- Missing information (e.g., unrepeated squares, landowner refusals) led to discrepancies when comparing adjacent survey results.
- Three potential consistency approaches exist; using stock from all measurements and change from differences between stock estimates was simple and robust but inefficient for some data and not suitable for plot-level data.
- Modelling (consistent estimation) was identified as feasible and robust, applicable to both square and plot data, and able to provide consistent and efficient estimates. It requires additional distributional assumptions, which must be validated.

## 4. Consistent Estimation
### 4.1 Possible Approaches
- Three sets of consistent estimates can be derived from a pair of surveys; each estimates the same stock and change values.
- Using all square measurements for stock and changes derived as differences between stock estimates offers robustness and ease of implementation, but estimates may be inefficient if inter-survey covariance is large and is not easily extended to plot data.

### 4.2 Modelling Basics
- Incomplete data techniques (e.g., EM, mixed models) enable consistent estimation by using data from all surveys and their correlation structure.
- Mixed-effects models combine fixed effects (stock/change means per land class per survey) with random effects (squares, plots, and survey-related correlations). Distributional assumptions are necessary for random effects, so robust SEs via bootstrap are emphasized.
- Full models can become unwieldy with many random parameters; thus simplifications are used to maintain computational practicality while preserving robustness of fixed effects.

### 4.3 Square Level Data
- For complete 1 km squares, data are treated as a random sample within each land class; a repeated-measures (mixed) model is used.
- Fixed effects: land-class means per survey.
- Random effects: square-level deviations and within-square, across-survey residual correlations.
- Correlations across surveys are modeled to reflect the hierarchical sampling structure.

### 4.4 Plot Level Data
- Within-square plots add another hierarchical layer; earlier analyses either aggregated to square level or treated plots as independent within land classes, risking bias or inefficiency.
- Modern modelling can include plot-level residuals in addition to square-level effects; both square- and plot-level models can be embedded in bootstrapping to obtain SEs.

### 4.5 Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Distributions: s_ij ~ N(0, τ_i^2) (land-class-specific), e_ijk ~ N(0, σ_ik^2) with covariances across surveys; complexity grows with the number of surveys.
- To keep models tractable, random-effect parameters are constrained (e.g., common variance across surveys, AR1 structure for covariances). AR1 reduces random parameters to three per land class, regardless of survey count.
- Bootstrap-based standard errors are recommended since parametric SEs may be unreliable when distributional assumptions are imperfect.

### 4.6 Model Testing – Broad Habitats
- Existing Broad Habitat data (stock and change across 1984, 1990, 1998) were re-evaluated with modelling to assess consistency.
- Previous methods produced inconsistencies between stock-derived and repeat-squares-derived changes; modelling produced consistent estimates, with differences generally within prior error bounds.
- Results supported adopting the modelling approach for CS 2007; similar analyses for soil and plot data confirmed feasibility and improved consistency across data types.

## 5. Limitations and Implications
- Computational intensity: model fitting (especially with many variables) is time-consuming; AR1 offers a balance between performance and speed.
- Robustness of fixed effects is generally good, but variance/covariance parameters are more sensitive to distributional assumptions; bootstrap helps mitigate this.
- Some variables with highly non-normal distributions (e.g., standing freshwater areas) may converge to local maxima or yield unreliable estimates with the new method; in such cases, the prior method may be preferred.
- Moving to a full modelling framework means that estimates for older surveys can be revised as new data are incorporated; reporting across surveys becomes more dynamically updated rather than fixed between reporting occasions.
- Overall, the modelling approach makes better use of all information, respects data hierarchy, and yields more precise estimates, at the cost of requiring automated, scalable analytical pipelines and careful validation.

## 6. References
- Barr et al. (1993); CS1990 Main Report
- Dempster, Laird, and Rubin (1977); EM algorithm
- Efron and Tibshirani (1993); Bootstrap
- Haines-Young et al. (2000); Accounting for Nature
- Scott (2002); Maximum likelihood estimation with empirical Fisher information
- CS2007 methodological reports and related CS publications

- Funding and contact: Countryside Survey 2007 funded by NERC/Defra partnership; project office contacts provided.