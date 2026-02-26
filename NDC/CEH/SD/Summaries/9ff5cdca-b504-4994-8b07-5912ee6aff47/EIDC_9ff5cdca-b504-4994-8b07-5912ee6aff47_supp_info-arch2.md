# Supporting documentation for R code to reproduce analyses of aboveground carbon stocks and associated plant diversity in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

- Purpose
  - Provides the workflow and data necessary to reproduce analyses from Fleiss et al. (2020) on aboveground carbon stocks (AGC) and plant diversity across fragmented and continuous forests in Sabah, Malaysian Borneo.
  - Documents the R code, input data, methods, outputs, and validation steps used in the study.

- Data and inputs
  - Field data: 49 plots across 18 sites (14 fragmented set-asides in RSPO-certified oil palm plantations; 4 continuous forest sites).
  - Measurements include: live trees and palms (dbh 10–> cm, and subplots for smaller sizes), lianas, coarse woody debris (CWD), seedlings, topography, and five soil parameters (moisture, pH, available P, total P, total N, organic C, C:N).
  - Data summary: veg_plot_summary.csv (plot-level data used by analyses_and_figures.R); full vegetation data available from Waddell et al. (2020).
  - Study design: nested plots in circular 30 m radius main plots; 20 m radius subplots for smaller trees and CWD; 5 m radius subplots for seedlings; edge effects and fragmentation context captured via UAV-derived landscape metrics and buffer analyses.
  - Carbon contents and models: biomass-to-carbon conversion set at 47.1%; oil palm AGC modeled using time-averaged growth curves (Carlson et al., 2013, 2012).

- Methods and computational approach
  - Aboveground carbon stocks (live trees ≥10 cm dbh)
    - Biomass via pantropical allometric equation (Chave et al., 2014) using dbh, height, and wood density (from Global Wood Density Database).
    - Height estimation via three methods: (i) field eye estimates (20 m and 30 m plots), (ii) Chave et al. 2014 climatic model (environmental stress), (iii) Feldpausch et al. 2012 Southeast Asia regional model.
    - Height validation: eye estimates vs clinometer-derived (tangent method) for accuracy check.
  - Palms biomass: mixed-species model using dry mass fraction (0.37), diameter, and height (Goodman et al., 2013).
  - Lianas biomass: pant tropical allometric equation based on dbh (Schnitzer et al., 2006).
  - Coarse woody debris (CWD): biomass from volume×density; volume via frustrum of a cone; decay class densities assigned (Pfeifer et al., 2015).
  - Carbon content: fixed at 47.1% for all biomass (Thomas & Martin, 2012).
  - Oil palm AGC: time-averaged 0–30 year AGC with mean and 95% CIs; simulated data points (15) from a normal distribution using growth-curve parameters (Carlson et al., 2013, 2012).
  - Biodiversity metrics: genus richness and Fisher’s alpha for seedlings, saplings, and trees.
  - Data processing and analysis: all calculations performed in R (version 3.6.2).

- Outputs and data products
  - plot_carbon dataframe (N = 49 plots) with:
    - Site_plot_code, Site_code, Forest_type (Continuous primary, Continuous logged, HCV set-aside),
    - AGC metrics under different height-estimation schemes (tree_carbon_20m_Mgha, tree_carbon_30m_Mgha, tree_carbon_chaveE_20m_Mgha, tree_carbon_chaveE_30m_Mgha, tree_carbon_feldpausch_20m_Mgha, tree_carbon_feldpausch_30m_Mgha),
    - Tree counts and densities (tree_count_20m_nha, tree_count_30m_nha),
    - Totals for trees, lianas, CWD, and palms (tree_carbon_Mgha, palm_carbon_Mgha, liana_carbon_Mgha, CWD_carbon_Mgha, total_carbon_Mgha),
    - Palm and seedling/sapling metrics, wood density, mean DBHs, and other metadata (e.g., soil parameters, fragmentation and topography metrics, Fisher’s alpha, richness).
  - Time-averaged oil palm AGC estimates for 0–30 year period (mean, 95% CI, and 15 simulated datapoints).
  - Outputs of analyses described in the paper:
    - Pearson correlations and scatterplots among height-estimation methods for AGC.
    - Land-use type comparisons (conservation set-asides, continuous logged, continuous primary, simulated oil palm AGC).
    - Bayesian linear mixed-effects models (LMMs) for live tree/palm AGC and total AGC by land-use type.
    - Moran’s I tests for spatial autocorrelation in LMM residuals.
    - Pseudo-R² for lianas and CWD contributions to total AGC.
    - Vegetation structure comparisons across forest types (mean wood density, stem density, mean DBH) by size class.
    - Fragmentation and soil-parameter driver analyses:
      - PCA to derive fragmentation index (PC1) from multiple landscape metrics; PCA on soil parameters to derive gradients (PC1, PC2).
      - GAMMs to assess predictors (fragmentation, soil PCs, elevation, slope) on live tree and palm AGC.
    - Relationships between AGC and plant diversity via Bayesian GLMMs for each size class.
    - Predictions of average AGC for plantations with varying set-aside coverage (1–100%) and continuous forest comparisons.
  - Outputs include plots, tables, and model statistics consistent with Fleiss et al. (2020).

- Code structure and workflow
  - Core scripts:
    - carbon_stock_calculations.R: AGC calculations for plots, biomass components, and oil palm AGC.
    - analyses_and_figures.R: statistical analyses and figures using veg_plot_summary.csv.
  - Data file:
    - veg_plot_summary.csv: plot-level summary of vegetation, structure, and environmental variables.
  - Supplementary references and data sources:
    - Data and protocols aligned with Waddell et al. (2020) and Fleiss et al. (2020).
  - Software and reproducibility:
    - Analyses conducted in R (version 3.6.2); BIOMASS package used for tree biomass estimation; vegan for diversity metrics.
    - Height-model selection and model comparisons detailed within the code (modelHD in BIOMASS).

- Study context and monitoring relevance
  - Focuses on carbon storage and biodiversity in fragmented vs continuous forest within Sabah, Malaysia.
  - Compares conservation set-asides in RSPO-certified plantations to continuous forest and oil palm surroundings.
  - Addresses data-quality requirements for environmental monitoring: standardized field protocols, consistent biomass conversion, and transparent data structures.
  - Provides a data-driven basis for assessing the value of set-asides for carbon storage and associated plant diversity, with implications for land-use policy and forest conservation monitoring.

- Quality assurance and validation
  - Peer-reviewed basis: Fleiss et al. (2020) in Biological Conservation; code validated and accepted for publication.
  - Field and lab procedures followed established protocols; height estimates cross-validated with clinometer measurements.
  - Biomass estimation workflow implemented in a validated R package (BIOMASS) with careful data handling and taxonomic wood density assignments.

- Access and references
  - Data and supporting information linked to the Biological Conservation study (Fleiss et al., 2020) and related datasets (Waddell et al., 2020).
  - Key methodological references include Chave et al. (2014), Feldpausch et al. (2012), Carlson et al. (2012, 2013), Pfeifer et al. (2015), Goodman et al. (2013), and Williams et al. (Thomas & Martin, 2012).