# Statistical Methodology Used for the Analysis of Countryside Survey Data

- Purpose: Describe the statistical methods used to analyze Countryside Survey (CS) data, summarise previous methodologies, and detail the changes implemented for CS in 2007.

- Key problem with previous methods: Stock estimates used all data from a survey, while change estimates used only repeated measurements across survey pairs, causing inconsistencies between stock and change estimates.

- Main finding and solution: Modelling (consistent estimation) is feasible, robust, and yields more precise estimates by using all available information and producing consistent stock and change estimates. These methods were adopted for CS 2007.

- Trade-offs and cautions: Modelling requires distributional assumptions; results are validated against previous methods, especially for small subsets. Bootstrap is used to obtain robust standard errors and significance in the presence of non-normal data.

- Data structure and sampling: CS uses a two-level hierarchical design across GB:
  - 1 km squares selected within a 15 km grid, classified into Land Classes.
  - Within squares, multiple plots/measurements (binary to continuous variables) describing vegetation, soils, etc.
  - Separate country-specific Land Class classifications (England, Wales, Scotland in CS2007).

- Estimation approaches:
  - Previous approach: means and standard errors by Land Class, then weighted combination by land area to obtain regional estimates.
  - New approach: modelling stock and change jointly via mixed-effects/repeated-measures models, providing consistent and more efficient estimates.

- Modelling framework (square and plot level data):
  - Square level: repeated-measures mixed model with fixed effects for land-class means across surveys and random effects for squares; within-square measurements are correlated across surveys.
  - Plot level: additional plot-level random effects can be included; bootstrapping extended to account for plot-level data.

- Model specification and simplification:
  - General model: y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land-class means by survey), square random effects s_ij, and repeated-measures residuals e_ijk.
  - Random effects: assumed normal with land-class-specific variances; correlations across surveys modelled.
  - To keep models tractable, random-effect parameters are constrained (e.g., AR1 structure: same variance across surveys, constant within land classes; first-order autocorrelation for covariances).
  - AR1 plus bootstrap (AR1-b): reduces parameter count while maintaining robust fixed-effect estimates.

- Model testing and Broad Habitats:
  - Applied modelling to Broad Habitat data across 1984, 1990, 1998 to assess consistency.
  - Modelling eliminated stock/change discrepancies observed with old methods; changes in estimates between old and new methods generally fell within old inconsistencies.

- Practical considerations and limitations:
  - Computational intensity: full models are slow; AR1 with bootstrap offers a practical balance for large numbers of variables.
  - Robustness: fixed-effect estimates are relatively robust to distributional mis-specification; variance/covariance parameters are more sensitive.
  - Data updates: incorporating data from all surveys means previous survey estimates can be updated when new data are added; reporting on a single occasion may not be strictly consistent with future data, but updates are small.
  - Non-normal data issues: very non-normal distributions (e.g., standing water) can lead to convergence to local maxima; in such cases old methodology results may be retained.

- Implications for practice:
  - More precise estimates by utilizing all available information and properly modelling data hierarchy.
  - Improved analytical consistency across surveys, albeit with potential updates to past results as new data are gathered.
  - Automated application of a standard modelling approach across many variables, supported by bootstrapping for reliable uncertainty measures.

- References:
  - Barr et al. (1993); Dempster, Laird, Rubin (1977); Efron, Tibshirani (1993); Haines-Young et al. (2000); Scott (2002).