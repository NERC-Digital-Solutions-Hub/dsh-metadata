# Countryside Survey 2007: Statistical Methodology

- Purpose: Describe the statistical methods used to analyse Countryside Survey (CS) data, summarise previous approaches, and detail the changes implemented for CS in 2007 to improve consistency between stock and change estimates.

- Background and motivation:
  - Previous methods estimated stock using all data from a survey but estimated change from repeated measurements across survey pairs, leading to inconsistencies between stock and change.
  - Investigations with Broad Habitat data showed that consistent estimation via modelling was feasible and robust, with new methods generally agreeing with old methods within existing inconsistencies.
  - The shift to modelling-based, consistent estimation for 2007 aimed to produce more precise estimates by using all available information and correctly reflecting the data hierarchy.

- Key outcomes of the modelling approach:
  - Implementation of consistent stock and change estimates across survey intervals.
  - Use of models that integrate data from all surveys, with the expectation that newer surveys update past estimates (small changes expected).
  - Although modelling introduces additional distributional assumptions, results were checked against the old methodology to ensure plausibility.

- Data structure and sampling:
  - Data come from a stratified sample of 1 km squares within a 15 km grid across Great Britain.
  - Each square is mapped and measured at two levels: square level (whole square) and plot level (within-square plots).
  - Land Classification (ITE) defines strata; the classification expanded from 32 to 45 classes to accommodate country reporting needs (England, Wales, Scotland).

- Estimation approach:
  - Old method: stock estimates used all data from a survey; change estimates used repeated measurements, causing potential misalignment.
  - New method: modelling-based, consistent estimation of both stock and change using data from all surveys; aims to be more efficient and robust.
  - For region-wide estimates, means and standard errors by Land Class are calculated and then area-weighted to produce national/regional figures.
  - Bootstrap is used to obtain standard errors and confidence intervals, particularly for square-level data, to accommodate non-normal data distributions.

- Modelling framework (square-level and plot-level data):
  - Square-level data: treated as a repeated-measures problem; implemented via mixed effects models with fixed effects for land-class means across surveys and random effects capturing square-level variation and within-square repeat measurements.
  - Plot-level data: recognition of hierarchical structure within squares; previous analyses either aggregated to square level or treated plots as independent. In CS2000, mixed models incorporating square-level variation and plot-level residuals were used; bootstrapping extended to plot-level data.
  - General modelling equation for square-level data:
    - y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (land-class means for survey k)
    - s_ij: square random effect
    - e_ijk: repeated-measures residual
  - Random effects structure:
    - Variances and covariances may vary by land class; modelling employs distributions for random and repeated effects.
    - The full model with all random effects can be unstable with many surveys; a simplified AR1 (autoregressive order 1) approach is used to reduce parameters and stabilize estimation.

- AR1 modelling and bootstrapping:
  - AR1 reductions: assume common random-effect variance across surveys (σ_i) and first-order autocorrelation for repeated measures; results in three random-effect parameters per land class regardless of survey count.
  - Bootstrap: used to obtain robust standard errors, especially since variance/covariance parameters are less precisely estimated; fixed-effect estimates are more stable, while bootstrap accommodates potential distributional misspecifications.

- Model testing and Broad Habitats:
  - Application to seven Broad Habitats across 1984, 1990, and 1998 surveys showed that modelling produced consistent stock and change estimates, resolving previous discrepancies where stock-derived changes did not align with repeat-squares changes.
  - Comparisons indicated that new estimates generally remained within the old-method error bounds, with some differences but not deemed statistically significant beyond existing inconsistency.

- Limitations and practical implications:
  - Computational intensity: full parameterised models are slow; AR1 model with bootstrap provides a practical balance for large variable sets.
  - Robustness: fixed effects are relatively robust to distributional mis-specification; variance/covariance estimates are more sensitive.
  - Data updating: because analyses fuse data from all surveys, estimates for earlier surveys can be revised as new data are added; this reflects improved information rather than errors.
  - Non-normal data considerations: some variables with highly non-normal distributions (e.g., standing water) may challenge the new method; in such cases, older methods may be retained for those variables to avoid convergence to local maxima.
  - General benefit: the modelling approach better utilises all information and the hierarchical structure, leading to more precise estimates.

- Implications for monitoring and data governance:
  - Adopting consistent estimation enhances the reliability of trend assessments over time, which is valuable for policy scrutiny and decision-making.
  - Results are produced in a way that can be automated for a large number of variables, supporting scalable monitoring frameworks.
  - While the approach improves precision, it also necessitates careful interpretation of updated past estimates as new data become available, highlighting the need for transparent documentation of methodologies and data provenance.

- References and further reading:
  - Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron and Tibshirani (1993), Scott (2002), among others, informing the methodological foundation (mixed models, EM algorithms, bootstrap, and covariance structures).