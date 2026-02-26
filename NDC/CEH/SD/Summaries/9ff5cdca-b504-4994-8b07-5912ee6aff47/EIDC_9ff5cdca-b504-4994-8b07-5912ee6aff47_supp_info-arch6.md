# Supporting documentation for R code to reproduce analyses of aboveground carbon stocks and associated plant diversity in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Overview
- Provides supporting information for reproducing analyses in Fleiss et al. 2020 using R scripts carbon_stock_calculations.R and analyses_and_figures.R and the data veg_plot_summary.csv.
- Data and code draw on vegetation measurements from 49 plots across 14 fragmented forest sites within RSPO-certified oil palm plantations and 4 continuous forest control sites in Sabah, Malaysian Borneo (2017).
- Aims to estimate aboveground carbon stocks (AGC) and associated plant diversity, compare land-use types, and examine drivers (fragmentation, topography, soils) that influence AGC.

## Data and data structure
- veg_plot_summary.csv: plot-level summary data used to run analyses in analyses_and_figures.R.
- Study design and data scope:
  - Nested plot design in 49 plots across 18 sites (14 fragmented set-asides, 4 continuous forest).
  - Measurements include trees and palms by size class, lianas, coarse woody debris (CWD), seedlings, soil parameters, topography, and fragmentation context.
- Key fields (examples):
  - Site_plot_code, Site_code, Forest_type, Latitude, Longitude, Elevation_masl, Slope_deg, Soil_pH, Soil_TP_ppm, Soil_AvP_ppm, Soil_TN_perc, Soil_OC_perc, Soi_CtoN_orgC, Soil_moisture_perc, Fisher_alpha and Richness metrics by life stage.
  - AGC components: tree_carbon_Mgha, tree_carbon_chaveE_Mgha, tree_carbon_feldpausch_Mgha, liana_carbon_Mgha, CWD_carbon_Mgha, palm_carbon_Mgha, total_carbon_Mgha.
  - Distinct AGC for palms and trees combined (tree_palm_carbon_Mgha, tree_palm_carbon_chaveE_Mgha, tree_palm_carbon_feldpausch_Mgha).
  - Density metrics: Stem_nha_seedling, Stem_nha_sapling, Stem_nha_smalltree, Stem_nha_medlargetree; palm counts; mean DBH by size class; mean wood density by life-form.
  - Fragmentation and landscape context: ForArea_buffer_Xm_m2 and ForEdge_buffer_Xm_index (buffers 200–2000 m), Nearest_edge_m, Years_since_frag, Principal Component analyses (fragmentation PC1), and associated scatterplots.
  - Vegetation structure and diversity: Richness and Fisher's alpha by life stage; four size classes.
- Data quality: standardized collection protocols, single observer for height estimates to minimize variation, quality checks; note that four outliers were excluded in published analyses.

## Methods and analyses (What the code does)
- Biomass and carbon stock estimation:
  - Live trees (≥10 cm dbh): pantropical allometric equation (Chave et al. 2014) via the BIOMASS R package; wood density from Global Wood Density Database; height estimated by three methods (field eye estimates; climatic model Chave et al. 2014; Feldpausch et al. 2012 regional model); accuracy checked against clinometer-based measurements (tangent method).
  - Palms: mixed-species biomass model using diameter, height, and dry mass fraction (0.37) with carbon content 47.1%.
  - Lianas: pantropical allometric equation based on dbh.
  - Coarse woody debris (CWD): biomass from volume x density; volume via frustum of a cone; decay-class-based densities.
  - Oil palm AGC: time-averaged AGC over 0–30 years using mean value theorem from growth curves (Carlson et al. 2012, 2013).
  - Conversion to carbon: 47.1% carbon content for all biomass components.
- Outputs produced by the code:
  - plot_carbon dataframe with 49 plots and numerous AGC metrics (by method and by component: trees, palms, lianas, CWD, oil palm), including total AGC and detailed per-radius measures (20 m and 30 m plots).
  - Time-averaged oil palm AGC with mean, 95% CIs, and 15 simulated datapoints drawn from a Normal distribution representing potential samples.
- Analytical workflow in analyses_and_figures.R:
  - Reproduce published results comparing AGC across land-use types (set-asides, continuous forest, oil palm) using three tree-height estimation methods.
  - Bayesian linear mixed-effects models (LMMs) to test land-use effects on AGC (live trees, palms, and total) across height-estimation methods; Moran’s I to assess spatial autocorrelation.
  - Variation partitioning using Moran’s I-based pseudo-R² for liana and CWD contributions to total AGC.
  - Vegetation structure comparisons (mean wood density, stem density, mean DBH) across forest types for seedlings, saplings, small trees, and medium-large trees, using Bayesian LMMs.
  - Fragmentation and soil drivers: PCA to reduce fragmentation metrics (buffer-based forest area and edge index) and soil parameters (pH, P forms, N, C, C:N, moisture); GAMMs to assess predictors (fragmentation index, soil PCs, elevation, slope) on AGC.
  - Diversity-AGC relationships: Bayesian GLMMs linking live-tree/palm AGC to genus richness and Fisher’s alpha across life stages.
  - Predictive analyses: average AGC of oil palm plantations under varying set-aside coverage (1–100%) vs. continuous forest, for comparison.
- Validation and reproducibility:
  - Analyses peer-reviewed and published (Biological Conservation, Fleiss et al. 2020).
  - Code checked for errors by the author; biomass workflow builds on established R package workflows (e.g., biomass package).

## Outputs and data products (for reuse)
- Reproducible figures and statistics from Fleiss et al. 2020:
  - Correlations between height-estimation methods for AGC.
  - Land-use type comparisons of AGC (live trees, palms, total; with and without CWD/lianas contributions).
  - Vegetation-structure comparisons across life stages.
  - Drivers of variation in AGC (fragmentation, soils, elevation, slope) via PCA and GAMMs.
  - Relationships between AGC and plant diversity (genus richness, Fisher’s alpha).
  - Predictive plots of average AGC under different plantation set-aside scenarios.
- Data products enable exploration of how fragmentation and management practices in oil palm landscapes influence carbon storage and biodiversity.

## Study context and data collection (brief)
- Field surveys conducted July–November 2017 in Sabah, Malaysian Borneo.
- Sites: 14 fragmented set-asides in RSPO-certified oil palm plantations and 4 continuous forest controls.
- Plot design: 30 m radius main plots with nested subplots (20 m and 5 m) for trees, palms, CWD; eight 1x1 m quadrats for seedlings.
- Variables collected include: tree and palm dbh, height estimates, liana dbh entering tree crowns, CWD dimensions and decay classes, soil chemistry (pH, P, N, C, moisture), topography, and landscape fragmentation metrics.
- Fragmentation context quantified using UAV-derived landscape data within 0.2–2 km buffers around plots; edge indices and distances to edge, plus time since fragmentation.

## Reuse and integration notes
- Primary data source for analyses is veg_plot_summary.csv; compatible with analyses_and_figures.R to reproduce published figures.
- For broader use, data linkages to Waddell et al. 2020 vegetation data can be incorporated to expand analyses beyond Sabah or to compare with additional datasets.
- The outlined methods offer a template for estimating AGC across multiple taxa and for conducting land-use, fragmentation, and biodiversity–carbon relationships in tropical forest settings.

## References (contextual)
- Core methodological references include Chave et al. (2014), Feldpausch et al. (2012), Réjou-Méchain et al. (2017), Goodman et al. (2013), Schnitzer et al. (2006), Pfeifer et al. (2015), Carlson et al. (2012, 2013), and the primary study Fleiss et al. (2020).