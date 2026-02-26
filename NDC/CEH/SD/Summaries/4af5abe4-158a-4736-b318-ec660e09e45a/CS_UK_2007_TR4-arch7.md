# Countryside Survey 2007 Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and explains changes introduced for CS 2007 to achieve consistent estimation.
- Old CS methods used stock estimates from all data in a survey and change estimates from repeated measurements only, leading to inconsistencies between stock and change.
- Modelling-based consistent estimation is feasible and robust, using all available data to produce more precise estimates; differences from old methods are generally small.
- New approach employs data from all surveys via mixed effects/repeated measures models, requiring additional distributional assumptions but validated by comparisons with previous methods.
- The AR1 modelling framework with bootstrap for standard errors is adopted to manage complexity, ensure robustness, and provide reliable uncertainty quantification.
- The methodology is tested on Broad Habitats and soil/plot-level data, showing feasibility and improved consistency across survey periods.
- Implementation is computationally intensive but ultimately yields a more coherent, network-wide data product suitable for map-based GIS outputs.

## Why changes were needed
- Prior point estimates (stock vs. change) could appear inconsistent because different data sources were used for stock and change due to missing information across survey years.
- With CS 2007, there was a shift to reporting timelines spanning multiple surveys, making consistency across non-adjacent periods important.
- Modelling approaches using all available data can provide consistent, efficient estimates, though they rely on stronger distributional assumptions.

## Modelling approach and key concepts
- Use of mixed effects and/or repeated measures models to handle incomplete data and the hierarchical sampling design (squares and plots within squares).
- Fixed effects correspond to land-class means across surveys; random effects capture square-level and plot-level variation and their correlations across surveys.
- To keep the model tractable, random-parameter reduction is applied, notably the AR1 (autoregressive of order one) structure, which reduces the number of random parameters per land class to a manageable amount.
- Bootstrapping is used to obtain standard errors and confidence intervals, accommodating non-normal data and providing robust significance testing.

## Data structure and levels
- Square-level data: complete 1 km squares within Land Classes; multiple surveys provide repeated measurements with potential missing observations.
- Plot-level data: within-square plots (e.g., vegetation and soils) add detail but require careful handling to reflect hierarchical sampling.
- Land Classification: GB Land Classes, with country-specific adaptations (England, Wales, Scotland) resulting in 45 classes in CS2007 (21 England, 8 Wales, 16 Scotland).

## Model specification (high level)
- Square-level model: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik are fixed effects (land-class means per survey),
  - s_ij are square-level random effects,
  - e_ijk are within-square repeated-measure residuals.
- Random effects are assumed to follow normal distributions with land-class-specific variances; correlations across surveys are modelled (AR1 structure reduces parameters).
- Plot-level models extend the square-level framework by adding plot-level residuals, allowing for correlation of plots within squares and across surveys.

## Practical implications for outputs and GIS
- Stock and change estimates are now produced in a consistent, integrated framework, enabling reliable map-based visualisations of habitat extent and change over time.
- Results for any given survey may be updated as new surveys are added, since information from all surveys informs fixed and random effects.
- Results are presented on the original measurement scale (avoiding transformations), which is important for clear GIS mapping and stakeholder interpretation.
- The approach is computationally intensive; AR1 with bootstrap was chosen as a practical balance between accuracy, robustness, and run-time for large numbers of analyses.

## Validation and limitations
- The AR1 model with bootstrap was tested against older methods; the fixed-effect estimates (stock/change) were robust to model variation, while variance-covariance estimates are more sensitive.
- For very non-normal data, model-based standard errors may be unreliable; bootstrap provides a robust alternative.
- In some non-standard data (e.g., very skewed freshwater standing water), the old method may be preferred due to convergence issues with the new modelling approach.
- Automated, consistent modelling is favored for large-scale application, though model checking remains important to ensure reliability.

## Limitations and implications for reporting
- Consistent estimation implies that estimates for a given survey can shift as new data arrive; previous results may be revised slightly in light of new information.
- Adoption of a modelling approach enhances precision and data utilisation but requires careful interpretation of updates across time series.

## References (indicative)
- Barr et al. (1993) Countryside Survey 1990 Main Report
- Dempster, Laird, Rubin (1997) EM algorithm
- Efron, Tibshirani (1993) Bootstrap
- Haines-Young et al. (2000) Accounting for nature: UK habitats
- Scott (2002) ML with empirical Fisher information

## Implementation notes for GIS professionals
- Map-ready outputs benefit from the integrated stock/change estimates across time, with uncertainties quantified via bootstrap.
- Data preparation should account for the hierarchical structure (land class, square, plot) and potential missing data across survey years.
- Regular updates after new CS waves should be anticipated, with revisited previous-survey estimates feeding into existing map layers.