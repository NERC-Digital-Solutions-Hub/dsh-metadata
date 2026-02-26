# Statistical Methodology for Countryside Survey Data

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for CS in 2007.
- Previous methods used stock estimates from an entire survey and change estimates from repeated measurements, leading to inconsistencies between stock and change.
- Modelling and consistent estimation, demonstrated with CS Broad Habitat data, provided robust and more precise estimates, with differences from old methods generally small.
- A modelling approach that uses all available data and accounts for data hierarchy was adopted for 2007 CS data; it requires additional assumptions about data distributions.
- The new method increases precision and allows improved estimates for past surveys as new data become available, but it is more computationally intensive.
- AR1-based mixed models, with bootstrapped standard errors, were chosen to balance robustness, speed, and scalability for large numbers of analyses.
- Validation included comparisons with old methods to ensure results remained within previous uncertainty ranges; improvements were particularly noted for improved data utilization and consistency across survey periods.

## 1. Introduction
- The CS dataset comprises measurements from a stratified sample of 1 km squares within a 15 km GB grid, with two sampling levels: square-wide and within-square plots.
- Land Classification stratifies squares; classifications vary by country (England, Wales, Scotland).
- Estimation traditionally involved combining land-class means weighted by land area; minimal distributional assumptions.
- Bootstrapping was introduced in CS2000 to better assess significance due to potential non-normality in some features.

## 2. Overview of Previous CS Methodology
- Stock estimates used all data from a survey; change estimates relied on repeated measurements, causing inconsistencies when comparing stock and change across surveys.
- Differences between adjacent surveys could not always be reconciled with non-adjacent survey changes.
- The old approach maximized information use for stock but limited change estimation to repeated plots, leading to mismatches.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies between stock and change estimates prompted exploration of consistent estimation methods.
- Missing data across survey pairs (due to new squares, landowner refusals, etc.) biased earlier comparisons.
- Modelling approaches offer consistency and efficiency, applicable to both square and plot level data, at the cost of added assumptions.

## 4. Consistent Estimation

### 4.1 Possible Approaches
- Stock from all measurements with change as the difference between stock estimates (consistent and robust under certain covariance conditions) but less efficient when survey correlations are high.
- Change estimated from repeat squares only (robust but potentially inefficient and not directly applicable to plot-level data).
- Modelling approaches offer consistency and efficiency for both square and plot data; explored in detail.

### 4.2 Modelling Basics
- Incomplete data techniques (e.g., mixed effects/repeated measures models) used to obtain consistent stock and change estimates across surveys.
- Models require assumptions about data distributions; fixed effects estimate stock/change, random effects capture sampling structure.
- Emphasis on using all surveys’ data, with complex models potentially involving many random parameters.

### 4.3 Square Level Data
- Data treated as repeated measures within Land Classes; a mixed model with fixed effects for land-class means across surveys and random effects for squares.
- Square-level residuals are allowed to be correlated across surveys.

### 4.4 Plot Level Data
- Plot-level data within squares can be summarized or modeled directly; full hierarchical treatment improves efficiency but is more complex.
- Models can include a plot-level random effect in addition to the square-level random effect; bootstrapping can be applied to either approach.

### 4.5 Model Specification
- General form: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects (land-class means by survey), s_ij are square random effects, and e_ijk are repeated-measures residuals.
- Variance components (τ_i for squares, σ_ik for residuals) vary by land class and survey; correlations across surveys modeled (often AR1).
- Full model can become unwieldy with many random parameters; practical reductions implemented (e.g., common σ_i across surveys, AR1 covariances).
- Bootstrap estimation of standard errors is used to maintain robustness given potential mis-specification.

### 4.6 Model Testing – Broad Habitats
- Analyses of seven Broad Habitats using 1984, 1990, and 1998 data showed modelling eliminated the stock/change discrepancies seen with old methods.
- Changes inferred from stock differences and those from consecutive inter-survey periods matched within expected inconsistency ranges.
- Comparing old and new methods showed most differences were within old method discrepancies; modelling supported consistency across time.
- Beyond Broad Habitats, findings for soil and plot-level data supported the feasibility of a consistent modelling approach.

## 5. Limitations and Implications
- While AR1 modelling with bootstrapped standard errors is robust, fully parameterised models are slow; AR1 provides a practical balance.
- Model selection requires automation for large numbers of analyses; fixed effects are robust to some distributional mis-specifications.
- Very non-normal data (e.g., standing water) may lead to convergence or estimation issues; in such cases, older methods may be reported for those variables.
- Adopting a model-based, data-inclusive approach means past survey estimates can be updated with new data, which may slightly revise earlier findings.
- Results are on the original measurement scale; transformations would complicate back-conversion due to dependence on both fixed and random effects.

## 6. References
- Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron and Tibshirani (1993), Scott (2002).