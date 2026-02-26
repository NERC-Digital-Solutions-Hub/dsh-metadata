# Countryside Survey 2007: Methodology

- This technical report describes the statistical methodology used to analyse Countryside Survey (CS) data and outlines the changes implemented for CS in 2007 to produce consistent and efficient estimates of stock and change.
- It compares the old approach (which used all data for stock and repeat data for change, causing potential inconsistencies) with a modelling approach that provides consistent estimates for stock and change across surveys.
- The modelling approach uses data from all surveys and employs mixed effects/repeated measures models, enabling more precise estimates at both square and plot levels, with results that can be updated as new surveys are added.

## Introduction (scope and aims)

- Provides an overview of CS sampling and analysis procedures, including reasons for the methodology changes in 2007.
- Builds on earlier CS methodology (referencing Barr et al., 1993) and introduces a modelling framework to achieve consistency between stock and change estimates over time.

## Overview of previous CS methodology

- Stock estimates used all data from a survey; change estimates used only repeated measurements, causing potential mismatches between stock and change.
- This led to inconsistencies when reporting changes across surveying timelines.

## Reasons for modifications to CS methodology

- Need to resolve inconsistencies between stock and change estimates across surveys.
- Explore whether modelling can provide consistent, robust, and more efficient estimates by using information from all surveys.
- Ensure methods can be applied to both square-level and plot-level data and are implementable within the CS workflow.

## Modelling basics and approach

- Consistent estimation is achieved by fitting mixed effects and/or repeated measures models to data from all surveys.
- Fixed effects represent stock/change values; random effects capture sampling variability (squares, plots, and survey-to-survey correlations).
- The approach requires distributional assumptions about random effects; bootstrap is used to obtain robust standard errors and confidence intervals.

## Square-level data

- Data are treated as a random sample of squares within each Land Class, with measurements across surveys (some missing).
- A repeated measures mixed model is used:
  - Fixed effects: land-class means across surveys (stock estimates when scaled by land-class area).
  - Random effects: square-level deviations from land-class means; survey-to-survey deviations allowed to be correlated.
- This yields consistent stock and change estimates and enables robust standard errors via bootstrap.

## Plot-level data

- Plot-level measurements within squares (e.g., vegetation, soils) can be incorporated.
- Earlier analyses either aggregated plots to the square level or treated plots as independent, which could misstate variability.
- The modern approach extends the square-level model to include a plot-level residual (random effect), with bootstrapping for standard errors to reflect the data hierarchy and correlations.

## Model specification

- General form for square-level data:
  y_ijk = a_iK + s_ij + e_ijk
  - a_ik: fixed effects (land-class means across surveys)
  - s_ij: square random effect
  - e_ijk: repeated-measures error
- Random effects (s_ij, e_ijk) are assumed normally distributed with land-class-specific variances; covariances across surveys are modelled (often via AR(1) structure to reduce parameters).
- To keep models tractable with many surveys and land classes, simplifications are used (e.g., common variance across surveys, AR1 covariance for repeated measures) while maintaining robust fixed-effect estimates.

## Model testing – Broad Habitats

- Used data from 1984, 1990, and 1998 to compare old methods with modelling approaches.
- Consistent estimates obtained with the AR1 modelling approach eliminated the discrepancies seen with stock/change from the old method.
- Differences between old and new methods were generally small relative to existing inconsistencies and within bootstrap-derived uncertainty.
- Extended modelling approach to soil data and plot-level data, confirming feasibility of consistent estimates beyond square-level data; led to adopting the new methodology for 2007 data.

## Limitations and implications

- AR1 modelling with bootstrap is robust for fixed effects but requires more computation than the old method.
- Fully parameterised models are slow; AR1 provides a practical balance between accuracy and computational demand.
- Model selection is important; in large-scale applications, a standard, automated model (AR1 with bootstrap) is preferred for consistency and efficiency.
- Distributional assumptions influence variance/covariance estimates; bootstrap helps mitigate potential mis-specification.
- Some variables with highly non-normal distributions (e.g., standing water) can cause convergence issues; in such cases, the previous method may be reported if necessary.
- Results are inherently updated as new surveys are added, meaning estimates for earlier surveys may be revised. This reflects the integrated use of all available data rather than static, independently reported years.

## Practical implications for GIS data products

- Produces consistent, time-spanning stock and change estimates suitable for map-based visualizations across multiple survey years.
- Improves precision of spatial estimates by leveraging hierarchical structure (square and plot levels) and all available data.
- Facilitates updating historical maps and trends as new CS data are collected, with small revisions to earlier results expected.
- Requires awareness of the modelling framework when interpreting map-derived change across years, especially with new data influencing past estimates.

## References and validation

- Validates modelling approach against previous CS results and Broad Habitat analyses; supports adoption of a consistent estimation framework for 2007 CS data.
- Cites foundational statistical methods (e.g., mixed-effects models, bootstrap, EM-type handling of missing data) and prior CS reports.