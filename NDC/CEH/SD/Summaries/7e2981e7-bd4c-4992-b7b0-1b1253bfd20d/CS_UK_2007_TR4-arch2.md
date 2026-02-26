# Countryside Survey 2007 Methodology

## Executive Summary
- Describes the statistical methodology used for Countryside Survey (CS) data analysis and outlines changes implemented for CS in 2007.
- Previous methods were robust but produced inconsistencies between stock and change estimates due to using different data subsets; new modelling provides consistent estimates.
- Modelling via mixed effects/repeated measures is feasible and generally robust; differences from old methods are small.
- The new approach uses all available information, yielding more precise estimates; estimates for earlier surveys may be revised as new data inform the model.
- Implementation is technically challenging and more computationally intensive than prior methods.
- Validation shows the modelling approach delivers consistent results and is adopted for 2007 CS outputs.
- Bootstrapping is used to obtain standard errors and confidence intervals, accommodating non-normal data distributions.
- The approach was tested on Broad Habitat data and other datasets, reinforcing consistency across survey periods.

## Data and Sampling
- CS field data come from a stratified sample of 1 km squares on a GB-wide 15 km grid; measurements occur at two levels: square level and within-square plot level.
- Land Classification (ITE) classifications have evolved: 32 classes originally, 42 for CS2000 (Scotland reporting), and 45 for CS in 2007 (Wales reporting added); each country has a related national classification.
- Measurements include binary and continuous variables, with area/lengths as examples.

## Estimation and Inconsistencies
- Old method: stock estimates used all data from a survey; change estimates used only repeated measurements across survey pairs, causing potential mismatches between stock and change.
- This led to apparent inconsistencies when comparing adjacent vs. non-adjacent survey changes.
- CS2007 shifts emphasis to consistent estimates across the full timeline (from the first survey to the present) to improve interpretability.
- Considered approaches to achieve consistency; modelling was chosen for its ability to provide consistent, efficient estimates across square and plot data.

## Modelling Approach for Consistent Estimation
- Mixed effects/repeated measures models are used to obtain stock and change estimates consistently across surveys.
- Models rely on distributional assumptions for random effects; the fixed effects capture land-class means per survey, while random effects capture hierarchical variation (squares/plots).
- To keep the model tractable, random effect parameters are reduced (AR1 structure), resulting in three random parameters per land class per survey.
- Bootstrap is used to obtain standard errors, ensuring robustness to distributional misspecification.

## Square-Level Data
- Model form: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik: fixed effects (land-class means for survey k),
  - s_ij: square-level random effect,
  - e_ijk: repeated-measures error.
- Random effects are assumed normal with land-class-specific variance; repeated-measures errors have covariances that vary by land class and survey.
- With K surveys, the model includes fixed effects for each survey and a manageable number of random parameters, enabling practical fitting.

## Plot-Level Data
- Plot-level data within squares add complexity; previous analyses either aggregated to square level or treated plots as independent.
- Extended modelling includes a plot-level residual in addition to the square-level random effect, enabling correlations at the plot level and allowing embedding within bootstrapping.

## Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk, with distributions for s_ij and e_ijk specified.
- A large number of random-effect parameters can arise; reducing them via assumptions (e.g., AR1, constant variance across surveys) improves stability and tractability.
- AR1 (first-order autoregressive) covariance reduces parameters to a small, consistent set across surveys.
- Distributional misspecification primarily affects variance estimates; fixed-effect estimates (stock/change) are relatively robust; bootstrap standard errors help maintain validity.

## Model Testing – Broad Habitats
- Historical Broad Habitat data (1984, 1990, 1998) were analyzed to assess modelling feasibility.
- Old approach yielded inconsistencies between stock and change; the AR1 modelling approach produced consistent estimates, with no significant departures beyond what is expected by methodological differences.
- Differences between old and new methods were generally within the old method’s error bounds; results from modelling aligned with prior discrepancies in a robust way.
- Similar consistent analyses extended to soil and plot-level data, supporting broad applicability of the modelling approach.

## Limitations and Implications
- AR1 modelling with bootstrapped SEs is computationally demanding but feasible; fixed-effect estimates are robust to some model variation.
- Fully parameterised models are slow; AR1 offers a practical balance of speed and reliability for large numbers of analyses.
- A standardized modelling approach is essential for automation and consistency across many variables.
- Analyses involve data from all surveys; estimates for any one survey may be revised as new data are incorporated.
- Non-normal data can affect variance estimates; when non-normality is severe, transformations may be needed, though results are preferred on the original measurement scale.
- In some datasets (e.g., freshwater standing water), non-normality caused convergence to local maxima; in such cases, older methods may be reported.
- Adoption of consistent estimation improves precision by leveraging all information and properly representing data hierarchy; it also implies ongoing updates to previous survey estimates as new data arrive.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron & Tibshirani (bootstrap); Scott (2002) on empirical Fisher information.