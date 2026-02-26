# Description of the statistical methodology used for the analysis of Countryside Survey data

## Executive Summary
- Describes the statistical methodology for Countryside Survey (CS) data analysis, detailing changes introduced for CS in 2007 from the previous methods.
- Previous methods were robust but used all data for stock and only repeated measurements for change, causing inconsistencies between stock and change estimates.
- Modelling-based, consistent estimation using all available data is adopted for 2007, improving precision but requiring additional distributional assumptions and validation checks.
- New approach uses mixed/repeated-measures modelling with bootstrap for significance, applicable to square and plot level data, and accessible via automated workflows.
- Implementation is computationally intensive but yields more precise estimates; past survey estimates may be revised as new data are incorporated.
- The report demonstrates that modelling-based, consistent estimation aligns with prior results and improves data utilisation.

## CS data and sampling overview
- Data come from a stratified sample of 1 km squares on a 15 km GB grid; each square is mapped and measured at two levels: square-wide and within-square plots.
- Land Classification (ITE) provides strata; classifications have been updated over time (GB 32 → 42 → 45 classes) with country-specific reporting (England, Wales, Scotland).
- Measurements include binary and continuous variables; data are hierarchical (square and plot level).

## Estimation: old vs new approaches
- Old approach: estimate stock using all data from a survey; estimate change from repeated measurements between surveys; leads to inconsistencies between stock and change estimates.
- New approach: aim for consistent estimation of stock and change via modelling that uses data from all surveys and handles missing information coherently.
- Consistency and robustness achieved through modelling; however, this requires stronger distributional assumptions and validation, especially for small subsets of data.

## Modelling approach for consistent estimation
- Incomplete data techniques (mixed effects/repeated measures) are used to handle missing data across surveys.
- Models include fixed effects (stock/change as functions of survey year) and random effects (variation at the square/plot level reflecting sampling design).
- To keep estimation practical, random-effect parameterization is reduced (AR1) to minimize the number of random parameters while preserving robustness of fixed effects.
- Bootstrap is used to obtain standard errors because parametric standard errors may be unreliable for complex variance structures.

## Square level data modelling
- For complete square-level measurements, the data are treated as a random sample of squares within each Land Class, with two components:
  - Fixed effects: land-class means across surveys (stock) modeled as a function of year.
  - Random effects: square-level deviations and survey-to-survey correlations (e.g., AR1 structure) to capture within-square and between-survey variability.
- The general form: y_ijk = a_i_k + s_i_j + e_i_jk, with a_i_k representing fixed effects, s_i_j the square random effect, and e_i_jk the repeated-measures error.
- Distributions: random effects assumed normal; covariances and variances may differ by land class and survey.
- The model includes K surveys and results yield stock estimates by land class and change estimates as differences between survey stocks.
- Due to the large number of potential random parameters, AR1 simplifications are used to maintain tractability.

## Plot level data modelling
- Plot-level data within squares are incorporated to improve efficiency and consistency.
- Previous analyses either aggregating to square level (robust but less precise) or treating plots as independent (potential bias).
- The modelling framework extends to include an additional plot-level residual, creating a two-level structure with square-level and plot-level random effects.
- Both square- and plot-level models can be embedded within bootstrap procedures for robust standard errors.

## Model specification and practical considerations
- General square-level model: y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land-class means across surveys), square random effects s_ij, and within-square repeated-measures e_ijk.
- Random effects and repeated-measures variances/covariances are allowed to vary by land class and survey; however, to keep models estimable, assumptions are made:
  - Random effect variances are allowed to vary by land class but may be held constant across surveys (σ_i).
  - AR1 structure reduces repeated-measures covariances to a single parameter per land class.
- Bootstrap-based standard errors are emphasised for robustness to distributional assumptions, especially when estimates are sensitive to non-normality or complex variance structures.
- For large numbers of variables, a standard AR1+bootstrap approach is recommended for automated, robust analysis.

## Model testing: Broad Habitats
- Historical CS outputs included stock and change estimates for Broad Habitats; prior methods yielded inconsistencies between stock-derived changes and directly estimated changes from repeated squares.
- Modelling with AR1 and bootstrap eliminated these discrepancies; stock and change estimates from the new method aligned with the older method within the prior error bounds.
- Analyses show that changes between non-adjacent surveys derive consistently from the summed adjacent-change estimates.

## Limitations and implications
- AR1-based modelling is computationally intensive but feasible with automated pipelines; more complex models are slower and may be impractical for large variable sets.
- Fixed effects are robust to some mis-specification of random-effect distributions; variance/covariance parameters are more sensitive to distributional assumptions.
- Non-normal variables (e.g., standing water) can cause convergence to local maxima or unreliable estimates; in such cases, older methods may be retained for those variables.
- Adoption of a fully model-based approach means past estimates can be revised as new data are integrated; estimates for any given survey may change slightly with new information.
- The approach utilises all available data and respects data hierarchy, improving precision but requiring automated, standardised modelling.

## References
- Barr et al., Countryside Survey 1990 Main Report; 1993.
- Dempster, Laird, Rubin (EM algorithm); 1977.
- Efron, Tibshirani (Bootstrap); 1993.
- Haines-Young et al. (Accounting for nature: UK habitats); 2000.
- Scott (Maximum likelihood with empirical information); 2002.