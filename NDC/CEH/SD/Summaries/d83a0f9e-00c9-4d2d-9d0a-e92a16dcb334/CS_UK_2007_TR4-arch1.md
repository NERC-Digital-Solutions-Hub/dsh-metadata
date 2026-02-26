# Statistical Methodology for Countryside Survey Data

## Executive Summary
- The report describes the statistical methodology used to analyse Countryside Survey (CS) data, summarising previous methods and detailing changes implemented for CS in 2007.
- Prior methods used minimal assumptions and were robust for stock estimates but led to inconsistencies between stock and change estimates due to using different data subsets.
- Modelling-based, consistent estimation was found feasible and robust for CS Broad Habitat data, generally aligning with previous estimates but with improved coherence.
- The new modelling approach uses all available information, yielding more precise estimates; updates to one survey can subtly revise past survey estimates.
- Implementing modelling is computationally intensive, requiring iterative model fitting and addressing CS’s complex sampling; this led to practical challenges and the need for automation.
- The 2007 CS adopted the consistent, modelling-based methodology, with validation against the old method to ensure results remained within prior uncertainty bounds.
- The AR1 mixed-effects model with bootstrapped standard errors was selected for square-level data due to its balance of robustness, precision, and computational feasibility; extensions to plot-level data were developed.
- For Broad Habitats, modelling confirmed consistency between stock and change estimates and reduced discrepancies evident in previous methods.
- Limitations include dependence on distributional assumptions for variance/covariance parameters and substantial computational demands; however, bootstrapping mitigates distributional concerns.
- Overall, the modelling approach provides more precise, internally consistent estimates and is recommended for CS analyses, including future surveys.

## 1. Introduction
- The report gives an overview of sampling and analysis procedures for Countryside Survey data.
- It reviews the previous CS methodology and explains the reasons and details for changes implemented for CS in 2007.
- It discusses limitations and implications of adopting the new modelling approach.

## 2. Overview of Previous CS Methodology
- CS Field Survey data come from a stratified sample of 1 km squares within a 15 km GB grid; data are collected at two levels: square-level and within-square plot-level measurements.
- Estimation traditionally computed means and standard errors for land classes and combined them to regional/national estimates, weighting by land area.
- Significance testing relied on bootstrap only for square-level data; prior methods assumed normality for many estimates.
- A key issue was inconsistency: stock was estimated using all data from a survey, while change used only repeated measurements, causing discrepancies between stock and change estimates.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock and change used different data subsets; the newer reporting scope emphasized timelines spanning from the first survey to the present, heightening concerns about apparent inconsistencies.
- Several approaches to achieve consistency were considered; modelling offered the best path to simultaneous, robust estimation of both stock and change across surveys and data levels (square and plot).
- The modelling approach uses incomplete-data techniques (mixed/repeated-measures models) to leverage information across all surveys and data hierarchies.

## 4. Methodology Details

### 4.2 Modelling Basics
- Incomplete data techniques (e.g., mixed-effect models) are used to handle missing information across surveys.
- Models include fixed effects (stock/change components) and random effects (to reflect sampling structure and repeated measures).
- The approach requires more distributional assumptions than previous methods; bootstrap is used to obtain robust standard errors.

### 4.3 Square Level Data
- Data are treated as a random sample of squares within each land class, with potential missing observations.
- A repeated-measures mixed-effects model is used: fixed effects capture land-class means across surveys; random effects capture square-level variation and within-square repeated-measure variation and correlations.
- The model acknowledges correlations of repeated measurements within the same square across surveys.

### 4.4 Plot Level Data
- Plot-level data within squares can be analyzed by extending the square-level model to include an additional plot-level residual (random effect).
- This extension allows plotting data to be analyzed with proper accounting for hierarchical structure and within-square variation.
- Both square and plot-level models can be embedded within bootstrap procedures.

### 4.5 Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik are fixed effects (land-class means in survey k),
  - s_ij are square-level random effects,
  - e_ijk are repeated-measures random effects.
- Random effects are assumed normally distributed with land-class-specific variances; repeated-measures covariances (within land class and across surveys) are modelled, typically with a manageable number of parameters.
- To keep the model parsimonious and computationally feasible, reduction strategies are used (e.g., assuming common variance components across surveys or land classes, or using an AR1 structure for covariances).
- The AR1 (autoregressive) approach reduces the number of random parameters, maintaining robust fixed-effect estimates while simplifying estimation.

### 4.6 Model Testing – Broad Habitats
- Broad Habitat stock and change have been analyzed using both the old method (prior) and the new modelling approach.
- Modelling showed that differences between old and new estimates were generally small and often within the existing uncertainty ranges.
- The new approach resolved discrepancies between stock and change observed with the old methods and provided consistent estimates across adjacent survey periods.
- The Broad Habitats results, and broader soil/plot data analyses, supported adopting the modelling approach for the 2007 CS.

## 5. Limitations and Implications
- While AR1-based modelling with bootstrap provides robust fixed-effect estimates, variance and covariance parameters are more sensitive to mis-specification; bootstrapping helps mitigate this.
- Very non-normal data or highly skewed distributions can cause convergence issues or convergence to local maxima; some variables (e.g., freshwater standing water) may require old methods or alternative handling.
- Fully parameterised models are computationally intensive; for large numbers of variables, a standard, automated AR1-based model is preferred for practicality and consistency.
- Analyses influence past estimates as new surveys provide information that updates previous results; thus estimates are not fixed across reporting occasions, though updates are generally small.
- The approach emphasizes using all available information and correctly modeling data hierarchy, improving precision when distributional assumptions are reasonable.

## 6. References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron, Tibshirani (Bootstrap); Scott (2002) on empirical Fisher information.
- The CS2007 methodology builds on these foundations and includes AR1 mixed-effects modelling and bootstrap-based standard error estimation.