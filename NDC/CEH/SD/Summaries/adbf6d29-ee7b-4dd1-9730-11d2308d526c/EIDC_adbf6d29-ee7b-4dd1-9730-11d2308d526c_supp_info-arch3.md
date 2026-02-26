# Supporting documentation for R code to reproduce analyses of exotic plant invasion in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Overview and aim
- Provides supporting information for reproducing analyses from Waddell et al. (2020a) on how fragmentation, disturbance, propagule pressure, soil characteristics, and native plant community composition influence exotic plant invasions.
- Focuses on how plot- and site-level data were processed and modeled to assess relative influences and potential bi-directional relationships between native communities and invasion.

## Study design and data
- Study area and sampling:
  - 47 plots across 17 sites in Sabah, Malaysian Borneo.
  - Comparison between forest remnants within oil-palm landscapes (13 sites) and continuous, extensive forest (4 sites).
  - Nested plot design sampling across four native plant size classes: adult trees, saplings, seedlings, and ground vegetation.
- Data sources:
  - Plot_measured_data.csv (plot-level measurements).
  - Exports and analyses conducted with PLSPM_invasion.R.
  - Full vegetation data availability via Waddell et al. (2020b).
- Variables measured:
  - Fragmentation: area of non-forest in a 2 km buffer; area of forest in 2 km buffer; edge density; fragmentation age.
  - Disturbance: number of large Dipterocarpaceae stems; average wood density for trees >10 cm DBH.
  - Soil: soil pH; available phosphorus (P).
  - Propagule pressure: exotic species richness and abundance along two 100 m transects outside remnant and in the oil-palm matrix.
  - Native community (subsets and total): richness and phylogenetic diversity (Faith's PD) for total natives and for adult trees, saplings, seedlings, and ground vegetation.
  - Exotic invasion: richness and abundance of exotic genera/stems.
- Data structure:
  - Detailed per-plot attributes including Site_code, Forest_type, geographic coordinates, environmental variables, and per-size-class native metrics.

## Modelling approach and variables
- Modelling framework:
  - Partial Least Squares Path Modelling (PLS-PM) using the plspm R package.
  - Latent variable blocks and corresponding measured indicators defined (e.g., Fragmentation, Disturbance, Soil, Natives, Propagule, Exotics).
  - Both directions tested for the native community -> invasion relationship due to unknown causality.
- Data preparation for modelling:
  - All measured variables centred and scaled (mean 0, variance 1).
  - Variables renamed for brevity (e.g., Fragmentation.age → Age; Edge.in.2km.buffer → Edge.density); created new variable Edge.density = Edge.in.2km.buffer / Area.in.2km.buffer.
  - Data frames created to assemble variables for modelling (data_pls).
- Model specification:
  - Inner model (connections between latent variables) specified as a lower-triangular matrix, with latent relationships guided by Fig. 1 in the article.
  - Two modelling strategies:
    - Full dataset with Native total -> Invasion.
    - Separate PLSPMs for native adult trees, saplings, seedlings, and ground vegetation to test which native subset most strongly relates to invasion.
  - Stepwise simplification: iteratively remove non-significant paths (P < 0.05) starting from the full specification.
- Assessment and validation criteria:
  - Measurement model reliability and validity:
    - Convergent validity: average variance extracted (AVE) > 0.50.
    - Indicator reliability: standardised loadings > 0.70 (with some exceptions).
    - Internal consistency: Cronbach’s alpha and composite reliability (Dillon-Goldstein’s rho) > 0.70.
    - Discriminant validity: cross-loadings assessed; Fornell-Larcker criterion (square root of AVE exceeds correlations with other latent variables).
  - Structural model assessment:
    - R-squared (R2) values for endogenous latent variables (thresholds: weak < 0.30, moderate 0.30–0.60, substantial > 0.60, with some sources using 0.20/0.50 as alternate cutoffs).
    - Goodness of Fit (GoF) index (higher values are better; no fixed threshold, used for comparative assessment).
  - Significance testing:
    - Two-sided P-values for standardised path coefficients estimated via 10,000 bootstrap iterations.
    - Site effects handled by bootstrapping samples at the site level (since site identity cannot be included as a random effect in PLSPM).
- Outputs:
  - Final path diagram (positive/negative relationships with standardised path coefficients) generated with plot(pls2); figures re-made for publication.
  - Summary outputs (summary(pls2)) including model fit and path significance.
  - Documentation of model specification and variable removal order (for reproducibility).

## Reproducibility, validation, and governance
- Code validation:
  - Analyses peer-reviewed and accepted for publication (Landscape Ecology; Waddell et al., 2020a).
  - Authors conducted careful checks for coding errors.
- Reproducibility notes:
  - The supporting document details steps to reproduce analyses from the provided CSV and R script.
  - Data and code are designed to be transparent and auditable, with explicit data preparation steps, model specifications, and validation criteria.
- Data governance considerations:
  - The dataset integrates site- and plot-level measurements across fragmented and continuous forest contexts, requiring careful handling of metadata, transformations, and variable naming for consistency.
  - Data are linked to broader vegetation datasets (Waddell et al., 2020b) and related publications, emphasizing openness and traceability.

## Practical implications for monitoring frameworks
- Demonstrates an integrated, model-based approach to monitoring environmental health in fragmented landscapes:
  - Combines landscape-scale fragmentation metrics with plot-scale biotic and edaphic factors to explain exotic invasions.
  - Assesses both drivers (fragmentation, disturbance, propagule pressure, soil) and biotic resistance (native community structure) within a single framework.
  - Evaluates potential bidirectional relationships between native community diversity and invasion to inform management priorities.
- Advantages for policymakers and practitioners:
  - A clear data workflow from collection to analysis and interpretation, including data transformations and quality checks.
  - Transparent reporting of model validity, reliability, and robustness via established PLS-PM criteria and bootstrapped inference.
  - Explicit data structure and metadata requirements to support future monitoring iterations and cross-site comparisons.
- Barriers and considerations:
  - Data sharing and metadata completeness are essential for reuse; some variables require careful standardization and documentation.
  - Site-level random effects are not native to PLSPM; bootstrap-based site resampling provides a workaround but may limit certain random-effects interpretations.
  - The approach relies on comprehensive, nested plot data across diverse forest contexts, which can be resource-intensive to collect and maintain.