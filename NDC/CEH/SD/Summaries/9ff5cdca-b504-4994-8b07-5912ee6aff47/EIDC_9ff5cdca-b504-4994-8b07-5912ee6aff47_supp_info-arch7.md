# Supporting documentation for R code to reproduce analyses of aboveground carbon stocks and associated plant diversity in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

- Purpose: Provide supporting information to reproduce analyses of aboveground carbon stocks (AGC) and plant diversity from 49 plots across 18 sites in Sabah, comparing conservation set-asides within RSPO-certified oil palm plantations to continuous forest controls.
- Related materials: Files carbon_stock_calculations.R, veg_plot_summary.csv, and analyses_and_figures.R used in Fleiss et al. 2020.

## Study design and data inputs

- Study area and sites: Sabah, Malaysian Borneo; 14 fragmented forest sites within RSPO-certified oil palm plantations and 4 continuous forest sites for comparison; fieldwork conducted in 2017.
- Plot design: 49 plots total across 18 sites, with a nested design inside each 30 m-radius main plot:
  - 30 m radius main plot: live trees and palms ≥25 cm dbh; coarse woody debris (CWD) ≥25 cm.
  - 20 m radius subplot: live trees and palms ≥10 cm and <25 cm dbh; CWD ≥10 cm and <25 cm.
  - 5 m radius subplot: saplings and smaller trees (2–10 cm dbh).
  - Seedlings: eight 1×1 m quadrats per plot.
- Data sources and protocols: Field data collected following established protocols; veg_plot_summary.csv summarizes plot-level data; full vegetation data available from Waddell et al. (2020).
- Biophysical and landscape context: UAV-derived land cover data within buffers (0.2–2 km) used to derive fragmentation metrics; soil parameters measured per plot (pH, available P, total P, total N, organic C, C:N, soil moisture); topography and elevation recorded.

## Spatial fragmentation and GIS-relevant measures

- Fragmentation metrics: within multiple buffers (0.2 to 2 km) around each plot:
  - Forest area and edge index (number of boundary cells dividing forest and oil palm) within the buffer.
  - Straight-line distance to nearest forest–oil palm edge.
  - Years since fragmentation (time since adjacent oil palm establishment).
- Data integration: fragmentation indicators are used as predictors in analyses (and combined via PCA to form fragmentation indices).

## Biomass and carbon estimation methods

- Trees (≥10 cm dbh): biomass estimated with pantropical allometric equation (Chave et al. 2014) using dbh, height, and wood density (from Global Wood Density Database).
- Height estimation for trees:
  - Field heights estimated by eye for a subset; three alternative height models to compare:
    - Second-order log-log relationship (field-derived heights).
    - Climatic model (Chave et al. 2014) incorporating environmental stress.
    - Southeast Asia regional model (Feldpausch et al. 2012) based on dbh.
  - Eye-estimated heights validated against clinometer measurements (tangent method) for a subset.
- Palms: biomass estimated using a mixed-species model based on dry mass fraction (0.37), diameter, and stem height; carbon content fixed at 47.1%.
- Lianas: biomass estimated using pantropical allometric equation based on dbh.
- Coarse Woody Debris (CWD): biomass estimated from volume (frustrum of a cone) and wood density; decay-class–based densities applied.
- Carbon content: biomass-to-carbon conversion fixed at 47.1% across all biomass components.
- Oil palm carbon: time-averaged AGC for oil palm over 0–30 years modeled using oil palm growth curves; simulations produce mean and 95% CIs and a set of 15 simulated datapoints per plot.

## Outputs (data and analysis results)

- plot_carbon data frame (per plot, N=49) including:
  - Site_plot_code, Site_code, Forest_type (Continuous primary, Continuous logged, HCV/set-aside), coordinates, and numerous AGC fields:
    - Tree and palm AGC by height method (20 m and 30 m radii), e.g., tree_carbon_20m_Mgha, tree_carbon_30m_Mgha, tree_carbon_chaveE_20m_Mgha, tree_carbon_chaveE_30m_Mgha, tree_carbon_feldpausch_20m_Mgha, tree_carbon_feldpausch_30m_Mgha, etc.
    - Totals: total_carbon_Mgha (live trees, palms, CWD, lianas) and tree_palm_carbon_Mgha, tree_palm_carbon_*_Mgha variants.
    - Liana, CWD, and palm components (Mgha-1), seedling/sapling/small-tree metrics, DBH means by size class, wood densities, and stem densities (nha).
    - Plot-level biodiversity metrics: genus richness and Fisher's alpha for seedlings, saplings, and trees.
    - Topographic and soil variables: slope, elevation, soil pH, TP, AvP, TN, OC, C:N, soil moisture.
  - Fragmentation and landscape metrics: buffers’ forest area (various m radii), edge indices, nearest edge distance, years since fragmentation, and other landscape descriptors.
- Oil palm AGC outputs: mean, 95% CIs, and 15 simulated points representing time-averaged oil palm AGC (0–30 years).
- Analytical outputs:
  - Pairwise comparisons of AGC across height-estimation methods and land-use types.
  - Bayesian linear mixed-effects models (LMMs) for land-use effects on live tree/palm AGC and total AGC.
  - Moran’s I for spatial autocorrelation in model residuals.
  - Variance explained (pseudo-R2) for liana and CWD contributions.
  - Vegetation structure comparisons (mean wood density, stem density, mean DBH) by forest type across four size classes.
  - Fragmentation and soil parameter explorations via PCA and GAMMs to identify drivers of AGC.
  - GLMMs relating AGC to plant diversity metrics (genus richness, Fisher’s alpha) by size class.
  - Predictive plots of average oil palm plantation AGC with varying set-aside cover and continuous forest baselines.

## Analysis workflow and reproducibility

- Software: R version 3.6.2.
- Primary scripts: carbon_stock_calculations.R (biomass and AGC calculations), analyses_and_figures.R (uses veg_plot_summary.csv to reproduce figures and statistics in Fleiss et al. 2020).
- Data processing and modelling approaches:
  - Biomass-to-carbon conversions, variable-specific allometric models, and height-estimation model comparisons.
  - Landscape fragmentation quantified with PCA on multiple fragmentation indicators; soil gradients summarized with PCA on seven soil parameters.
  - Statistical models: Bayesian LMMs, GLMMs, and GAMMs; Moran’s I for spatial checks; and PCA for dimension reduction.
- Validation and quality control:
  - Calculations peer-reviewed and accepted for Biological Conservation (Fleiss et al. 2020).
  - Field measurements largely performed by a single observer for consistency; outliers and data quality checked; four data points removed due to extreme Fisher’s alpha values.

## Context and availability

- Study context: Evaluation of conservation set-asides within oil palm landscapes to assess aboveground carbon stocks and associated plant diversity.
- Locations and timing: 2017 field surveys in Sabah; comparison between fragmentation within RSPO-certified plantations and continuous primary/logged forest.
- Data provenance: veg_plot_summary.csv (plot-level data) and Waddell et al. (2020) vegetation data; full methodological details and study results provided in Fleiss et al. (2020) with supporting data and code.