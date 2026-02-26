# Countryside Survey 2007 Methodology

## Executive Summary
- Describes the statistical methodology for Countryside Survey (CS) data and changes implemented for CS2007.
- Previous methods produced stock estimates from all survey data and change estimates from repeat measurements, causing inconsistencies between stock and change.
- Modelling via consistent estimation (mixed effects/repeated measures, AR1) is feasible, robust, and yields more precise estimates; differences from old methods are generally within existing inconsistencies.
- The modelling approach uses all available information, improves precision, and allows past survey estimates to be updated as new data are added (typically with small changes).
- Implementation is computationally intensive; AR1 modelling balances robustness, speed, and a small, stable parameter set; extensive checks compare new and old methods.
- For Broad Habitats, soil, and plot-level data, the modelling approach provides consistent estimates across time and data levels; CS2007 adopts this methodology.

## Introduction
- Technical report outlining sampling and analysis procedures for CS data; reviews previous CS methodology, explains why modifications were needed for CS2007, and discusses limitations and implications.

## Sampling and Data Structure
- Data come from a stratified sample of 1 km squares within a 15 km GB grid; each square is mapped and measured, with some measurements within squares (plots) as well.
- Two data levels: square-level (whole square) and plot-level (within-square plots).
- Land Classification (ITE) divides the landscape into classes; classifications have been updated over time (GB to England/Wales/Scotland-specific classifications).

## Estimation
- Old approach: estimate means and standard errors for each Land Class, then combine (weighted by land-area) to produce regional/national stock or area estimates.
- Assumes independence between Land Classes and between class estimates and total land; minimal distributional assumptions.

## Bootstrapping
- Significance testing uses bootstrap rather than normality assumptions due to potential skewness, particularly for square-level data.

## Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock was estimated from all data while change was estimated from repeated data; reported inconsistencies could be misinterpreted as errors.
- Several approaches to achieve consistency were considered; modelling (consistent estimation) using data from all surveys was chosen for robustness, efficiency, and applicability to both square and plot data.
- Modelling requires distributional assumptions; results are validated by comparison with the old method, especially for small subsets.

## Modelling Basics
- Incomplete-data techniques underpin consistent estimation; mixed effects/repeated measures models handle missing data and hierarchical structure.
- Models include fixed effects (stock/change values) and random effects (sampling variation). The distributional form of random effects must be specified.
- Full models can be large and unstable; practical reduction of random effects is achieved (e.g., AR1 structure) to manage parameter counts and computation.
- Bootstrap can provide robust standard errors when variance/covariance parameters are difficult to estimate precisely.

## Square-Level Data
- Treat the CS square-level dataset as a random sample of squares within each Land Class.
- A repeated-measures mixed model is used: fixed effects capture land-class means across surveys; random effects account for square-level variation and within-square survey correlations.

## Plot-Level Data
- Plot measurements within squares can be modeled with an extended mixed model that includes plot-level residuals in addition to square-level random effects.
- Both square-level and plot-level models can be embedded within bootstrap procedures for standard errors.

## Model Specification
- General form for square-level data: y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land-class means across surveys), square random effects s_ij, and repeated-measures residuals e_ijk.
- Random effects are typically normal with land-class-specific variances; correlations across surveys are modelled (often AR1).
- Reducing random-effect parameters (e.g., assuming common variance across surveys, AR1 covariance structure) improves stability and feasibility for many analyses.

## Model Testing – Broad Habitats
- Re-analysis of Broad Habitat data from key surveys showed the modelling approach removes stock-change discrepancies observed under old methods.
- Stock estimates and change estimates from the new modelling approach are consistent with differences within historic inconsistencies.
- Similar consistency checks extended to soil data and plot-level data; adoption of the modelling approach for CS2007 is supported.

## Limitations and Implications
- AR1 modelling with bootstrapped SEs is robust for fixed effects but increasingly slow with many variables; a balance between robustness and practicality is required for large CS analyses.
- Model selection is streamlined for automated application across many variables; fixed-effects estimates are robust to some mis-specifications in random effects, but variance/covariance estimates can be sensitive.
- Very non-normal data can destabilize estimation (e.g., standing water variables); in some cases, old methodology may be retained for those variables.
- Adopting a full, data-integrative modelling approach means past survey estimates can be revised when new data are added; updated estimates are generally small but reflect new information.
- Outputs are delivered as reports, maps, and charts; datasets are stored and uploaded to appropriate portals to facilitate access and reuse.

## References
- Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron & Tibshirani (1993), Scott (2002), plus CS2007 materials and CS2000 methodology.