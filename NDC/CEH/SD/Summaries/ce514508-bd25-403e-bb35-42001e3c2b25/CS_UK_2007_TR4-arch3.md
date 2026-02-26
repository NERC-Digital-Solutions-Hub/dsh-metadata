# Statistical methodology used for the analysis of Countryside Survey data

## Executive summary
- The report describes the statistical methodology for Countryside Survey (CS) data analysis, detailing changes implemented for CS2007.
- Previous methods used minimal assumptions for stock estimation but caused inconsistencies between stock and change estimates due to using different data subsets; the new approach seeks consistency by modelling.
- Modelling demonstrated that consistent estimation is feasible and robust; differences from previous methods were generally within prior inconsistencies.
- A modelling approach was adopted for 2007 data, with advantages including using all available information and producing more precise estimates; however, it introduces additional assumptions about data distributions.
- The new method is computationally more demanding and requires careful validation, especially for small data subsets.
- The AR1 mixed-effects modelling framework, combined with bootstrapping for standard errors, was selected to balance robustness, efficiency, and the ability to handle square and plot level data.
- The shift to modelling enables consistent stock and change estimates across surveys and demonstrates feasibility for broad habitat and plot-level analyses; it also implies that estimates for past surveys may be revised as new data are added.

## 1. Introduction and background
- This technical report outlines CS sampling and analysis procedures, reviews the previous CS methodology, and explains the reasons and details of changes for CS2007.
- It discusses limitations and implications of adopting modelling-based estimation and the emphasis on producing timelines spanning from the first survey to the present.

## 2. Sampling design
- CS uses a stratified sample of 1 km squares at the intersection of a 15 km GB grid; two levels of measurements within each square:
  - Square-level measurements (covering the whole square) and plot-level measurements (within squares).
  - Data types range from binary to continuous variables.
- Land Classification (ITE) defines strata for square selection; classifications have evolved for country-specific reporting (GB → 42 classes for CS2000, then 45 classes for CS2007 with England, Wales, Scotland subsets).
- This hierarchical sampling supports analysis at both square and plot levels, accommodating missing observations.

## 3. Estimation and bootstrapping
- Old method: estimate means and standard errors for each Land Class and combine them to regional estimates, weighting by land area.
- Significance testing: prior normality assumption was replaced with bootstrap (resampling) to accommodate non-normal data distributions.
- Bootstrapping provides robust standard errors and confidence intervals without strict distributional assumptions.

## 4. Reasons for modifications to CS methodology
- Prior point estimates for stock and change were perceived as inconsistent because stock used all survey data while change used only repeated measurements.
- Inconsistencies arise when comparing adjacent and non-adjacent survey changes; different data subsets yield non-identical stock-change differences.
- The modelling approach offers consistent estimation for both stock and change and can be applied to square and plot data; it also better utilizes all available information.
- Several potential approaches were considered; modelling was chosen for its consistency, efficiency, and applicability across data types, despite requiring more assumptions.

## 4.1 Modelling basics
- Incomplete data techniques (e.g., EM-type mixed models) enable consistent estimation but require distributional assumptions; robust fixed-effect estimates can persist under moderate mis-specification of random effects.
- Mixed-effects/repeated-measures models link fixed effects (stock/change) with random effects (e.g., squares, plots) to reflect sampling structure.
- The approach fits models to data from all surveys, and fixed-effect estimates are transformed into stock and change estimates.

## 4.2 Square-level data
- Square-level data are treated as repeated-measures within Land Classes; a mixed-effects model is used.
- Fixed effects: mean values within Land Classes across surveys (treated as categorical year effects).
- Random effects: square-level deviations from Land Class means; within-square repeated measures across surveys are correlated.
- The model provides stock estimates via Land Class means scaled by area; changes are differences of fitted stock estimates.

## 4.3 Plot-level data
- Plot-level data within squares are more complex due to hierarchical structure.
- Previous analyses either summarized to square level (robust but less efficient) or treated plots within squares as independent (potential bias).
- The CS2000 approach used mixed models that included square-level variation but sometimes ignored the full sampling structure; plot-level data can be integrated by extending the model to include plot-level residuals (random effects) with potential correlations across surveys.
- Both square- and plot-level models can be embedded within bootstrapping for robust uncertainty estimates.

## 4.4 Model specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means in survey k)
  - s_ij: square random effect
  - e_ijk: repeated-measures error
- Random effects are assumed normal with land-class-specific variances; repeated errors have land-class and survey-specific variances and covariances.
- The model becomes parameter-heavy as the number of surveys grows; random-effect parameters can become unstable, necessitating reduction strategies.
- Reduction strategies:
  - Assume random effect variances do not vary with land class but may vary across surveys (often not true).
  - Use AR1 assumptions: common within-land-class variance across surveys and first-order autoregressive covariances between adjacent surveys.
  - AR1 reduces random parameters to three per survey, irrespective of survey count.
- Bootstrap estimation is recommended for standard errors due to potential instability in parametric SEs.

## 4.5 Model testing – Broad Habitats
- Examined stock and change for seven Broad Habitats across 1984, 1990, and 1998 to test modelling against previous methods.
- Old method produced inconsistencies between stock- and repeat-square-based change estimates; modelling eliminated these discrepancies.
- Differences between old and new methods generally fell within the old method’s own inconsistencies; modelling provided more coherent, consistent estimates.
- Findings supported adopting consistent modelling for 2007 CS data, including soil data and plot-level data, increasing methodological coherence.

## 4.6 Limitations and implications
- Implementing a bootstrapped model-based analysis for square data was challenging but feasible; fixed-effect estimates (stock/change) were robust to model variation.
- Fully parameterised models were slow; the AR1 model offered a practical balance of stability, speed, and performance for large-scale CS analyses.
- Model estimation of variances/covariances can be sensitive to distributional assumptions; bootstrapping alleviates some concerns.
- Non-normal data (e.g., standing water) can cause convergence issues; in some cases, old methodology results were retained to avoid unreliable estimates.
- Benefits of modelling include more precise estimates by leveraging all information and properly representing data hierarchy; however, estimates for past surveys may be revised as new data are added, since all-survey data inform current estimates.
- The approach is intended to be automated for large-scale analysis, and performance checks compare new and old methods to ensure results remain within expected bounds.

## 5. Implications for monitoring frameworks
- Transition to consistent, model-based estimation aligns with best practices for monitoring frameworks by ensuring stock and change estimates are coherent across time and data levels.
- The approach supports transparent uncertainty quantification (via bootstrap) and explicit modelling of data hierarchy (squares and plots).
- As new survey data arrive, past estimates may be updated, reflecting improved information rather than errors, which is a shift from previous static reporting.
- While more computationally intensive, the AR1 modelling framework offers scalable, robust estimates suitable for routine reporting and decision support in environmental monitoring.