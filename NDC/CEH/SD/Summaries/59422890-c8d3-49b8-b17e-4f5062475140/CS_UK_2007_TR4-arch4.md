# Countryside Survey 2007: Statistical Methodology

- Executive Summary
  - Describes the statistical methodology used to analyse Countryside Survey (CS) data, summarising previous methods and detailing changes implemented for CS in 2007.
  - Previous approach: stock estimates used data from the whole survey; change estimates relied on repeated measurements. This created inconsistencies between stock and change estimates.
  - Modelling approach (consistent estimation) via data modelling was shown feasible and robust using CS Broad Habitat data; differences from old methods were generally small relative to existing inconsistencies.
  - For 2007, modelling methods were adopted to utilise all available information and yield more precise estimates. This approach requires additional distributional assumptions; results are checked against the old methodology, especially for small data subsets.
  - Benefits: improved precision by using all information and preserving data hierarchy; updates to past estimates are possible as new surveys add information, though changes are typically small.
  - Implementation challenges: modelling is technically demanding and more CPU-intensive than the previous formula-based approach; AR1 mixed-effects modelling with bootstrapped standard errors was chosen for robustness and practicality.
  - Validation: comparisons with old methods show differences typically within existing error bounds; Broad Habitats testing and soil/plot-level analyses supported extending the approach to 2007 CS.
  - Outcome: adoption of a consistent estimation framework for CS2007, with plans to automate the method across many variables.

- 1. Introduction
  - Provides an overview of sampling and analysis procedures for Countryside Survey data; reviews the previous CS statistical methodology and outlines reasons for and details of the 2007 estimation changes; discusses limitations and implications of the new methods.

- 2. Overview of previous CS methodology
  - 2.1 Sampling
    - CS field data come from a stratified sample of 1 km squares on a GB-wide 15 km grid, with measurements at two levels: square-level (whole square) and within-square plot-level. Variables range from binary to continuous, and land-class stratification guides square selection.
  - 2.2 Estimation
    - Regional/national estimates were produced by combining land-class means (weighted by land area). This method made few distributional assumptions and treated land-class estimates as independent.
  - 2.3 Bootstrapping
    - Significance testing used bootstrapping due to concerns about normality, especially for square-level data, providing robust standard errors and confidence intervals without assuming normal distributions.

- 3. Reasons for modifications to CS methodology
  - Past reporting produced apparent inconsistencies between stock and change due to using all data for stock but only repeated data for change.
  - Missing information across survey pairs (new squares introduced over time; occasionally, squares missing due to landowner refusal) contributed to inconsistencies in adjacent vs. non-adjacent survey changes.
  - Three potential approaches to consistency were considered; modelling (consistent estimation) offered the advantages of consistency and efficiency, and could be applied to both square and plot level data, albeit with additional distributional assumptions.

- 4. Consistent Estimation
  - 4.1 Possible approaches
    - Discusses potential strategies to achieve consistency; highlights that using all data for stock while using repeated data for change yields inconsistencies; modelling offers a coherent framework for stock and change.
  - 4.2 Modelling basics
    - Incomplete data techniques (e.g., EM-like methods) enable consistent estimation by leveraging correlations in repeated measurements; however, they require distributional assumptions.
    - Mixed-effects/repeated-measures models are fitted to data from all surveys; fixed effects represent stock/change across surveys; random effects capture sampling variation.
  - 4.3 Square level data
    - For complete 1 km squares, data are treated as a random sample within each Land Class; a repeated-measures (mixed) model is used with fixed effects for land-class means by survey and random square effects; correlations across surveys are modelled.
  - 4.4 Plot level data
    - Plot-level data are more complex; previous analyses either collapsed plots to square level or treated plots as independent, which could bias SEs. The modelling framework extends to include plot-level residuals (random effects) in addition to square-level effects; both forms can be bootstrapped.
  - 4.5 Model specification
    - General model: y_ijk = a_ik + s_ij + e_ijk, with a_ik as fixed effects (land-class means by survey), s_ij as square random effects, and e_ijk as repeated-measures errors.
    - Distributions are assumed normal with land-class-specific variances and covariances; a large number of random parameters can be unstable, so simplifications are used.
    - Reductions include assuming variance components do not vary by survey or land class (often not true) and using an AR1 structure to constrain repeated-measures covariances, reducing random parameters to a manageable number.
    - Bootstrap-based standard errors are robust to mis-specification of random-effect distributions; AR1 with bootstrap was tested as a robust approach.
  - 4.6 Model testing – Broad Habitats
    - Retrospective testing on 1984, 1990, and 1998 Broad Habitat data showed that the modelling approach produced consistent stock and change estimates, unlike the old method where stock/change discrepancies existed.
    - Comparisons demonstrated that differences between old and new methods were generally small relative to the old method’s inherent inconsistencies; the modelling approach was adopted for 2007 analysis.

- 5. Limitations and Implications
  - Bootstrapped, model-based estimation is computationally intensive; fixed-effects estimates are robust to some mis-specification of random-effects distributions, but variance/covariance parameter estimates are more sensitive.
  - AR1 with bootstrap provides robust SEs; however, fully parameterised models can be slow, so an automated AR1-based approach was preferred for large numbers of analyses.
  - Model selection/ checking is constrained by computational practicality; a standard AR1 model was chosen for consistency and automation, with cross-checks against the old method.
  - Data updates: because the new method uses data from all surveys, estimates for past surveys may be revised as new surveys are added; this is conceptually different from previous inconsistencies but is a reasonable consequence of incorporating more information.
  - Non-normality concerns (e.g., freshwater data) may limit applicability or require alternative handling; results for problematic variables may rely on older methodologies.
  - Overall, modelling is more efficient and takes full advantage of the data hierarchy, but requires careful validation and automated implementation for large-scale use.

- 6. References
  - Key references include Barr et al. (1993), Dempster, Laird, and Rubin (EM algorithm) (1977), Efron and Tibshirani (Bootstrap) (1993), Haines-Young et al. (2000), and Scott (2002) on maximum likelihood with empirical Fisher information.
  - The publication acknowledges NERC and Defra as funders and provides contact information for the Countryside Survey project office.