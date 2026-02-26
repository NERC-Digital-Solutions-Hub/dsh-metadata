# Statistical methodology for Countryside Survey data

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and changes made for CS 2007.
- Highlights a shift from stock/change estimates based on different data subsets to a consistent modelling approach that uses all available information.
- Finds that modelling provides more precise estimates and reduces inconsistencies between stock and change, while requiring additional data distribution assumptions.
- Notes that the AR1 mixed-effects modelling approach, combined with bootstrapping for uncertainty, offers a robust and efficient solution, though it increases computational demands.
- Emphasises the need to check results against previous methods, particularly for small data subsets, and acknowledges potential updates to past results as new data are added.

## Context and Sampling
- CS data come from a stratified sample of 1 km squares within a 15 km GB grid; measurements occur at two levels: square level and within-square plot level.
- Land Classification underpins stratification; classifications have evolved (GB → country-specific classes) to support separate reporting (England, Wales, Scotland).
- Data types range from binary to continuous measurements (areas, lengths).

## Previous Methodology and Issues
- Earlier estimation combined means/standard errors by Land Class to produce region-wide estimates, assuming independence across Land Classes.
- Stock estimates used all data from a survey; change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Discrepancies arose because different data sets were used for stock vs. change, especially when squares appeared in only one survey.
- Reporting focused on changes since the immediately preceding survey; this could exaggerate apparent inconsistencies when viewed over longer timelines.

## Reasons for Methodological Modifications
- To produce consistent estimates across surveys by using modelling to incorporate data from all years.
- Modelling addresses missing information more coherently than simply comparing stock to repeated-square changes.
- Modelling can be applied to both square and plot-level data, yielding more efficient (precise) estimates, though it requires stronger distributional assumptions.
- To ensure robustness, results from new modelling are compared with the old method, especially for small subsets.

## Modelling Basics and Approach
- Purpose: obtain consistent stock and change estimates by integrating data across all surveys via mixed-effects/repeated-measures models.
- Key idea: fixed effects capture land-class means across surveys; random effects account for square-level and plot-level variation and their correlations over time.
- Data structures:
  - Square-level data: treated as repeated measures within land classes; a mixed model with fixed effects (land class means over time) and random effects (square-level deviations, repeated-measures deviations).
  - Plot-level data: within-square plots introduce additional residuals; models extended to include plot-level random effects and correlations; bootstrapping can be used to derive standard errors.
- Model specification (high level):
  - y_ijk = a_ik + s_ij + e_ijk
  - where a_ik are fixed effects (land-class means across surveys), s_ij are square-level random effects, and e_ijk are repeated-measures residuals.
  - Random effects are typically assumed normal with land-class-specific variances; covariances across surveys are modelled (e.g., AR1 structure to reflect time correlations).
- Practical modelling choices:
  - Full models with many random parameters can be unstable with limited data per land class.
  - To keep models tractable, reduce random parameter count by assuming common variance components across surveys (and often across land classes) and by adopting an AR1 structure for covariances.
  - The AR1 + bootstrap approach was adopted to balance robustness, efficiency, and computational feasibility.

## Handling Data and Procedures
- Bootstrapping is used to obtain confidence intervals and significance when normality is questionable, accommodating non-normal distributions.
- Two-level data (square and plot) require careful treatment of hierarchical structure; plotting and square-level aggregation have to reflect within-square and between-square variation.
- Model fitting is computationally intensive, especially when scaling to many variables; a standard automated AR1-based approach was chosen for practicality and consistency.

## Model Testing: Broad Habitats
- Used to evaluate stock and change across seven Broad Habitats with data from 1984, 1990, and 1998.
- Old methods showed inconsistencies between stock-derived changes and directly estimated changes from repeated squares.
- The AR1 mixed-effects modelling approach provided consistent estimates where stock and change matched the differences implied by consecutive inter-survey periods.
- Comparisons indicated the new method generally aligned with or exceeded the reliability of the old approach, with differences typically within existing error bounds.
- Extension to plot-level data and soil datasets demonstrated feasibility of consistent estimation beyond square level, informing adoption for 2007 results.

## Limitations and Implications
- Implementing model-based analyses within a bootstrap framework is computationally demanding, but fixed-effect estimates are robust to moderate modelling variations.
- Fully parameterised models are slow; the AR1 approach offers a practical balance between speed and accuracy.
- Results for past surveys can be updated as new data from subsequent surveys become available; estimates for any given year may shift slightly with new information.
- Distributional assumptions for random effects influence variance/covariance estimates; bootstrapping helps preserve robustness for standard errors.
- Certain non-normal variables (e.g., standing water) may not converge well with the modelling approach, leading to selective reporting choices (retaining old method results for those variables).
- Overall, the modelling approach makes more efficient use of all available information and better reflects data hierarchy, though it requires explicit governance around data sharing and metadata to support reproducibility and transparency.

## Data Governance and Monitoring Implications
- Data openness: increased emphasis on sharing underlying data to promote transparency; metadata quality is essential to assess data suitability for modelling.
- Data management: need to establish standards at the data source to support robust modelling and long-term comparability.
- Stakeholder engagement: consistent, model-based outputs help stakeholders understand long-term environmental change; clear communication of estimates and their uncertainties is essential.
- Update cycles: yearly data updates can revise past results; monitoring frameworks should accommodate iterative revisions rather than presenting fixed historical figures.

## References
- Barr et al. (1993); Countryside Survey 1990 Main Report
- Dempster, Laird, and Rubin (1977); EM algorithm for incomplete data
- Efron and Tibshirani (1993); Bootstrap
- Haines-Young et al. (2000); Accounting for nature: assessing habitats in the UK countryside
- Scott (2002); Maximum likelihood estimation using the empirical Fisher information matrix