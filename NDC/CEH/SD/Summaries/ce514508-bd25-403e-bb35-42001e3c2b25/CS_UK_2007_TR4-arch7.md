# Statistical methodology for Countryside Survey data

- This report describes the statistical methodology used to analyze Countryside Survey (CS) data, compares previous methods, and details the modelling changes implemented for CS in 2007.
- It emphasizes moving from separate stock and change estimates (constructed from different data sets) to a consistent, model-based approach that uses all available information.

## Key aims and rationale

- Prior methods produced inconsistencies: stock was estimated from all survey data, while change used only repeated measurements.
- Modelling approaches were investigated for consistency and efficiency, showing that model-based consistent estimation is feasible and robust for Broad Habitat data.
- The 2007 CS adopts modelling for consistent estimation, improving precision but requiring additional modelling assumptions and computational effort.
- Results are validated by comparing new model-based estimates with old methods, especially for small subsets of data.

## Data, sampling, and structure

- CS data come from a stratified sample of 1 km squares on a 15 km GB grid; measurements occur at two levels within each square (square-wide and within-square plots).
- Land Classification (LC) strata: GB classification evolved from 32 to 42 (CS2000) to 45 (CS2007) classes, with country-specific classifications (England, Wales, Scotland).
- Measurements include binary and continuous variables; estimation weights LC estimates by land area.

## Estimation and inference methods

- Old method: means and standard errors for each LC, then area-weighted combination to regional/national estimates; assumes independence across LC estimates.
- Bootstrapping: used since normality assumptions for all estimates were questionable, enabling robust SEs and significance testing for square-level data.

## Reasons for methodological modifications

- Inconsistencies arose because stock estimates used all data while change estimates used repeated data only.
- Three conceptual approaches to achieve consistency were considered; modelling (consistency and efficiency) was chosen for applicability to both square and plot data.
- The shift aims to provide estimates of stock and change that are coherent across time intervals and reporting levels.

## Modelling basics and structure

- Incomplete data techniques (e.g., mixed effects, repeated measures) are employed to utilize data from all surveys while accounting for missingness.
- Models include fixed effects (stock/change parameters) and random effects (capturing survey-specific, square-specific, and plot-level variation).
- Distributional assumptions are necessary for some parameters; bootstrap can provide robust SEs where parametric SEs may be unreliable.

## Square level data modelling

- Model for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: LC-specific fixed effects across surveys (stock estimates).
  - s_ij: square-level random effect within LC.
  - e_ijk: within-square, repeated measures residuals.
- Random effects assumed normal with LC-specific variance; covariances of repeated measures modeled across surveys.
- A balanced approach reduces the parameter load: fixed effects grow with the number of LCs, while random effects are constrained.

## Plot level data modelling

- Plot-level data introduces additional complexity due to hierarchical structure (plots within squares).
- Extended models include a plot-level residual (random effect) in addition to the square-level random effect.
- Both square- and plot-level models can be embedded within bootstrap procedures to obtain SEs.

## Model specification and practical considerations

- General square-level model: y_ijk = a_ik + s_ij + e_ijk with distributions:
  - s_ij ~ N(0, τ_i^2)
  - e_ijk ~ N(0, σ_ik^2) with covariances across surveys
- To keep the model tractable with many surveys and LC classes, a simplified AR1 (autoregressive) structure is used:
  - Assume common within-survey variances across surveys for each LC, and AR(1) correlation for repeated measures.
  - This reduces random parameters to a small, fixed set that does not grow with the number of surveys.
- AR1 plus bootstrap is recommended for robust SEs, balancing model stability and computational feasibility.

## Model testing: Broad Habitats

- Analyses of Broad Habitats across 1984, 1990, and 1998 show that modelling methods remove the inconsistencies observed with old methods.
- Stock estimates and cumulative changes align under the consistent modelling framework.
- Comparisons between old and new methods show differences typically within the existing uncertainty; most changes are small or negligible relative to the standard errors.

## Limitations and implications

- Computational intensity: full parameterised models are slow; AR1 with bootstrap offers a practical compromise for large numbers of analyses.
- Automated modelling: a standard AR1-based approach is favored to enable automated processing across many variables.
- Data distribution sensitivity: fixed-effects estimates are robust, but variance/covariance estimates depend on distributional assumptions; bootstrap mitigates some risks.
- Some variables with highly non-normal distributions (e.g., standing water) may converge to local maxima or require older methods for reliable estimates; noted as exceptions.
- Updating past results: because data from all surveys inform current estimates, past survey estimates may be revised as new data are added (i.e., results get updated with new information).

## Implications for GIS data products

- More precise, consistent stock and change estimates enable coherent map-based representations across time and across land classifications.
- The modelling framework supports integrating multiple surveys, improving the reliability of spatial visualizations and trend maps.
- Users should be aware that past estimates may be revised slightly as new survey data are incorporated.

## References

- Barr et al. (1993); CS1990 main report
- Dempster, Laird, Rubin (1977); EM algorithm
- Efron & Tibshirani (1993); Bootstrap
- Haines-Young et al. (2000); Accounting for nature
- Scott (2002); Maximum likelihood with empirical Fisher information