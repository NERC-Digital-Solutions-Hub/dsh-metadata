# Supporting documentation for R code to reproduce analyses of aboveground carbon stocks and associated plant diversity in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Overview
- Supplement to the article Conservation set-asides improve carbon storage and support associated plant diversity in certified sustainable oil palm plantations (Fleiss et al., 2020).
- Includes the R scripts carbon_stock_calculations.R and analyses_and_figures.R and the data veg_plot_summary.csv used to reproduce analyses and figures.
- Analyses focus on aboveground carbon stocks (AGC) and plant diversity across 49 plots in 14 fragmented forest sites (RSPO-certified oil palm plantations) and 4 continuous forest control sites in Sabah, 2017.
- Data are partly drawn from Waddell et al. (2020) and field protocols described in the document.

## Study design and data sources
- Study area: Sabah, Malaysian Borneo; 18 sites (14 fragmented set-asides within RSPO plantations; 4 continuous forest sites).
- Plot design: 49 plots across 18 sites using a nested layout:
  - Main plot: 30 m radius for trees ≥25 cm dbh and palms ≥25 cm dbh; CWD ≥25 cm diameter.
  - Subplot: 20 m radius for trees ≥10 cm and <25 cm dbh; CWD ≥10 cm and <25 cm.
  - Seedling subplot: eight 1×1 m quadrats for seedlings <2 cm dbh.
- Data collected include tree and palm dbh, height estimates, lianas, CWD, seedlings, topography, soils, and fragmentation metrics (from UAV imagery and other sources).
- Fragmentation metrics computed within multiple buffer distances (0.2–2 km) and combined via PCA to derive a fragmentation index.
- Soil parameters measured: pH, available P, total P, total N, organic C, C:N, and soil moisture.

## What the code does
- Estimates aboveground carbon stocks (AGC) for live tree biomass using pantropical allometric equations (Chave et al., 2014) with wood density from Global Wood Density Database.
- Height estimation for biomass: compares three approaches to tree height:
  - Field eye estimates (subset)
  - Climatic model (Chave et al. 2014)
  - Southeast Asia regional model (Feldpausch et al. 2012)
  - Includes a comparison against clinometer-based tangent method for accuracy.
- Biomass components:
  - Live trees ≥10 cm dbh (with height-derived AGC)
  - Palms (mixed-species model; dry mass fraction 0.37; 47.1% carbon)
  - Lianas (pantropical allometric equation)
  - Coarse woody debris (CWD) with decay classes and volume-based biomass
- Carbon content conversion: 47.1% for all biomass.
- Oil palm AGC: time-averaged AGC over a 30-year planting cycle using growth curves (mean and 95% CIs; 15 simulated points reflecting sampling uncertainty).
- Outputs also include time-averaged oil palm AGC with uncertainty.
- Calculations are performed in R (version 3.6.2) with the BIOMASS package for tree biomass and standard statistical tools.

## Data outputs and outputs of analyses
- Main data frame: plot_carbon
  - Per-plot AGC and components, with multiple height-model variants:
    - tree_carbon_20m_Mgha, tree_carbon_30m_Mgha
    - tree_carbon_chaveE_20m_Mgha, tree_carbon_chaveE_30m_Mgha
    - tree_carbon_feldpausch_20m_Mgha, tree_carbon_feldpausch_30m_Mgha
  - Densities and counts for trees and palms at 20 m and 30 m radii
  - Totals: tree_carbon_Mgha, tree_carbon_chaveE_Mgha, tree_carbon_feldpausch_Mgha
  - Liana, CWD, palm carbon stocks and their subcomponents
  - Total AGC per plot (various methods), and combined metrics like tree_palm_carbon_Mgha
  - Palm and seedling/sapling richness metrics (Fisher’s alpha and genus richness)
  - Plot-level covariates: mean DBH by class, mean wood density by class, stem densities, tooth-combed soil parameters, topography, and fragmentation measures
