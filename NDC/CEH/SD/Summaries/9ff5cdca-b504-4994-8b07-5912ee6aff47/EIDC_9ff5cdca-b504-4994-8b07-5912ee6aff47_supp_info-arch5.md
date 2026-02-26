# Supporting documentation for R code to reproduce analyses of aboveground carbon stocks and associated plant diversity in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Overview
- Provides the accompanying data and R scripts to reproduce analyses from Fleiss et al. (2020) on aboveground carbon stocks (AGC) and plant diversity.
- Study design: 49 plots across 18 sites in Sabah, Malaysia Borneo (2017) including 14 fragmentation-set-asides within RSPO-certified oil palm plantations and 4 continuous forest sites.
- Data and scripts link to the article’s analyses and figures, including data provenance from Waddell et al. (2020) and field protocols for vegetation and soil measurements.
- Goals include comparing AGC between conservation set-asides and continuous forest, assessing drivers of AGC (fragmentation, topography, soils), relationships between AGC and biodiversity, and predicting AGC under varying plantation set-aside coverage.

## Data assets and structure
- veg_plot_summary.csv: plot-level summary data used for analyses; includes site/plot codes, land-use type, geographic coordinates, biomass and carbon estimates (trees, palms, lianas, coarse woody debris), and biodiversity metrics (genus richness, Fisher’s alpha) by size class.
- plot_carbon dataframe (described outputs): per-plot AGC components and totals for living trees, palms, lianas, CWD, and their combinations under three height-estimation methods.
- Key data columns (selected):
  - Site_plot_code, Site_code, Forest_type, Latitude, Longitude, Elevation_masl, Slope_deg, Soil parameters (pH, Available P, Total P, Total N, Organic C, C:N, Moisture), DBH-based biomass metrics, tree/palm/liana C/ha totals, CWD C/ha, seedling/sapling/tree richness and Fisher’s alpha.
  - AGC estimates calculated with three height-models: field heights, Chave et al. climatic model, and Feldpausch et al. Southeast Asia regional model.
  - Outputs include total plot AGC (live trees, palms, CWD, lianas) and oil palm AGC time-averaged (0–30 years) with mean and 95% CIs.

## Provenance, study design, and data cataloging
- Field data collection ( Sabah, 2017 ):
  - Nested plot design in each 30 m radius main plot: 20 m radius subplot for 10–25 cm dbh trees/palms and 25–30 cm CWD; 5 m radius subplot for 2–10 cm dbh; seedling quadrats (8x1 m) for <2 cm dbh.
  - Measurements of dbh for trees and palms, tree height by eye (with a subset validated by clinometer), liana dbh, CWD dimensions and decay classes, soil sampling (0–20 cm) for seven soil parameters.
  - Species identification for trees; palms not identified to species; liana biomass modeled; biospecimen vouchers prepared.
  - Fragmentation context quantified using UAV-derived land-cover around plots (0.2–2 km buffers), including forest area, edge index, distance to nearest edge, and time since fragmentation.
- Data lineage and sources:
  - Core data linked to Waddell et al. (2020) vegetation dataset.
  - Contextual background and comparisons drawn from Fleiss et al. (2020) Biological Conservation.

## Data processing, methods, and workflow
- Software and reproducibility:
  - Calculations and analyses performed in R v3.6.2.
  - Analyses scripts: carbon_stock_calculations.R and analyses_and_figures.R, using veg_plot_summary.csv as input.
- Biomass and carbon estimation approaches:
  - Live trees (≥10 cm dbh): pantropical allometric biomass model (Chave et al., 2014) via BIOMASS R package; wood densities assigned from Global Wood Density Database (by species/genus/family where possible).
  - Height estimation: three approaches for comparison:
    - Field heights estimated by eye (subset).
    - Chave et al. climatic model (dbh + environmental stress).
    - Feldpausch et al. regional Southeast Asia model (dbh-driven).
  - Palms biomass: mixed-species model using diameter, height, and dry mass fraction (0.37).
  - Lianas biomass: pantropical allometric model (dbh-based).
  - Coarse woody debris (CWD): volume estimation (frustum of a cone) and wood density by decay class; biomass = volume × density.
  - Carbon content: fixed at 47.1% for all biomass components.
  - Oil palm AGC: time-averaged AGC over 0–30 years using oil palm growth curves (mean and 95% CIs; simulated data points from Normal distribution for uncertainty).
- Outputs and data products:
  - plot_carbon: per-plot AGC values for various components and model combinations (e.g., tree_carbon_Mgha, tree_carbon_chaveE_Mgha, palm_carbon_Mgha, CWD_carbon_Mgha, liana_carbon_Mgha, total_carbon_Mgha, etc.).
  - Additional derived metrics: palm and tree densities, mean DBH by class, wood-density metrics, seedling/sapling/tree genus richness and Fisher’s alpha.
- Analytical outputs:
  - Correlations and scatterplots comparing AGC across height-estimation methods.
  - Land-use type comparisons via Bayesian linear mixed-effects models (LMMs) for AGC by land-use type and height-method.
  - Spatial autocorrelation assessment (Moran’s I) on LMM residuals.
  - Variation analysis through PCA (fragmentation metrics and soil parameters) and GAMMs to identify drivers (fragmentation index, soil gradients, elevation, slope).
  - Biodiversity-AGC relationships via Bayesian GLMMs linking AGC to genus richness and Fisher’s alpha across size classes.
  - Predictive scenarios for average oil palm plantation AGC across varying set-aside coverage (1–100%) and continuous forest comparisons.
- Validation and quality checks:
  - Peer-reviewed study (Fleiss et al. 2020) and author validation; BIOMASS-based biomass workflow is established.
  - Consistent observer for eye-height measurements; data quality checks and an explicit outlier exclusion (four data points with anomal Fisher’s alpha) noted.

## Data access, governance, and stewardship considerations
- Data accessibility:
  - Vegetation and plot-level data are hosted via the NERC Environmental Information Data Centre (EIDC) with a documented DOI/link in the accompanying references.
  - Core data sources include veg_plot_summary.csv and related outputs used to reproduce analyses in analyses_and_figures.R.
- Reproducibility and versioning:
  - Clearly linked scripts (carbon_stock_calculations.R, analyses_and_figures.R) to reproduce results and figures from Fleiss et al. (2020).
  - Use of established R packages (BIOMASS, biomass, vegan) and published models ensures methodological consistency and transparency.
- Metadata and documentation:
  - Comprehensive description of field methods, plot design, measurement protocols, and data columns provided to support interpretation and reuse.
  - Documentation covers data structure, column definitions, and data processing steps, enabling replication and potential updates with new data.
- Data governance considerations for data stewards:
  - Clear lineage from field collection to biomass estimation and statistical analyses; inclusion of multiple height models enhances robustness and traceability.
  - Detailed quality control notes ( observer consistency, outlier handling) support data integrity.
  - Data are designed to be updated with future field campaigns or extended datasets, given the modular R scripts and explicit data structure.

## Key references for context and provenance
- Fleiss et al. (2020). Conservation set-asides improve carbon storage and support associated plant diversity in certified sustainable oil palm plantations. Biological Conservation.
- Waddell et al. (2020). Vegetation and habitat data for fragmented and continuous forest sites in Sabah, Malaysian Borneo, 2017. NERC EIDC.
- Supporting methodological references: Chave et al. (2014); Feldpausch et al. (2012); Réjou-Méchain et al. (2017); Pfeifer et al. (2015); Barbone et al./others as cited in the document.