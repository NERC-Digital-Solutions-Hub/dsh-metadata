# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology for analyzing Countryside Survey (CS) data, outlining previous methods and detailing changes implemented for CS in 2007.
- Previous stock estimates used all data from a survey, while change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling-based, consistent estimation is feasible and robust; results with the new method differ little from old estimates, and are more precise because all available information is used.
- The modelling approach requires additional distributional assumptions; validity is checked by comparing with previous methods, especially for small data subsets.
- Implementation is technically challenging and computation-intensive, but yields a substantially improved product; the AR1 modelling framework with bootstrapping is adopted for CS2007.
- Because analyses combine data from all surveys, past estimates can be updated when new data are added, leading to small revisions to earlier findings.

## Background and Aims
- Aim to provide a consistent, data-driven description of environmental condition over time to support scrutiny of environmental health and policy performance.

## Data and Sampling
- CS data come from a stratified sample of 1 km squares on a 15 km GB grid.
- Two levels of sampling: square level (whole square) and plot level (within-square plots).
- Variables range from binary to continuous; land classifications have evolved (GB: 32 → 42 → 45 classes) with country-specific classifications (England, Wales, Scotland).

## Estimation and Bootstrapping
- Old method: compute means and standard errors per Land Class and combine (weighted by land area) to regional estimates; assumed data independence across Land Classes.
- Significance testing used bootstrap due to non-normality concerns (CS2000 onward).

## Reasons for Method Modifications
- Inconsistencies: stock estimates used all data while change estimates used repeated data, leading to mismatches.
- New methods aim for consistency across stock and change estimates and across non-adjacent survey intervals.
- A modelling approach (consistent estimation) was explored and adopted for CS2007.

## Modelling Basics
- Incomplete data techniques (mixed effects and repeated measures) are used to obtain consistent estimates of stock and change.
- Models include fixed effects (stock/change values) and random effects (reflecting sampling structure and variability).
- Models require distributional assumptions; fixed-effect estimates are robust to some mis-specifications, but variance/covariance parameters are more sensitive.

## Square Level Data
- Data treated as repeated measures within Land Classes; a mixed effects model with fixed Land Class means by survey and random square effects.
- Correlations across surveys are modelled, acknowledging the hierarchical sampling.

## Plot Level Data
- Plot data within squares are accommodated by extending the model to include plot-level residuals in addition to square-level effects.
- Both square- and plot-level random effects can be embedded within bootstrap procedures.

## Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk, with a_ik as fixed effects (land class means by survey), s_ij as square random effects, and e_ijk as repeated-measures errors.
- Random effects are normally distributed with land-class-specific variances; repeated-measures covariances vary by land class and survey.
- To keep the model tractable, random effects are simplified using approaches like AR1 (common variance across surveys and autocorrelated covariances).
- AR1 reduces random parameters to three per survey; bootstrap estimation of standard errors remains robust.

## Model Testing – Broad Habitats
- Re-assessed stock and change for seven Broad Habitats using old and new methodologies (1984, 1990, 1998 data).
- AR1 modelling produced estimates consistent with the old approach within prior discrepancies; differences largely fell within old error bounds.
- Findings supported adopting the new modelling methodology for CS2007, including for plot- and soil-level data.

## Limitations and Implications
- Bootstrapping square-level data is computationally demanding; fixed effects are robust to model variation, but full parameterisation can be slow.
- Auto-regressive (AR1) model offers a good balance of stability, speed, and robustness for large-scale CS analyses.
- Analyses across all surveys mean past estimates may be updated as new data become available; reporting across time thus differs from past practice but remains consistent in interpretation.
- Some variables with highly non-normal distributions (e.g., standing water) may challenge convergence; in such cases, older methods may be reported for those variables.
- Overall, the approach uses all available information and respects data hierarchy, producing more precise, consistent estimates suitable for long-term environmental monitoring and policy evaluation.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (1977); Efron & Tibshirani (1993); Scott (2002) and related CS2000 materials.