- Oil palm AGC outputs: mean, 95% CI, and simulated 15 data points from a Normal distribution
- Analyses and figures produced by analyses_and_figures.R include:
  - Pairwise comparisons of AGC across height-estimation methods
  - Land-use type comparisons (conservation set-asides, continuous forest, oil palm) with field-based AGC and simulated oil palm data
  - Bayesian linear mixed-effects models (LMMs) for land-use effects on AGC
  - Spatial autocorrelation assessment (Moran’s I) on model residuals
  - Pseudo-R2 for variance explained by lianas and CWD
  - Vegetation-structure comparisons (mean wood density, stem density, mean DBH) across size classes
  - Within-site variation visualizations (boxplots) of AGC
  - Drivers of variation in set-asides: fragmentation index and soil gradients (via PCA) and GAMMs with covariates (fragmentation, elevation, slope, soil PCs)
  - Relationships between AGC and plant diversity (GLMMs for genus richness and Fisher’s alpha)
  - Predictions of average AGC for plantations with varying coverage of set-asides (1–100%), and comparisons to continuous forest
- Data provenance and references are documented (Fleiss et al., 2020; Waddell et al., 2020; related biomass and soil methodology references)

## Data structure and metadata
- veg_plot_summary.csv: plot-level summary data used by analyses_and_figures.R
- Each row corresponds to a single study plot with comprehensive fields, including:
  - Site and plot codes, forest type (continuous primary, continuous logged, HCV/set-aside), coordinates, and environmental covariates
  - AGC components (live trees, palms, lianas, CWD) and total AGC
  - Crown-related and density metrics for different size classes
  - Wood density estimates by taxon and taxonomic level
  - Seedling/sapling metrics and genus richness/Fisher’s alpha
  - Fragmentation metrics (area and edge index within multiple buffers, distance to edge, years since fragmentation)
  - Soil properties (pH, TP, available P, TN, OC, C:N, moisture)
  - Topographic metrics (slope, elevation)
- Quality control notes:
  - Protocols follow established methodologies; height estimates were consistently collected by a single observer per variable; data checked for errors.
  - Four data points were excluded from analyses due to anomalously high Fisher’s alpha values.

## Data provenance, validation, and reproducibility
- Data sources include field surveys (Sabah, 2017) and published vegetation data (Waddell et al., 2020; Fleiss et al., 2020).
- Biomass estimation workflows are based on established allometric equations and wood-density databases; code uses the BIOMASS R package (Réjou-Méchain et al., 2017).
- Peer-reviewed validation:
  - The underlying analyses have been peer-reviewed and accepted for publication in Biological Conservation (Fleiss et al., 2020).
  - The R code and methodology have been carefully reviewed by the author.
- Reproducibility and access:
  - Analyses rely on R 3.6.2; outputs reproduce figures and statistics in Fleiss et al. 2020.
  - Veg plot data and documentation are available via the NERC Environmental Information Data Centre (Waddell et al., 2020).
  - Key references and data sources are cited within the document.

## Relevance to data leadership and data-system considerations
- Data availability and discoverability:
  - veg_plot_summary.csv and analyses scripts (carbon_stock_calculations.R, analyses_and_figures.R) provide a clear, replicable data pipeline.
  - Data provenance links to Waddell et al. (2020) and Fleiss et al. (2020) facilitate traceability from raw field data to published results.
- Data quality and standards:
  - Standardized nested-plot design, measurement protocols, and biomass estimation methods support comparability across sites and time.
  - Explicit documentation of height estimation methods, wood-density assignment, and carbon conversion aids consistency and auditability.
- Data gaps and granularity:
  - Fragmentation and soil gradients are integrated as predictors, but some flows (e.g., exact species-level wood densities for all stems) rely on taxonomic approximations when unidentified.
  - Oil palm AGC is modeled with time-averaged curves and uncertainty; real-time updates would require renewed growth data.
- Collaboration and stewardship:
  - The workflow links field data collection, standardized metadata, and open-access documentation to support collaboration, reuse, and extension by data teams and external researchers.
  - Data products (plots, models, predictions) enable scenario analysis for forest conservation, land-use planning, and carbon accounting initiatives.

## References to key components
- Fleiss S., Waddell E. H., et al. (2020). Conservation set-asides improve carbon storage and support associated plant diversity in certified sustainable oil palm plantations. Biological Conservation.
- Waddell E. H., Fleiss S., Bala Ola B., et al. (2020). Vegetation and habitat data for fragmented and continuous forest sites in Sabah, Malaysian Borneo, 2017. NERC EIDC.
- Foundational methodologies: Chave et al. (2014), Feldpausch et al. (2012), Pfeifer et al. (2015), Goodman et al. (2013), Schnitzer et al. (2006), Thomas & Martin (2012).