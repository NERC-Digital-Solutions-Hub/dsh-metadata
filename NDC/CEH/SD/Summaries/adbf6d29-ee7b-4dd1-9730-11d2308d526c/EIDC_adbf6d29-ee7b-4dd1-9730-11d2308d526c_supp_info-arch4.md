# Supporting documentation for R code to reproduce analyses of exotic plant invasion in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Overview
- Provides reproducible R code and data descriptors for analyses on exotic plant invasion in Sabah, Malaysian Borneo.
- Supports the article: Land-use change and propagule pressure promote plant invasions in tropical rainforest remnants (Waddell et al., 2020a).
- Focuses on how fragmentation, disturbance, propagule pressure, soil characteristics, and native community composition influence invasion, using partial least squares path modelling (PLS-PM).

## What the code does
- Uses the plot-level data (Plot_measured_data.csv) to run PLSPM analyses with the plspm package.
- Assesses relative influence of fragmentation, disturbance, propagule pressure, soil traits, and native community on exotic invasions in forest remnants and continuous forest.
- Evaluates bidirectional relationships between native community and invasion.
- Runs 10 models: one full dataset model (Native community → Invasion) plus nine models for native components (adult trees, saplings, seedlings, ground vegetation) in both directions.

## Data and study design
- Data: plot-level measurements from 47 plots across 17 sites ( Sabah, Malaysian Borneo) sampled in 2017.
- Landscape: 13 fragmented forest sites within RSPO-certified oil palm plantations and 4 continuous forest sites; gradient of fragmentation and disturbance.
- Plot design: nested circular plots (0.28 ha) with measurements for large trees, smaller trees, saplings, seedlings, and ground vegetation.
- Invasion metrics: exotic richness and exotic abundance recorded along two 100 m transects outside forest remnants.
- Native community metrics: alpha diversity (observed genus richness) and Faith’s phylogenetic diversity (PD), computed for total native community and separately for adults, saplings, seedlings, and ground vegetation.

## Modelling approach
- Structural equation modelling via partial least squares (PLS-PM) with the plspm R package.
- Inner model defines connections among latent variables (e.g., Fragmentation, Disturbance, Soil, Natives, Propagule, Exotics); measured variables map to latent variables per Table 1.
- Data preprocessing: centering and scaling (mean 0, variance 1); transformations to improve normality; variable renaming to create a compact data_pls dataframe.

## Variables and data processing
- Latent and measured variables include:
  - Fragmentation: Area of non-forest, Edge density, Age since fragmentation.
  - Disturbance: Number of large Dipterocarpaceae stems, Wood density.
  - Soil characteristics: Soil pH, Available phosphorus (P).
  - Native community: Native richness, Native abundance, Native phylogenetic diversity (PD) by total and by component (adult trees, saplings, seedlings, ground vegetation).
  - Propagule pressure: Exotic richness outside the remnant, Exotic abundance outside.
  - Exotics (invasion): Exotic richness, Exotic abundance per plot.
- Data preparation steps:
  - Created data_pls dataframe with Site, Plot and all measured variables (including Edge.density calculated from 2 km buffer).
  - Specified inner and outer model matrices (pathway) and defined which observed variables load onto which latent variables.
  - Addressed bidirectionality by testing Native → Invasion and Invasion → Native across models.

## Outputs and assessment
- Model outputs: standardized path coefficients with bootstrap-derived two-sided P-values (10,000 bootstraps; site-level resampling to account for site effects).
- Measurement model evaluation: convergent validity (AVE > 0.50), reliability (loadings > 0.70; with few exceptions), internal consistency (Cronbach’s alpha and Dillon-Goldstein’s rho > 0.70), discriminant validity via cross-loadings and Fornell-Larcker criteria.
- Structural model evaluation: R2 for endogenous latent variables, GoF index (no fixed threshold; interpreted as higher is better).
- Model refinement: start from full specification and remove non-significant terms (P < 0.05) in a stepwise fashion.
- Visualization: simple plot of final path model with standardized coefficients (plot(pls2)); figures re-created for publication.

## Data structure and quality control
- Data structure: one row per plot with fields including Site_code, Site_plot_code, Forest_type, coordinates, fragmentation metrics, soil metrics, exotic metrics, and native community metrics by component.
- Quality control: standardized collection protocol, same observers for field surveys, thorough data checks; analyses and code peer-reviewed and accepted in Landscape Ecology (Waddell et al., 2020a).

## Reproducibility and references
- Complete methodological details, data description, and analysis steps provided for replication.
- Data and scripts are linked to associated publications (Waddell et al. 2020a, 2020b) and are grounded in established SEM and PLSPM practices (Sanchez 2013; Chin 1998; Fornell & Larcker 1981).
- Key software/tools: R, plspm, phylogenetic tools (Phylomatic, APGIII supertree), phylogenetic diversity (picante).