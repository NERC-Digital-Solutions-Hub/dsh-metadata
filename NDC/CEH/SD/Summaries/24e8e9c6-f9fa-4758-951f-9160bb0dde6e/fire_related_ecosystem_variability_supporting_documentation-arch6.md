# biodiversity in relation to fire in Sebangau National Park, Central Kalimantan, Indonesia, 2003-2019

## Overview
- Methodological details for collecting, processing, and assessing ecological components (17 ecosystem properties and 21 biodiversity variables) in relation to fire impacts in the Natural Laboratory of Peat-swamp Forest special research Zone (NLPSF), Sebangau National Park, Indonesia.
- Supporting Information for Harrison, Deere et al. (2024) “Impacts of fire and prospects for recovery in a tropical peat forest ecosystem.” CC-BY licensed.
- Aims to enable exploration and analysis of fire-related biodiversity and ecosystem responses across spatial and temporal scales.

## Data provenance and scope
- Provenance: 16 years of ecological data from NLPSF, a peat-swamp forest site with a history of logging, drainage modifications, and fire susceptibility; includes both direct fire impacts and indirect landscape-level effects (haze).
- Spatial scope: 181 sampling locations spanning three fire history treatments—new burn (N=72), old burn (N=27), unburned (N=82)—to compare against unburned controls.
- Temporal scope: 16-year time series (Sept 2003–Dec 2019) capturing multiple megafires; seasonal/time-series analyses cover annual to multi-year fire regimes.

## Data collected and variables (spatial assessment)
- Ecosystem properties: microclimate (temperature), vegetation cover and density (canopy, grasses, ferns, pitcher plants, lianas, seedlings, saplings, trees), and forest structure (tree height, aboveground biomass).
- Biodiversity: trees (species richness/abundance), Odonata (Anisoptera, Zygoptera), Lepidoptera (butterflies: Papilionoidea), herpetofauna (amphibians and reptiles), avian-focused soundscape indices (Bioacoustic Index, Acoustic Complexity Index, Acoustic Diversity Index, Normalised Difference Soundscape Index).
- Fire regime data: MODIS thermal anomalies (MCD14ML, high-confidence detections) for Central Kalimantan and NLPSF area; megafire periods defined using 95th percentile thresholds of fire frequency and radiative power.
- Other biophysical measurements: river pH, forest productivity via leaf-fall, tree leaf flush and reproductive phenology, and fish and terrestrial vertebrate surveys.
- Units: detailed in accompanying Metadata file.

## Data collected and variables (temporal assessment)
- Time-series components (2003–2019): nine ecological components including river pH, leaf-fall productivity, leaf flush and phenology (fruit/flower expression), fruit-feeding butterflies, freshwater fish, ground-dwelling birds, and medium-large mammals.
- Data structure: ecosystem properties as aggregated time-series by site/season; biodiversity as occupancy detection matrices.
- Megafire-focused covariates: time since last megafire, distance from previous megafire, and covariates across optimized spatial buffers.

## Data collection methods and protocols
- Spatial assessment components:
  - Microclimate: DS1921G-F5 Thermochrons; 30-minute temperature readings; maximum daily temperature used as the metric.
  - Vegetation: 45 nested 10x10 m plots (15 per treatment); canopy cover, grass/fern cover, density of pitcher plants, large Pandanaceae, lianas, seedlings, saplings, and trees; biomass estimated using allometric equations with DBH and wood density.
  - Species inventories: trees identified to species where possible.
  - Odonata, Lepidoptera, Herpetofauna: standardized transects and canopy trapping methods; species-level identification supported by guides and experts.
  - Avian soundscape: autonomous recorders (Song Meter SM4); 2-hour daily recordings during peak bird activity; indices derived via Soundecology package.
- Fire regime characterization: MODIS fire detections, with megafire periods identified per province and NLPSF boundary.
- Other data streams: river pH, leaf-fall traps, phenology plots, butterfly canopy traps, fish traps, camera traps for terrestrial vertebrates.
- Forest specialists classification: datasets filtered to forest specialist species based on literature and expert opinion to control for generalist responses.
- Quality control: observer training, consistent field leadership, outlier and error checks, exclusion of disrupted sound files, careful species identification with reference guides.

## Analytical approaches
- Spatial analyses:
  - Effect sizes: standardized mean differences (Hedges g) comparing burn treatments to unburned controls, with heteroscedasticity adjustments.
  - Proportional changes: calculated from GLMM-estimated means.
  - Synthesis: hierarchical mixed-effects meta-analysis with random effects for data type, ecological components, and observations.
- Temporal analyses:
  - Seasonally partitioned time-series (primary sampling occasions) to reflect life histories and fire activity.
  - Biodiversity occupancy models: hierarchical multispecies occupancy with imperfect detection; random walk priors for inter-season sharing; season-specific intercepts and detection covariates.
  - Fire regime modelling: two candidate models per time-series—fire properties (frequency and intensity) and spatio-temporal proximity (space-time mediation).
  - Bayesian framework: analyses implemented in rstan and JAGS via R.
- Data normalization and structure:
  - Covariates centered and scaled; scale-optimized radii for fire covariates; spatial random effects to account for clustering.

## Data structure and access
- Data package includes 24 files: 23 data files plus a metadata document.
- Data groupings:
  - Species groupings: Bird_Groups.csv, Mammal_Groups.csv, SpGroups_Specialists_AllTaxa.csv.
  - Spatial analysis inputs: MetaAnalysis_Treatment_AllSpecies.csv, MetaAnalysis_Treatment_Specialists.csv, Spatial_GLMMs_AllSpecies.csv, Spatial_GLMMs_Specialists.csv, MODIS fire data files, occupancy detection data (OM_*.csv/.rds), covariate files (OM_Covariates_*.csv), Temporal GLMM outputs (Temporal_GLMM_*.csv).
- Metadata file describes the content and columns of each data file.

## Outputs, data products, and intended use
- Outputs include standardized effect sizes and meta-analytic summaries of fire impacts, GLMM-derived estimates of proportional changes, occupancy model results (presence/absence, detection probabilities), time-series analyses of ecosystem properties and biodiversity, and covariate effects related to megafire events.
- Data products are designed to enable users to explore fire-related ecological changes, compare burn histories, and assess recovery trajectories across taxa and ecosystem properties.

## Licensing and access
- Supplementary Information is CC-BY licensed; dataset components include openly documented data files and metadata to facilitate reuse.
- Clear provenance and methodological detail to support reproducibility and reuse in related biodiversity-fire studies.

## Limitations and considerations for users
- Some data gaps due to fire disruption (e.g., no data in Oct 2015 and Sep 2019 for certain datasets).
- Sampling effort and survey months varied across treatments and taxa, which may influence comparisons.
- Forest specialist classifications rely on literature and expert opinion; some taxa remain partially unresolved at species level.
- Spatial and temporal scales reflect a tropical peat swamp system; generalizing beyond similar ecosystems should be done with caution.