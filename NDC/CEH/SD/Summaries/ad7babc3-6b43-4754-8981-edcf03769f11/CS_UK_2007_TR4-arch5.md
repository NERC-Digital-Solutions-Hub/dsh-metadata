# Statistical methodology for Countryside Survey data (CS2007)

## Executive Summary
- Purpose: describes the statistical methodology used to analyze Countryside Survey (CS) data, highlighting changes from previous methods and detailing the modelling approach adopted for CS2007.
- Key shift: from estimations based on separate stock and change calculations with minimal assumptions to a consistent, model-based estimation framework that uses all available data across surveys.
- Benefits: more precise estimates by leveraging complete information; consistency between stock and change estimates; potential improvements to past survey estimates as new data are incorporated.
- Trade-offs: modelling requires distributional assumptions and greater computational effort; results may update as new surveys are added.
- Validation: comparisons with old methods show differences generally within existing uncertainties; Broad Habitat and plot/square data analyses support feasibility and consistency of the new approach.
- Implementation notes: AR1 mixed-effects models with bootstrap for standard errors; plans for automated, scalable application to large numbers of variables; explicit checks comparing new and old methods to ensure robustness.

## Data Structure and Sampling
- Two-level sampling design:
  - Level 1: complete 1 km squares selected from a stratified sample across a 15 km GB grid.
  - Level 2: within-square plots/quadrat measurements (vegetation, soils, etc.).
- Stratification by Land Classification (ITE classifications), with country-specific adaptations:
  - England, Wales, Scotland each have distinct but related classifications (CS2007 features 45 Land Classes overall).
- Data types vary from binary to continuous (areas, lengths); multiple measures per square and per plot.

## Estimation and Modelling Approach
- Old methodology:
  - Stock estimates used all data from a survey; change estimates used only repeated measurements across surveys, creating potential inconsistencies between stock and change.
  - Weighted means by land class area used to obtain regional/national estimates; assumptions of independence between Land Classes.
- New methodology (consistent estimation):
  - Modelling framework (mixed effects/repeated measures) applied to data from all surveys, producing stock and change estimates that are internally consistent.
  - Square-level data: yijk = aik + sij + eijk, where aik are fixed effects (land-class means per survey), sij are square-level random effects, and eijk are repeated-measures residuals.
  - Random effects: normally distributed with land-class-specific variances; repeated measures have covariances that may vary by land class and survey.
  - Plot-level data: extended models include plot-level residuals in addition to square-level structure; bootstrapping accommodates complex residual structures.
  - Model specification emphasizes robustness: fixed effects estimation is relatively robust to mis-specification of random effects; variance/covariance parameters are more sensitive to distributional assumptions.
  - AR1 (autoregressive order 1) simplification: common variance/covariance structure across surveys reduces parameter count (three random-effect parameters per survey) while retaining essential correlation structure.
  - Bootstrapping: employed to obtain standard errors and confidence intervals, particularly important where distributional assumptions are uncertain or non-normalities exist.
- Model testing and validation:
  - Broad Habitat analyses compared old vs. new methodologies; new models produced results within the old method’s error bounds, with improved internal consistency.
  - Analyses extended to soil data (1978, 1998) and plot-level data, confirming feasibility of consistent estimation across data types.

## Handling Missing Data and Consistency
- Incomplete data (e.g., unrepeated squares, landowner refusals) historically caused inconsistencies between stock and change estimates.
- Modelling approach treats missing information through structured random effects and correlations across surveys, rather than imputing exact values.
- Consistency achieved by ensuring change estimates align with differences in stock estimates within the modelling framework; results are coherent across adjacent and non-adjacent survey periods.
- If needed, outcomes can update with new surveys, reflecting information from all available data; past results may be revised modestly as data accumulate.

## Model Specification and Computation
- Square-level model structure:
  - yijk = aik + sij + eijk
  - aik: fixed effects (land-class means per survey)
  - sij: square-level random effects
  - eijk: repeated-measures residuals
- Distributional assumptions:
  - sij ~ N(0, τi^2)
  - eijk ~ N(0, σik^2) with land-class and survey-specific variances; covariances for squares across surveys modeled
- Parameter considerations:
  - Large numbers of random-effect parameters can hinder stability and speed; AR1 and common-variance assumptions help manage complexity.
  - Fixed effects are relatively robust to random-effects mis-specification; variance/covariance estimates require careful modelling.
- Practical considerations:
  - Fully parameterised models are slow; AR1 with bootstrap strikes a balance between accuracy and computational feasibility for large-scale CS analyses.
  - Automated, standardized modelling workflow is desirable to handle the large number of variables consistently.

## Plot vs. Square Level Data
- Square-level data: robust mixed-models with repeated measures; bootstrapping used for SEs.
- Plot-level data: initial analyses treated plots within squares as independent or aggregated, which could misrepresent variance; updated practice includes plot-level residuals to capture within-square variability.
- Bootstrapping applicable to both data levels to maintain robust inference despite potential non-normality.

## Limitations and Implications for Data Governance
- Distributional assumptions: fixed-effects estimates are robust, but variance/covariance parameters depend on assumed distributions; bootstrap mitigates some risks.
- Non-normal data: certain variables (e.g., freshwater standing water) can lead to convergence issues; in such cases, legacy methods may be preferred for those variables.
- Cross-survey updates: as new CS data are added, past survey estimates may be revised; data systems must support versioning and provenance to reflect these updates.
- Practicality vs. ideal modelling: a balance is struck between model fidelity and computational practicality; a standard AR1-based approach with bootstrap is advocated for large-scale automation.
- Implications for reporting: the new methodology emphasizes consistency across the entire time series; reporting can reflect evolving estimates as new data are integrated, rather than fixed values from a single survey period.

## Practical Considerations for Data Managers and Stewards
- Data architecture should support:
  - Longitudinal, hierarchical data structures (squares, plots, land classes, surveys)
  - Storage of model specifications, random-effects structures, and covariance parameters
  - Versioning and audit trails to capture updates when new surveys are analyzed
  - Reproducible workflows and automated analyses for scalable application across many variables
- Metadata needs:
  - Clear documentation of sampling design, land-class definitions, and country-specific classifications
  - Details on modelling choices (AR1, bootstrap procedures, fixed vs random effects)
  - Assumptions and limitations, including when legacy methods are used for specific variables due to non-normality
- Data discovery and sharing:
  - Ensure discoverability of both stock and change estimates along with associated uncertainty
  - Provide access to both old (where still relevant) and new modelling results for transparency and comparability
  - Communicate that past estimates may be revised as new data are incorporated, and provide guidance on interpreting updates

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002)
- Countryside Survey data, methodology, and validation discussions within the CS2000 and CS2007 frameworks