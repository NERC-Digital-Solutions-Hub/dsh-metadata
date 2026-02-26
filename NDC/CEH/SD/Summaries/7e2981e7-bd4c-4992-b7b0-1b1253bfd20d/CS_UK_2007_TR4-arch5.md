# Countryside Survey 2007: Consistent Estimation

## Executive summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for CS 2007 to achieve consistency between stock and change estimates.
- Previous methods used all data for stock but only repeated measurements for change, causing inconsistencies between stock and change estimates.
- Modelling approaches (consistent estimation) using all available data produce more precise (efficient) estimates, with changes in estimates generally small relative to prior inconsistencies.
- A modelling framework was adopted (AR1 mixed-effects models with bootstrapping) to provide robust, consistent stock and change estimates for square and plot level data.
- Although more computationally intensive, the modelling approach leverages hierarchical data structure and all available information, improving precision.
- The switch required careful validation and checks against older methods, and it was decided to apply the new method to the 2007 CS data while providing compatibility checks with the old approach.
- The report also covers limitations, practical implementation considerations, and implications of updating results with new survey data.

## What the CS data and design look like
- Data originate from a stratified sample of 1 km squares across a 15 km grid covering Great Britain; each square has land-class (Land Class) stratification.
- Within each square, measurements are taken at two levels: square-level (covering the whole square) and plot-level (within the square), with a variety of data types (binary and continuous).
- Land Class classifications have evolved over time (GB to country-specific classifications with 21 England, 8 Wales, 16 Scotland classes in CS 2007).

## Estimation approaches and rationale
- Old approach: stock estimates computed from all data in a survey; change estimates computed from repeated measurements only. This created inconsistencies because stock and change drew on different data subsets.
- New approach: modelling to obtain consistent estimates of both stock and change, using data from all surveys in a single framework. This approach yields more precise estimates and ensures internal consistency across time.
- Bootstrapping is used to obtain standard errors and confidence intervals due to potential non-normality in some features.

## Modelling framework (square-level data)
- Data are treated as a random sample of squares within each land class; a repeated-measures (mixed) model is used.
- Basic fixed effects: land-class means across surveys (treated as year/survey indicators).
- Random effects describe square-level deviations and the correlation structure of repeated measurements across surveys.
- The general model is: y_ijk = a_ik + s_ij + e_ijk, with:
  - a_ik: fixed effects for land class i in survey k
  - s_ij: square-level random effects
  - e_ijk: repeated-measure residuals
- Random effects include variances and covariances that can be complex; to keep the model stable, variance-covariance parameters are often constrained (see AR1 below).

## Plot-level data and extensions
- Plot-level data add another layer of residuals (plot-level random effects) in addition to square-level effects.
- Two modelling options exist: (1) include only square-level structure, or (2) add plot-level residuals and allow correlations at the plot level across surveys.
- Both square- and plot-level models can be implemented within bootstrap procedures to obtain robust SEs.

## Practical model specification and simplifications
- A full multivariate random-effects specification with many parameters is often unstable given CS’s many land classes and relatively few squares per class.
- Simplifications used (AR1 model, common variance parameters across surveys) reduce parameter count while preserving essential structure:
  - AR1: assumes a first-order autoregressive structure for covariances across successive surveys.
  - Common variance for repeated measures across surveys (σ_i) reduces per-land-class parameters.
- These simplifications yield three random-effect parameters per land class per survey, making automated, large-scale application feasible.
- Bootstrapping is used for standard errors because parametric SEs can be unreliable under complex variance structures.

## Model testing and Broad Habitats
- Historically, CS reports included Broad Habitat stocks and changes estimated from stock and repeat-squares; inconsistencies were evident under old methods.
- Modelling with AR1 and bootstrapping removed discrepancies between stock and change across the tested habitat data (1984, 1990, 1998) and ensured consistency by construction.
- Comparisons show most differences between old and new methods are within prior inconsistency ranges, and changes are generally small in magnitude.

## Limitations and implications
- The AR1 model with bootstrapped SEs is robust for fixed effects but relies on distributional assumptions for random effects; mis-specification can affect SEs, though bootstrap mitigates this.
- Some variables with highly non-normal distributions (e.g., standing water in freshwater data) can cause convergence to local maxima; in such cases, older methods may be preferred for those variables.
- Fully parameterised models are slow; AR1 provides a good balance of speed and robustness for CS-scale analyses.
- Analyses now reflect information from all surveys; estimates for any given survey can be updated as new data are added, which means historical results may shift slightly with new information.
- The approach supports consistent analyses across plot and square levels and across time, but requires careful documentation of model choices and transparency for data users.

## Implications for data governance and stewardship
- Data lineage: clear documentation of modelling choices, assumptions, and the switch from old to new methodology is essential.
- Metadata: capture detailed model specifications, variance-covariance structures, and bootstrap procedures to enable reproducibility.
- Versioning: prepare for updates to past survey estimates as new data become available; maintain access to both old and new method results for comparability.
- Automation: adopt a standard, automated modelling pipeline to produce robust estimates across many variables and surveys.
- Transparency: provide diagnostics comparing old and new methods and document any exceptions (e.g., non-normal data cases) and their handling.

## Takeaways for data stewardship
- Consistent estimation across CS surveys improves accuracy and comparability by leveraging all available data and respecting the data hierarchy.
- The AR1 mixed-effects modelling framework, combined with bootstrapping, offers robust, scalable, and auditable estimates for stock and change at both square and plot levels.
- While more computationally intensive, the approach enhances data governance through improved precision, explicit assumptions, and reproducible workflows.
- Documentation and metadata should reflect model choices, validation checks, and the implications of updating past results with future data.