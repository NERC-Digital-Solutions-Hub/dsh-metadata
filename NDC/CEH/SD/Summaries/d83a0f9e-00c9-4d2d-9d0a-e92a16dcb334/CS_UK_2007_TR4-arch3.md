Countryside Survey 2007: Consistent Estimation for Stock and Change

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data, detailing changes made for CS in 2007.
- Old methods were robust but produced inconsistencies between stock and change estimates; new modelling-based methods aim for consistency by using all available data.
- Modelling (consistent estimation) is feasible and generally robust; differences from earlier methods are within previous inconsistency ranges.
- The new approach improves precision by leveraging all information and the data hierarchy, though it requires more computation.
- Implementation of modelling is technically challenging; AR1 mixed-effects models with bootstrap were adopted to balance robustness, efficiency, and automation.
- The report compares old and new methods for Broad Habitats (and other data) to validate consistency; results generally align within prior error bounds.
- Adoption of the new methodology for the 2007 CS extends to square and plot-level data, including soil and habitat datasets, enabling a coherent, hierarchical analysis.

## 1. Introduction
- The technical report provides an overview of CS sampling and analysis procedures, outlining reasons for and details of changes for CS2007; prior CS methodology is reviewed.
- CS sampling design: stratified sampling of 1 km squares on a 15 km GB grid; two levels of data collection within each square (square-wide and within-square plots) with varied data types (binary to continuous).
- Land Classification: ITE Land Classification used for stratification; classifications have expanded (GB 32 -> 42 for CS2000; 45 for CS2007) to accommodate separate England, Wales, and Scotland reporting.
- Estimation: previously, means and standard errors were computed per Land Class and combined by area weighting; this assumed independence between Land Classes and between estimates within/among classes.
- Bootstrapping: significance testing shifted to bootstrap methods (1000–10,000 resamples) due to concerns about non-normality, especially for square-level data.

## 2. Overview of Previous CS Methodology
- Stock estimates used all data from a survey; change estimates used only repeated measurements across survey pairs, leading to inconsistencies between stock and change.
- Inconsistencies arose when comparing stock and change across adjacent or non-adjacent surveys due to differing data sub-sets used for stock vs. change.
- The CS2007 reporting shift emphasized timelines from the first survey to the present, highlighting the need for consistent estimates.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies between stock and change were not errors but results of the estimation approach.
- Three potential approaches: (a) use stock estimates from all data and change as differences between stock estimates; (b) use only repeated squares for both stock and change; (c) apply modelling to produce consistent estimates for both stock and change across square and plot data.
- Modelling (option c) offers consistency and robustness, can utilize data from all surveys, and is applicable to both square and plot level data, albeit with additional distributional assumptions.

## 4. Modelling Basics
- Incomplete data techniques (e.g., EM algorithms) allow consistent estimation by leveraging correlation structures rather than simply filling missing values.
- Mixed-effects/repeated-measures models are used to fit data from all surveys, with fixed effects representing Land Class means by survey and random effects capturing sampling variability (squares, plots, repeated measures).
- Models require assumptions about distributions of random and repeated effects; fixed-effect estimates tend to be robust to some mis-specifications.
- To manage model complexity, random-effect parameterization is reduced (e.g., AR1 assumptions) to keep the model tractable for CS’s large number of variables and surveys.

## 4.1 Square Level Data
- Square-level data are treated as a random sample of squares within each Land Class; data across surveys are modeled with a repeated-measures (mixed) model.
- Fixed effects: land-class means per survey (regression of variable on year/survey as a categorical variable).
- Random effects: square-level deviations from land-class means; within-square repeated measures are allowed to be correlated across surveys.

## 4.2 Plot Level Data
- Plot-level data within squares require careful handling of hierarchical structure.
- Earlier analyses either summarized to square level or treated plots as independent, risking inefficiency or bias.
- CS2000 used mixed models that included square-level variation; later approaches added plot-level residuals to capture within-square heterogeneity, with both square and plot level models embedded in bootstrap procedures.

## 4.3 Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik: fixed effects (land-class means by survey)
  - s_ij: square random effects
  - e_ijk: repeated-measures residuals
- Distributional assumptions:
  - s_ij ~ N(0, τ_i^2)
  - e_ijk ~ N(0, σ_ik^2) with covariances for repeated measures within squares
- For K surveys, the model includes K fixed effects and many random-effect parameters; to avoid over-parameterization, assumptions are made to reduce random effects (e.g., same σ_i across surveys; AR1 for covariances).
- AR1 model with bootstrap combines efficiency and robustness, providing consistent SEs for fixed effects.

## 4.4 Model Testing – Broad Habitats
- Historical data (1984, 1990, 1998) for Broad Habitats were analyzed to compare old vs. new modelling approaches.
- Old method: changes estimated from repeated squares vs. stock differences; inconsistencies observed.
- Modelling approach (AR1) produced consistent stock and change estimates; differences with the old method were small and within old inconsistency bounds.
- Analyses extended to soil data (1978 and 1998) and plot-level data, confirming feasibility of consistent estimates across data types.
- Result: CS2007 adopted the modelling approach for analysis.

## 5. Limitations and Implications
- Implementing model-based analysis within a bootstrap framework is computationally intensive but feasible; fixed-effect estimates are robust to model variation.
- Fully parameterized models are slow; the AR1 model provides a practical balance between speed and accuracy for large CS analyses.
- Model assumptions (distribution of random effects) influence standard errors; bootstrap offers robustness for standard errors.
- Some data (e.g., freshwater standing water) exhibited very non-normal distributions, causing convergence issues; in such cases, older methods may be preferred for those variables.
- Benefits of modelling: fully utilizes information and data hierarchy, yielding more precise estimates.
- Updating consequences: because analyses borrow information across all surveys, estimates for earlier surveys may be updated as new data become available; such revisions are expected to be small and reflect new information rather than prior errors.
- Overall, adopting a consistent, model-based approach improves precision and comparability across surveys and data types.

## 6. References
- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, Laird, and Rubin (1977). Maximum likelihood from incomplete data via EM algorithm.
- Efron and Tibshirani (1993). An introduction to the bootstrap.
- Haines-Young et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002). Maximum likelihood estimation using the empirical Fisher information matrix.