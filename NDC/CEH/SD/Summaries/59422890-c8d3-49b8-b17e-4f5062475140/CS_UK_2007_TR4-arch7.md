# Countryside Survey 2007: Consistent Estimation

## Executive Summary
- Describes the statistical methodology for Countryside Survey (CS) data analysis and changes implemented for CS 2007.
- Old methods used all data for stock estimates but only repeated measurements for change, causing inconsistencies between stock and change estimates.
- Modelling (consistent estimation) using CS Broad Habitat data proved feasible and robust; differences from old methods were generally within existing inconsistencies.
- The 2007 approach adopts modelling for both stock and change, utilizing all available information to yield more precise estimates.
- New modelling requires additional distributional assumptions; results are checked against the old methodology, especially for small data subsets.
- Uses AR1 modelling with bootstrapped standard errors to maintain robustness; benefits include improved precision and coherence across surveys, with past estimates potentially updated as new data arrive.
- Implementation is technically challenging and more computationally intensive, but the AR1 framework provides a practical balance of stability, speed, and robustness for large-scale CS analyses.

## Introduction
- This technical report outlines sampling and analysis procedures for CS data, reviewing previous CS methodology and detailing 2007 changes.
- Fuller expositions of prior CS methods are available in Barr et al. (1993).

## Sampling (2.1)
- CS Field Survey data come from a stratified sample of 1 km squares at the intersection of a 15 km GB grid.
- Two levels of sampling: square-level measurements (for whole squares) and within-square plot measurements (describing features inside squares).
- Measurements vary from binary to continuous (areas, lengths).
- Land Classification (ITE) stratifies square selection; classifications have been updated for country-specific reporting (England, Wales, Scotland).

## Estimation (2.2)
- Original method: estimate regional/national means by calculating land-class means and combining them with area-weighted values.
- This approach makes minimal distributional assumptions but treats stock (all data) and change (repeat measurements) from different data sets, leading to potential inconsistencies.

## Bootstrapping (2.3)
- Significance testing uses bootstrapping due to potential non-normality (reliable for skewed data).
- Bootstrap resamples (typically 1000–10,000) estimate distributions of stock/change, providing robust SEs and CIs.

## Reasons for Modifications (Section 3)
- Previous point estimates (stock vs. change) were considered inconsistent by some users due to different data subsets used for stock and change.
- Inconsistencies arise when all-square data are used for stock but only repeated squares are used for change.
- Reporting shift in 2007 emphasizes timelines across multiple surveys, necessitating genuinely consistent estimates.
- Explored three consistency approaches; modelling was chosen to provide consistent, efficient estimates across square and plot data.

## Modelling Basics (4.2)
- Incomplete data techniques (EM/related mixed-effects models) allow consistent estimation across surveys by leveraging data from all surveys.
- Models include fixed effects (stock/change as functions of surveys) and random effects (reflecting sampling variation).
- More assumptions are required than the previous bootstrap-based approach; however, these enable using all available information and handling the data hierarchy.

## Square Level Data (4.3)
- Data from complete 1 km squares are treated as repeated-measures data within a Land Class.
- Mixed-effects models: fixed effects for land-class means over surveys; random effects include square-level deviations and repeated-measures residuals.
- Within-square measurements are correlated across surveys; the model accounts for this structure.

## Plot Level Data (4.4)
- Plot data within squares can be analyzed with improved modelling to exploit hierarchical structure.
- Previous approaches either aggregated plots to square level or treated plots as independent, risking bias or imprecise SEs.
- The model can incorporate a plot-level residual in addition to the square-level random effect, and both can be embedded in bootstrapping.

## Model Specification (4.5)
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means across surveys)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Distributions: s_ij ~ N(0, τ_i^2) varying by land class; e_ijk ~ N(0, σ_ik^2) with covariances between surveys.
- The full model has many random-effect parameters; to keep fitting feasible, simplifications are used.

## Model Reduction (AR1) and Bootstrap
- Two practical reduction strategies:
  - Equal variances across surveys within a land class (σ_i constant across surveys).
  - Autoregressive AR1 structure for covariances between successive surveys (only one covariance parameter per land class).
- This AR1 approach reduces random parameters to a manageable number (three per survey per land class) and is combined with bootstrap to obtain robust SEs.

## Model Testing – Broad Habitats (4.6)
- Historically, Broad Habitats (proportions within squares) were estimated from 1984, 1990, and 1998 data.
- Old methods showed substantial stock-change inconsistencies; modelling (AR1) produced consistent estimates, with changes matching differences between successive stock estimates.
- Comparisons showed most differences between old and new methods were small relative to their SEs; many were well within old-method discrepancies.

## Limitations and Implications (Section 5)
- Bootstrapped square-level analysis with complex models is computationally demanding but feasible.
- Fixed-effect estimates (stock/change) are robust to some model misspecification; variance/covariance estimates are more sensitive.
- For large variable sets, a standard AR1 model is preferred for automation and robustness; checks are performed by running both old and new methods and comparing results.
- Non-normal data can affect parametric SEs; bootstrap mitigates this.
- Some variables with highly non-normal distributions (e.g., standing water) may diverge between old and new methods; in CS freshwater, older method estimates were retained due to convergence issues.
- The modelling approach uses information from all surveys, potentially updating past estimates as new data arrive; this is conceptually different from prior inconsistencies and is viewed as reasonable with new data.
- Adoption enhances precision and consistency across map-based outputs, though it increases data processing time and requires careful interpretation of updated past results.

## Implications for GIS and Data Products
- Provides consistent, model-based stock and change estimates across surveys, enabling reliable map-based visualisations over time.
- Data updates past survey estimates as new data become available, improving long-term trend maps and habitat assessments.
- Hierarchical modelling (square and plot levels) supports richer spatial summaries and more accurate uncertainty quantification for map displays.
- Requires awareness of underlying modelling assumptions and potential revisions to prior years when reprocessing with the new methodology.