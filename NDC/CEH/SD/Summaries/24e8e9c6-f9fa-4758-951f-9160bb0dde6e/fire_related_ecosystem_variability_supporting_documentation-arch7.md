# biodiversity in relation to fire in Sebangau National Park, Central Kalimantan, Indonesia, 2003-2019

- Overview
  - Methodological details for collecting, processing, and assessing 17 ecosystem properties and 21 biodiversity variables relative to fire impacts.
  - Supporting information for Harrison, Deere et al. (2024) “Impacts of fire and prospects for recovery in a tropical peat forest ecosystem.”
  - Datasets are CC-BY licensed and designed to underpin map-based data products and GIS analyses.

- Provenance and study context
  - Location: Natural Laboratory of Peat-swamp Forest (NLPSF) within Sebangau National Park, Central Kalimantan, Indonesia.
  - 16 years of ecological data across three fire history categories: new burn (2015), old burn (2006), and unburned forest.
  - Fire history enables spatial comparisons (new vs old vs unburned) and temporal assessments across 2003-2019, including exposure to regional haze.
  - Fire regime data cover megafire events defined by MODIS thermal anomalies (1 km resolution) and 95th percentile thresholds; six megafire periods identified.

- Spatial assessment components
  - Microclimate: Temperature measured via Thermochrons attached to acoustic units (August–September 2018); maximum daily temperature per sampling day.
  - Vegetation: 45 nested 10x10 m plots (15 per treatment) with per-plot metrics for canopy/grass/fern cover, densities (pitcher plants, Pandanaceae, lianas, seedlings, saplings, trees), and forest structure (tree height, aboveground biomass).
  - Trees: Taxonomic identities assigned for ~200 live trees per plot.
  - Odonata: 22 transects (250 m) surveyed Jan–July 2019; separate Anisoptera/Zygoptera treatments; standard mark-recapture style protocols.
  - Lepidoptera (Papilionoidea): Canopy traps along transects; monthly sampling Aug 2018–2019; canopy and ground sampling; individual marking and recaptures tracked.
  - Herpetofauna: Amphibians and reptiles surveyed along six 1-km transects (Aug–Sept 2021); diurnal and nocturnal surveys over three days.
  - Avian-focused soundscape indices: Acoustic recordings at nine locations (peak bird activity hours) using Song Meter units; four indices computed (Bioacoustic Index, Acoustic Complexity Index, Acoustic Diversity Index, Normalised Difference Soundscape Index).
  - Fire regime characterization: MODIS fire detections (MCD14ML, Collection 6) with low-confidence removals; megafire periods defined and cross-validated at provincial and local scales.
  - River pH: 20 locations along Sebangau River (Sept 2014–Dec 2015); monthly measurements.
  - Forest productivity (leaf fall): 16 traps (1 m2); monthly leaf-fall weighting (excluding December 2007 disturbances).
  - Tree phenology: Monthly leaf flush and fruit/flower expression data from unburned plots (Sept 2003–Jan 2018); phenology scores as percent stems with fruit/flowers/flush.
  - Butterflies: 20 canopy traps (two unburned transects) with canopy stratification and monthly checks (2012–2018); marking and recaptures tracked.
  - Fish: 20 traps along river banks (Sept 2014–Dec 2015); species-level counts; spacing and baiting as per local practices.
  - Terrestrial vertebrates: 174 camera-trap locations (May 2008–Jan 2020) for ground-dwelling birds and medium-large mammals; data aggregated by location.
  - Forest specialist classifications: taxa-specific rules to identify forest-dependent species (e.g., pioneer trees, forest-associated Odonata, Lepidoptera, herpetofauna, fish, terrestrial mammals/birds).

- Biodiversity and data standardization
  - Species grouping files: Bird_Groups.csv; Mammal_Groups.csv; SpGroups_Specialists_AllTaxa.csv to support analyses across spatial and temporal assessments.
  - Quality control: standardized observer training; cross-checking of data entries; outlier checks; sound-file screening for acoustic data; species identifications validated against taxonomic references and local experts.
  - Units and metadata: all recorded values documented in the accompanying Metadata file.

- Temporal assessment and time-series design
  - Primary sampling occasions defined as seasons (3 months for terrestrial vertebrates; 1 month for others); occupancy histories constructed per taxon group.
  - Fire covariates: seasonal sums of fire radiative power; derived measures include time since last megafire and distance from previous megafire.
  - Covariates extracted within scale-optimized buffers; data centered and scaled for modeling.

- Analytical framework
  - Spatial analyses: standardized mean differences (Hedges g) for burn vs unburned comparisons; adjustments for multiple controls and heteroscedasticity; pro-rating of sample sizes for non-independent comparisons.
  - Meta-analysis: hierarchical mixed-effects models to synthesize fire impacts across data types (ecosystem properties vs biodiversity) and components; variance-weighted estimates.
  - Proportional changes: generalized linear mixed-effects models (GLMMs) to estimate burn-related changes at the plot/sampling location level; covariates and spatial random effects included.
  - Temporal analyses: Bayesian GLMMs for ecosystem properties (season-specific random intercepts, spatial random effects); multispecies occupancy models for biodiversity with imperfect detection, season-specific intercepts, random walks for occupancy, and survey-effort covariates.
  - Model comparisons: fire properties model vs spatio-temporal proximity model; quadratic terms used where appropriate; analyses implemented in rstan and JAGS via R.

- Data structure and accessibility
  - 24 files total: 23 data files plus a metadata document; files organized by species groupings, spatial GLMM inputs, temporal GLMM inputs, and occupancy detection data.
  - Key data files include:
    - MetaAnalysis_Treatment_AllSpecies.csv; MetaAnalysis_Treatment_Specialists.csv
    - Spatial_GLMMs_AllSpecies.csv; Spatial_GLMMs_Specialists.csv
    - MODIS_Central_Kalimantan_Fires.csv; MODIS_Field_research_area_Fire.csv
    - Detection and Covariate files for Birds, Butterflies, Fish, Mammals; Temporal GLMM files for Litterfall, pH, Phenology, etc.
    - Temporal_Covariate files (Litterfall, pH, Phenology) and their covariates
  - Metadata document describes the columns and data file contents to facilitate GIS integration.

- GIS-oriented implications and potential map products
  - Spatially explicit comparisons of burn treatments relative to unburned controls across multiple ecological components.
  - Proportional-change maps at plot-level scales and aggregated across treatment groups.
  - Temporal trend maps and occupancy surfaces for key taxa, incorporating detection probabilities and sampling effort.
  - Fire regime maps showing megafire occurrences, radiative power, and proximity effects over time.
  - Scale-aware data integration: MODIS-based fire data (1 km) with finer-scale plot and transect data; buffers and scale-optimization steps documented for covariate extraction.

- Limitations and caveats relevant to GIS use
  - Temporal gaps due to field disruption (noted in several data series); uneven survey effort across treatments and months.
  - Some taxa had reduced sampling in certain periods due to safety concerns or operational disruptions.
  - Forest specialist classifications rely on literature-based references; some taxa had unresolved species identifications.

- Key references and data governance
  - Provisional datasets and metadata align with the Harrison et al. (2024) study and related methodological literature.
  - Data are provided with clear provenance, standardized grouping schemes, and established identification references to support reproducible GIS analyses.