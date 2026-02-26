# Statistical methodology used for the Countryside Survey data

- Purpose and scope
  - Describes the statistical methodology for analysing Countryside Survey (CS) data.
  - Compares previous CS methodologies with changes implemented for CS in 2007 (CS2007).
  - Emphasises consistent estimation of stock and change, and the use of modelling approaches to utilise all available data.

- Data and sampling framework
  - Data come from a stratified sample of 1 km squares on a 15 km GB grid.
  - Two sampling levels: square level (whole square) and plot level (within squares).
  - Measurements range from binary to continuous variables.
  - Land classification (ITE) forms the basis for stratification; classifications have expanded and become country-specific (England, Wales, Scotland).

- Estimation principles
  - Old approach: stock estimates used all data from a survey; change estimates used only repeated measurements, leading to inconsistencies between stock and change.
  - New approach (CS2007): modelling to provide consistent, efficient estimates of both stock and change across all surveys.
  - Bootstrapping is used to obtain standard errors and confidence intervals due to potential non-normality, improving significance testing.

- Modelling framework and rationale
  - Consistent estimation requires complex models that handle incomplete data across multiple surveys.
  - Mixed effects and/or repeated measures models are fitted to data from all surveys.
  - Fixed effects represent land-class means across surveys; random effects capture square-level and plot-level variability and inter-survey correlations.
  - The modelling approach uses distributions and variances/covariances; variance/covariance estimates can be less robust, so bootstrap is emphasized for standard errors.

- Square-level data modelling (CS2007)
  - Data treated as complete within squares, with a repeated-measures structure.
  - Core model: y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (land-class means by survey)
    - s_ij: square random effects
    - e_ijk: repeated-measures residuals
  - Random effects assume normality with land-class-specific variances; correlations across surveys modelled (e.g., via AR1 structure).
  - AR1 reduces the number of random parameters, improving stability and feasibility for large-scale analyses.

- Plot-level data modelling
  - Plot data within squares can be modelled by extending the square-level model to include a plot-level residual, allowing correlation of plots within squares.
  - Both square-level and plot-level models can be embedded in bootstrap procedures to obtain robust SEs.

- Model specification and practical considerations
  - General formulation: y_i j k = a_i k + s_i j + e_i j k, with distributions specified for random effects.
  - A large number of random-effect parameters can cause instability; hence AR1 and common-variance assumptions are used to simplify models.
  - Fixed effects (stock/change estimates) are relatively robust to mis-specification of random effect distributions; variance/covariance estimates are more sensitive.
  - For non-normal data or complex cases, transformations are discouraged when results on the original scale are required.

- Model testing and Broad Habitats
  - Broad Habitat data (from 1984, 1990, 1998) used to test consistency of modelling against old methodologies.
  - Old approach produced discrepancies between stock and change across survey pairs; modelling yielded consistent estimates with smaller gaps.
  - Differences between old and new methods generally fell within the old method’s error bounds; modelling confirmed feasibility and consistency.
  - Findings supported adopting the new modelling approach for CS2007 and extended consistency to soil and plot-level data.

- Limitations and implications
  - Computational intensity: substantial time required for fitting models, especially across many variables.
  - AR1 model provides a balance of robustness, tractability, and performance; fully parameterised models are slower and less practical for large datasets.
  - Bootstrap SEs offer robustness against distributional mis-specification.
  - Results are updated as new surveys are added; estimates for earlier surveys may be revised slightly, reflecting new information (not a fault, but a conceptual shift from past inconsistencies).
  - Automated, standard modelling approaches are preferred for large-scale application.

- Implications for reporting and practice
  - The modelling approach utilises all available information and respects data hierarchy, leading to more precise estimates.
  - Adoption of consistent estimation changes reporting across time: estimates for a given survey can be influenced by information from all surveys.
  - There is a shift from presenting isolated adjacent-survey changes to presenting coherent histories across the full survey timeline.

- References
  - Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron & Tibshirani (Bootstrap); Scott (2002) on maximum likelihood and empirical Fisher information.

- Publication context
  - CS2007 methodology described in a Centre for Ecology and Hydrology technical report, funded by Defra and partners, with detailed methodological exposition and validation against previous approaches.