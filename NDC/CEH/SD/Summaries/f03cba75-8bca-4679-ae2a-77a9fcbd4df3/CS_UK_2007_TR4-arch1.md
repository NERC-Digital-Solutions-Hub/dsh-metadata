# Countryside Survey 2007: Statistical Methodology

- This report describes the statistical methodology used to analyse Countryside Survey (CS) data, summarises previous methods, and details the changes implemented for CS in 2007.
- It evaluates the shift from non-model-based estimation to consistent estimation via modelling, and assesses the impact on stock and change estimates.

## Executive summary

- Previous CS estimation used minimal assumptions and was robust, but stock was estimated from all data in a survey while change used only repeated measurements, causing inconsistencies between stock and change estimates.
- Modelling methods for consistent estimation were found feasible and robust when tested with Broad Habitat data from prior surveys.
- The 2007 CS adopts a modelling approach to achieve consistency and improve precision by using all available information.
- The modelling approach requires additional distributional assumptions; results for small subsets are checked against the old method to ensure validity.
- Unlike previous methods, the new approach often yields more precise estimates, though new survey data can slightly revise past estimates.
- Implementation is computationally intensive, involving iterative model fitting and complex CS sampling, but results in a significantly improved, more coherent product.
- For Broad Habitats and plot-level data, modelling demonstrated feasibility and consistency, supporting adoption of the new methodology for 2007 CS.
- A key trade-off is that estimates are not strictly consistent across reporting occasions once new data are added; updates to past surveys are expected as information accumulates.

## 1. Introduction

- The report provides an overview of CS sampling and analysis procedures, reviews the previous methodology, and explains the rationale and details of changes for CS2007.
- Full methodological detail of CS sampling and estimation is documented in earlier work (Barr et al., 1993).

## 2. Overview of previous CS methodology

- CS field data come from a stratified sample of 1 km squares on a 15 km GB grid; two sampling levels provide square-wide and within-square (plot) measurements.
- Land Classification (ITE) stratifies squares; classifications expanded over time (GB: 32 → 42 → 45 classes; separate national classifications for England, Wales, Scotland).
- Estimation combined land-class means/standard errors to produce regional/national estimates, weighting by land-class area.
- Significance testing used normality assumptions prior to CS2000; CS2000 introduced bootstrap to handle non-normality for square-level data.

## 3. Reasons for modifications to CS methodology

- Point estimates of stock and change were considered inconsistent because stock used all data from a survey while change used repeated measurements only.
- Inconsistencies arise because some squares are not recorded in both surveys (e.g., new squares added; some squares lost due to landowner refusals).
- Three potential approaches to achieve consistency were considered; modelling provided consistent and more efficient estimates across square and plot data.
- The shift aims to report estimates that are coherent across time and use all available information.

## 4. Consistent estimation

- Models require more assumptions about data distributions; however, they enable consistent stock and change estimates by using data from all surveys.
- Mixed-effects/repeated-measures models are used to reflect the hierarchical CS sampling structure (square- and plot-level data).

### 4.1 Square level data

- Square-level data are modeled with repeated-measures/mixed-effects structures.
- Fixed effects model mean values by land class across surveys; stock is derived by scaling by land-class area.
- Random effects account for square-level deviations and correlation of survey deviations over time.

### 4.2 Plot level data

- Plot data within squares can be modeled with square-level variation plus a plot-level residual.
- Models can be embedded within bootstrapping to obtain robust standard errors.

### 4.3 Model specification (square level)

- General form: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means across surveys)
  - s_ij: square random effect
  - e_ijk: repeated-measures residual
- Random effects are normally distributed with land-class-specific variances; repeated-measures covariances vary by land class and survey.
- A large number of random-effect parameters can be unstable; simplifications are used to keep the model tractable.

### 4.4 Model specification (plot level)

- Extends the square-level model to include a plot-level random effect, capturing variation among plots within squares.
- Both square- and plot-level forms can be bootstrapped for standard errors.

### 4.5 Model specification (practical considerations)

- To keep the model tractable, a reduced-parameter approach is used (e.g., AR1: autoregressive structure with a common variance across surveys).
- Fixed effects estimation is relatively robust to distributional mis-specification; variance/covariance parameters are more sensitive.
- The AR1 model with bootstrap estimation of standard errors is investigated as a balance between robustness and computational efficiency.

### 4.6 Model testing – Broad Habitats

- Historical Broad Habitat analyses showed inconsistencies between stock- and change-based estimates under old methods.
- Modelling (AR1) produced consistent stock and change estimates and eliminated major discrepancies.
- When comparing old vs new methods, differences were generally within the prior method’s error bounds; some estimates changed by minor margins.
- The modeling approach was also validated for soil data (1978/1998) and plot-level data, confirming feasibility and consistency.

## 5. Limitations and implications

- Bootstrapped square-level analysis is computationally demanding; larger variable sets increase run time.
- The AR1 model provides a stable, efficient, and robust framework, but variance/covariance estimates may still be sensitive to distributional assumptions.
- In highly non-normal data, results on the original measurement scale may be undermined if transformations are used; bootstrap-based standard errors help preserve robustness.
- Some variables (e.g., standing water) exhibited non-normality that caused convergence to local maxima with the new method; old methodology was retained for these cases.
- Using all-survey data improves estimates but means past survey estimates can be revised as new information accumulates; future reporting may differ from earlier versions due to updated data.
- Overall, the modeling approach uses more information and better represents data hierarchy, yielding potentially more precise estimates, with reasonable checks against old methodology.

## 6. References

- Barr et al. (1993); CS1990 main report
- Dempster, Laird, and Rubin (1977); EM algorithm
- Efron and Tibshirani (1993); Bootstrap
- Haines-Young et al. (2000); Accounting for nature: UK habitats
- Scott (2002); ML estimation using empirical Fisher information