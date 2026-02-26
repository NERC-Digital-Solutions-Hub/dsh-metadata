# biodiversity in relation to fire in Sebangau National Park, Central Kalimantan, Indonesia, 2003-2019

- Objective and scope
  - Methodological details for collecting, processing, and assessing ecological components related to fire impacts.
  - Covers 17 ecosystem properties and 21 biodiversity variables in Sebangau National Park, Indonesia.
  - Associated with Harrison, Deere et al. (2024) and licensed CC-BY.

- Study context and provenance
  - Location: Natural Laboratory of Peat-swamp Forest (NLPSF), Sebangau National Park, Central Kalimantan.
  - Long-term data: 16-year ecological time series (2003–2019) with multiple megafire events; 181 sampling locations across burn histories (new burn 2015, old burn 2006, unburned).
  - Fire history integrated with wider landscape effects (haze, smoke).

- Data scope and components
  - Spatial assessment: 27 ecological components across three burn treatments (new burn, old burn, unburned).
    - Ecosystem properties: microclimate (temperature), vegetation cover/density/structure (canopy, ferns, grasses, pitcher plants, lianas, seedlings, saplings, trees), tree height, aboveground biomass.
    - Biodiversity: trees, Odonata, Lepidoptera (butterflies), herpetofauna, avian-focused soundscape indices (Bioacoustic Index, Acoustic Complexity Index, Acoustic Diversity Index, Normalised Difference Soundscape Index).
  - Temporal assessment: 16-year time series (2003–2019) across nine ecological components.
    - Ecosystem properties: river pH, leaf fall (productivity), tree leaf flush and reproductive phenology.
    - Biodiversity: fruit-feeding butterflies, freshwater fish, ground-dwelling birds, medium-large mammals.
  - Data outputs: standardized mean differences (fire vs. unburned) for spatial analyses; time-series, occupancy, and covariate analyses for temporal assessments.

- Data collection methods (spatial)
  - Microclimate: temperature data from Thermochrons (August–September 2018) across burn treatments.
  - Vegetation: 45 nested plots (15 per treatment) with multi-scale transects; recording canopy cover, grass/fern density, counts of pitcher plants, large Pandanaceae, lianas, seedlings, saplings, and trees; biomass estimated via allometric methods.
  - Trees and biodiversity: taxonomic identification for 200 trees per set of plots; Odonata via 250 m transects; Lepidoptera via canopy fruit-baited traps; Herpetofauna via 6 transects; Acoustic Indices from avian-focused recorders.
  - Fire regime data: MODIS fire detections (2000–2020) used to identify megafires (monthly anomalies exceeding 95th percentile at provincial and local scales).

- Data collection methods (temporal)
  - Time-series data collected per season (season definitions vary by taxon; e.g., 3 months for terrestrial vertebrates, 1 month for others).
  - Biodiversity detection histories constructed; occupancy modelling used to handle imperfect detection.
  - Fire covariates: seasonal summaries of fire radiative power; distance/time since megafire; spatial buffers optimized by scale.

- Data quality, curation, and provenance
  - Rigorous observer training and consistent field leadership.
  - Outlier checks, data cleaning, and cross-checking with field notes; audio files scrutinized for disruptive noise.
  - Species identifications standardized using referenced taxonomic guides and experts; latin binomials ensured.
  - Forest specialist classifications applied to reduce confounding by generalist species (groupings by Trees, Odonata, Lepidoptera, Herpetofauna, Fish, Terrestrial Vertebrates).

- Species groupings and forest specialization
  - Forest specialist designations for all taxa, based on habitat dependence and sensitivity to disturbance.
  - Group files provided (Bird_Groups.csv, Mammal_Groups.csv, SpGroups_Specialists_AllTaxa.csv) to support analyses.

- Data structure, files, and metadata
  - A total of 24 files: 23 data files plus a metadata document.
  - Data folders include:
    - Meta-analysis inputs (MetaAnalysis_Treatment_AllSpecies.csv, MetaAnalysis_Treatment_Specialists.csv)
    - Spatial GLMM inputs (Spatial_GLMMs_AllSpecies.csv, Spatial_GLMMs_Specialists.csv)
    - Fire detection data (MODIS_Central_Kalimantan_Fires.csv, MODIS_Field_research_area_Fire.csv)
    - Occupancy detection datasets (OM_Detection_*.csv/.rds)
    - Covariate and temporal GLMM datasets (Temporal_GLMM_*.csv)
    - Covariate files for GLMMs (Temporal_GLMM_Covariates_*.csv)
  - Metadata document describes each file and column-level details to support reproducibility and discovery.

- Analytical framework
  - Spatial analyses: standardized mean differences (Hedges g) to compare burn treatments vs unburned controls; hierarchical mixed-effects meta-analysis with random effects for data type, components, and observations.
  - Temporal analyses: Bayesian GLMMs for ecosystem properties; hierarchical multispecies occupancy models for biodiversity with imperfect detection; model comparisons to isolate fire regime drivers (fire properties vs. spatio-temporal proximity).
  - Data are centered and scaled for covariates; spatial random effects account for clustered sampling; time-series models incorporate random walks and season-specific effects.
  - Software and approach: Bayesian inference using rstan (meta-analysis) and JAGS (GLMMs and occupancy models) via R.

- Data license and accessibility
  - Supporting Information is CC-BY licensed; datasets are structured for reuse by researchers and data managers.
  - Data governance emphasizes discoverability, format consistency, metadata availability, and updates.

- Key references and tools
  - MODIS fire detections, standard biodiversity guides, and multiple methodological references underpin data collection, classification, and analysis pipelines.
  - Emphasis on forest specialist designations, rigorous species identification, and consistent metadata for cross-study comparability.

- Practical implications for data leaders
  - Demonstrates end-to-end data stewardship from field collection to advanced modelling and dissemination.
  - Highlights importance of harmonized metadata, standardized groupings (forest specialists), and transparent data provenance to enable cross-project data sharing and reuse.
  - Provides a replicable framework for assessing environmental drivers (fire regimes) across spatial and temporal scales, suitable for networked data ecosystems and policy-relevant analyses.