# Supporting documentation for R code to reproduce analyses of aboveground carbon stocks and associated plant diversity in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

- Purpose and context
  - Provides supporting information for reproducing analyses from Fleiss et al. 2020 (Biological Conservation).
  - Uses data and scripts to examine aboveground carbon stocks (AGC) and plant diversity across fragmented forest set-asides in RSPO-certified oil palm plantations and continuous forest in Sabah, Malaysian Borneo, collected in 2017.
  - Data and code underpin comparisons of conservation set-asides, continuous forest, and simulated oil palm AGC, and explore drivers of AGC and biodiversity.

- Data, inputs, and data provenance
  - Base data: veg_plot_summary.csv (plot-level vegetation and characteristics) and related field protocols; full vegetation data available from Waddell et al. 2020.
  - Field design: 18 sites (14 fragmented set-asides, 4 continuous forest); nested plots within each site: main 30 m radius, 20 m radius subplot, 5 m radius sapling subplot; seedlings sampled in eight 1x1 m quadrats.
  - Measurements include: dbh for trees and palms, estimated tree heights (eye estimates with validation via clinometer for a subset), liana dbh, coarse woody debris, soil parameters (pH, P, N, organic C, C:N, moisture), and topography.
  - Taxonomy and wood density: species/genus identifications; wood densities from Global Wood Density Database; carbon conversion set at 47.1%.

- What the code does
  - Reconstructs aboveground carbon stocks for:
    - Live tree biomass (≥10 cm dbh) using pantropical allometric equations (Chave et al. 2014) via the BIOMASS R package.
    - Palm biomass using a mixed-species model (Goodman et al. 2013) with a fixed 0.37 dry mass fraction.
    - Liana biomass using pantropical allometric equations (Schnitzer et al. 2006).
    - Coarse Woody Debris (CWD) biomass by volume × wood density, with decay class considerations.
    - Oil palm AGC using time-averaged growth curve functions (Carlson et al. 2013, 2012).
    - Carbon content assumed at 47.1% for all biomass.
  - Height estimation approaches for biomass:
    - Eye-derived field heights (primary method).
    - Climatic model (Chave et al. 2014) incorporating environmental stress.
    - Southeast Asia regional model (Feldpausch et al. 2012).
  - Produces a comprehensive plot-level data frame (plot_carbon) with numerous AGC metrics across components and methods.
  - Calculates biodiversity metrics (genus richness and Fisher’s alpha) for seedlings, saplings, and trees.

- Outputs and outputs formats
  - Primary data object: plot_carbon (per plot, 49 plots across 18 sites) with columns for:
    - Site_plot_code, site-level and plot-level AGC by component and method (e.g., tree_carbon_Mgha, tree_carbon_chaveE_Mgha, etc.), total AGC, palm and liana contributions, CWD, and oil palm AGC estimates.
    - Descriptive statistics and biodiversity indicators (mean DBH by class, wood density means, stem densities, Fisher’s alpha, genus richness).
    - Topographic and environmental covariates (slope, elevation, soil parameters, fragmentation metrics, edge indices, distances to edges, years since fragmentation).
  - Analytical outputs (as described in the document):
    - Pearson correlations and scatterplots comparing the three height-estimation methods.
    - Land-use type comparisons (conservation set-asides, continuous logged, continuous primary, and simulated oil palm AGC data) using Bayesian linear mixed-effects models.
    - Spatial autocorrelation diagnostics (Moran’s I) on model residuals.
    - Variation partitioning via PCA for fragmentation metrics and soil parameters.
    - Generalized additive mixed models (GAMMs) for AGC predictors (fragmentation, soil gradients, elevation, slope).
    - Bayesian GLMMs for relationships between AGC and genus richness / Fisher’s alpha across size classes.
    - Predictive plots of average oil palm AGC under varying set-aside cover (1–100%), with prediction intervals.
  - Reproducibility and validation
    - Code and analyses have been peer-reviewed and accepted for Biological Conservation (Fleiss et al. 2020).
    - Biomass estimation workflow leverages established packages and models; height estimation methods tested against field estimates.

- Study design and data structure details
  - Sites and sampling
    - 18 sites: 14 fragmented set-asides in RSPO-certified oil palm plantations; 4 primary continuous forest sites.
    - Sampling avoids spatial autocorrelation: minimum 1.5 km between sites; edge effects considered in fragmented sites.
  - Plot design and measurements
    - Main plots: 30 m radius; 49 plots total.
    - Subplots: 20 m radius for smaller trees and palms (≥10 cm and <25 cm dbh), 5 m radius for seedlings.
    - Measured variables include dbh classes, heights, liana associations, CWD, soil parameters, and topography.
  - Data quality and governance
    - Field measurements consistently conducted by a single observer for height estimates; data checked for errors.
    - Excluded four outlier data points (three seedlings, one sapling) in analyses due to anomal Fisher’s alpha values.
    - Clear documentation of data structure and variable definitions in veg_plot_summary.csv.
  - Data availability and references
    - Data and summary tables contribute to analyses in Fleiss et al. 2020; full vegetation data available via Waddell et al. 2020.
    - Data repository: Vegetation and habitat data for fragmented and continuous forest sites in Sabah, Sabah, 2017 (NERC EIDC).

- Analytical workflow and software
  - All calculations performed in R (R 3.6.2).
  - Key methods and tools:
    - Biomass estimation via BIOMASS package; Chave et al. 2014 allometric equations; wood density from Global Wood Density Database.
    - Palm biomass modeling (Goodman et al. 2013) with fixed dry mass fraction.
    - Liana and CWD biomass allometric and volumetric calculations per standard references.
    - Flowering and seedling biodiversity metrics calculated with vegan package (Fisher’s alpha).
    - Fragmentation and soil gradients summarized via PCA; landscape fragmentation metrics computed for multiple buffer sizes (0.2–2 km).
    - Advanced models: Bayesian LMMs, GLMMs, GAMMs; Moran’s I for spatial autocorrelation.
  - Outputs include complete figures and statistics from Fleiss et al. 2020, enabling replication of main findings.

- Practical notes for users of the monitoring framework
  - The code is designed to reproduce specific analyses from the 2020 Biological Conservation paper; it relies on the veg_plot_summary.csv dataset and linked analyses scripts (analyses_and_figures.R).
  - Reproducibility hinges on data provenance, consistent height estimation, and application of standardized allometric equations and biomass conversions.
  - Data governance considerations highlighted in the archetype context (data availability, metadata, and openness) are addressed by explicitly linking to data sources and providing detailed metadata within the dataset structure, while recognizing potential barriers to sharing certain measurements.

- Key references and provenance
  - Fleiss et al. 2020 (Biological Conservation) – primary analyses and context.
  - Waddell et al. 2020 – vegetation data source.
  - Chave et al. 2014; Feldpausch et al. 2012 – height-allometry models.
  - Goodman et al. 2013; Schnitzer et al. 2006 – palm and liana biomass models.
  - Pfeifer et al. 2015; Chambers et al. 2000 – CWD biomass and geometry.
  - Carlson et al. 2013, 2012; Carlson et al. – oil palm AGC growth curves.
  - Data and methods also align with RSPO guidelines and HCSA framing for forest edge and fragmentation.