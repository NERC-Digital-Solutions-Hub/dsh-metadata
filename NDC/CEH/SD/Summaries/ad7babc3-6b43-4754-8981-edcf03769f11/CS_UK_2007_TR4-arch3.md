# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used for analysing Countryside Survey (CS) data and outlines changes introduced for CS in 2007.
- Identifies inconsistencies in previous methods where stock estimates used all data from a survey while change estimates used only repeated measurements, leading to potential mismatches.
- Demonstrates that consistent estimation via modelling (using all available data) is feasible and robust, providing more precise estimates than older methods.
- Indicates that the modelling approach requires additional distributional assumptions but results can be validated against previous methods; comparisons show most changes fall within prior error bounds.
- Highlights that modelling utilises hierarchical data (square and plot levels) and improves precision, with the caveat of greater computational demand.
- Notes that outputs (stock and change) can be updated as new survey data become available, potentially adjusting previous estimates slightly.
- Reports that the AR1 mixed-effects modelling with bootstrap for standard errors was selected as a practical, robust approach for CS2007 analyses.
- Confirms successful application to Broad Habitats data and suggests broader applicability to plot-level data, not just square-level data.

## Introduction and Context
- The report provides an overview of CS sampling and analysis procedures, reviews the previous CS methodology, and details the reasons and specifics of methodological changes implemented for CS2007.
- CS sampling uses a stratified 1 km square design within a 15 km GB grid, with two levels of sampling (square-level and within-square plots) and varied measurement types.
- Land Classification (ITE) and national adaptations (England, Wales, Scotland) underpin country-specific classifications for reporting.

## Previous CS Methodology and Rationale for Change
- Past methods estimated stock with all survey data and change from repeated measurements, causing inconsistencies between stock and change estimates.
- Investigations showed that consistent estimation via modelling using data across surveys was feasible and generally robust; differences from old methods were typically small relative to existing inconsistencies.
- The shift aims to produce coherent, temporally consistent results (stock and change) across the full timeline of surveys.

## Modelling for Consistent Estimation
- Modelling approach leverages incomplete-data techniques (mixed-effects/repeated measures models) to handle data gaps and to produce consistent stock and change estimates from all available information.
- Models introduce fixed effects (stock/change means by land class over time) and random effects (square-level and plot-level variation, plus their correlations across surveys).
- Practical constraints include a large number of random parameters; therefore, model reduction is used (e.g., AR1 structure) to keep parameter counts manageable and estimation stable.

### AR1 Modelling and Bootstrap
- The AR1 model reduces random-effects parameters by assuming constant variance across surveys and an autoregressive covariance structure between successive surveys.
- Bootstrap methods (non-parametric resampling) are employed to obtain robust standard errors, accommodating non-normal data and complex variance structures.
- This combination (AR1 with bootstrap) is tested to balance robustness, computational feasibility, and accuracy for a large number of analyses.

## Data Structure and Modelling Approaches

### Square Level Data
- Data from complete 1 km squares are modelled as repeated measures with two components: fixed effects (land-class means across surveys) and random effects (square-level deviations and survey-to-survey deviations).
- The basic form: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects, s_ij are square random effects, and e_ijk are repeated-measures errors.
- Assumes normal distributions for random effects with land-class-specific variances; correlations across surveys are modelled.

### Plot Level Data
- Plot-level data within squares are more complex due to hierarchical structure. Earlier analyses either aggregated to square level or treated plots independently, risking inefficiency or bias.
- The modelling framework extends to include plot-level residuals (random effects) in addition to square-level effects, with bootstrapping used to derive standard errors.

### Model Specification and Practicalities
- Full model involves many fixed and random parameters; to maintain practicality, simplifications are made (e.g., common variance across surveys, AR1 covariance structure).
- Emphasizes that fixed-effects estimates are robust to reasonable distributional mis-specifications, while variance/covariance estimates are more sensitive to assumptions.
- When distributions are highly non-normal, data transformation is considered, but results must be presented on the original measurement scale; transformations complicate back-transformation of results.

## Application to Broad Habitats and Other Data
- Re-analysis of Broad Habitats data (from 1984, 1990, 1998) showed the old method’s stock-change inconsistencies were largely eliminated under the modelling approach.
- Models (AR1) produced estimates that were within the ranges of prior methods, with improved internal consistency.
- Additional consistency checks were performed on soil data and plot-level data, supporting the feasibility of consistent estimation across data types.
- Based on these checks, CS2007 adopted the modelling approach for broader data analyses.

## Limitations and Implications
- Computation: Model-based analyses are more computationally intensive, particularly for large variable sets; AR1 offers a practical balance between performance and speed.
- Model selection: A standard AR1 + bootstrap approach is used for automation across many variables; more complex models may offer marginal gains but are often impractical at scale.
- Distributional assumptions: Fixed-effects estimates are robust to some mis-specifications, but variance/covariance estimates depend on distributional assumptions; bootstrap ameliorates some risk.
- Non-normal data challenges: Very non-normal variables can lead to convergence issues; in some cases, results from the old method remain the default.
- Updating estimates: As new surveys are added, previous survey estimates may be revised upward or downward, reflecting new information; this is a feature of fully integrated data usage rather than a shortcoming.
- Overall impact: The modelling approach is more efficient, makes full use of available information, respects data hierarchy, and yields more precise estimates, justifying the transition for CS2007.

## Practical and Governance Considerations for Monitoring Frameworks
- Data integration: Demonstrates the value of combining data across time and hierarchical levels to obtain coherent measures of stock and change.
- Metadata and data sharing: Highlights the importance of clear metadata and accessible underlying data to support transparent, governance-ready outputs.
- Transparency and communication: Emphasizes presenting results on the original measurement scale and clearly communicating uncertainties through bootstrapped intervals.
- Automation and scalability: Proposes a standard, automatable modelling framework suitable for large, multi-variable monitoring programs.
- Data governance: Points to the necessity of maintaining consistent methodological standards over time, while allowing for updates as new data become available.

## Key References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P. et al. (1977). Maximum likelihood from incomplete data via the EM Algorithm.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.