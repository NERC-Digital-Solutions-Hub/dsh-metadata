# Statistical methodology for the Countryside Survey data (CS2007)

## Executive summary
- The report describes the statistical methodology for analyzing Countryside Survey (CS) data and outlines changes introduced for CS2007.
- Previous methods used stock estimates from all data within a survey and change estimates from repeated measurements, causing inconsistencies between stock and change.
- Modelling approaches show that consistent estimation via modelling is feasible and robust; such methods yield estimates that differ little from previous methods, but are more precise since they use all available information.
- The new modelling approach is adopted for CS2007, with added assumptions about data distributions that are checked against prior methods to ensure validity, especially for small sub-samples.
- Benefits include improved precision and the ability to propagate information from new surveys to refine past estimates; drawbacks include greater computational effort and sensitivity to distributional assumptions.
- The AR1 mixed-effects modelling with bootstrap standard errors is favoured for square-level data, and extensions to plot-level data are implemented to exploit hierarchical structure.
- Outputs shift from single-survey summaries to longitudinal timelines, with past estimates potentially revised as new data arrive; this is treated as a natural update rather than an inconsistency.

## Introduction
- This technical report outlines sampling and analysis procedures for Countryside Survey data, reviewing the previous methodology and detailing CS2007 changes.
- Full methods of CS sampling and estimation are described in earlier CS reports (Barr et al., 1993).

## 2. Countryside Survey sampling and estimation

### 2.1 Sampling
- CS field data come from a stratified sample of 1 km squares on a 15 km GB grid.
- Each square is mapped and measured at two levels: square-wide measures and within-square plot-level measurements.
- Data types range from binary to continuous; land classification (ITE) strata have expanded over time (GB: 32 → 42 → 45 classes), with separate national classifications for England, Wales, and Scotland.

### 2.2 Estimation
- Regional/national estimates combine Land Class means (with their standard errors) weighted by land area within each class.
- This approach makes minimal distributional assumptions and treats Land Class estimates as independent across classes and from total land.

### 2.3 Bootstrapping
- Because some data are skewed, bootstrapping is used to estimate standard errors and confidence intervals, particularly for square-level data.
- Bootstrapping involves resampling the data to approximate the distribution of stock or change estimates.

## 3. Reasons for modifications to CS methodology
- Past reporting showed inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements.
- Inconsistencies arise when comparing adjacent surveys to longer intervals; some unrepeated squares cause discrepancies.
- A modelling approach capable of delivering consistent stock and change estimates across surveys was explored and found feasible and robust.
- The modelling approach is adopted for CS2007 to provide consistent estimates across timelines.

## 4. Modelling approach and data types

### 4.1 Possible approaches
- Approaches considered include using stock estimates for all data with change as differences between stock estimates, using only repeated squares for change, or adopting a modelling approach for both stock and change.
- Modelling stock and change provides consistency and robustness and can be applied to both square and plot data, though it requires more assumptions and computational effort.

### 4.2 Modelling basics
- Incomplete data techniques (e.g., EM-like methods) allow consistent estimation but require distributional assumptions.
- CS uses mixed effects models to combine fixed effects (stock/change means by land class over surveys) with random effects (squares/plots, survey correlations).
- These models can be complex; simplifications are sought to keep models tractable without greatly compromising fixed-effect estimates.

### 4.3 Square-level data
- For complete 1 km squares, data are treated as repeated measures within land classes.
- A mixed model with fixed effects for land-class means per survey and random effects for squares (within land class) is used.
- Random effects capture square-level deviations; repeated measures correlations across surveys are modeled.

### 4.4 Plot-level data
- Plot data within squares introduce additional hierarchical structure.
- Previous analyses treated plots separately or summarized to the square level; modern approaches embed plot-level residuals within the model to reflect within-square variability.
- Both square- and plot-level models can be embedded in bootstrap procedures for robust standard errors.

### 4.5 Model specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means at survey k)
  - s_ij: square-level random effect for square j in land class i
  - e_ijk: repeated-measures error
- Random effects are typically assumed normal with land-class-specific variances; covariances across surveys may be modeled.
- A full model with many random effects can be unstable; simplifying assumptions are used to reduce parameters (e.g., constant random-effect variance across surveys; AR1 structure for covariances).
- AR1 with bootstrap standard errors is favored for consistent, robust estimation, balancing model flexibility with computational practicality.

### 4.6 Model testing – Broad Habitats
- Broad Habitat data (stock and change) were re-examined across 1984, 1990, and 1998 surveys.
- Earlier methods produced inconsistencies between stock- and repeat-square-based change estimates.
- Modelling with AR1 and bootstrap provided consistent estimates; differences between old and new methods were generally within old method inconsistencies.
- Results demonstrated the feasibility and benefits of consistent estimation for Broad Habitats, soil data (1978–1998), and plot-level data, supporting adoption of the new methodology for CS2007.

## 5. Limitations and implications
- While bootstrapped, square-level estimation with modelling is feasible, it is computationally demanding.
- Fixed-effect estimates (stock/change) are robust to some model variations; variance/covariance parameters are more sensitive to distributional assumptions.
- AR1 with bootstrap offers a practical balance of robustness and computational efficiency for large numbers of analyses.
- Large-scale adoption means past estimates can be updated as new data arrive, reflecting updated information rather than fixed past results.
- Some data (e.g., freshwater standing water) exhibited non-normal distributions causing convergence issues; in such cases, older methods were retained for those variables.
- The modelling approach uses information from all surveys, making past estimates dependent on future data; results are conceptually updates rather than paradoxical inconsistencies.

## 6. References
- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, Laird, Rubin (1977). Maximum likelihood from incomplete data via EM.
- Efron, Tibshirani (1993). An introduction to the bootstrap.
- Haines-Young et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002). Maximum likelihood estimation using the empirical Fisher information matrix.