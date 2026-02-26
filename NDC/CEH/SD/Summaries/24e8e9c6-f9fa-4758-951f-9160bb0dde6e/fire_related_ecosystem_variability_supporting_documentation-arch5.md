# biodiversity in relation to fire in Sebangau National Park, Central Kalimantan, Indonesia, 2003-2019

## Aim
- Present methodological details for collecting, processing, and assessing 17 ecosystem properties and 21 biodiversity variables in relation to fire impacts in the Natural Laboratory of Peat-swamp Forest (NLPSF), Sebangau National Park, Indonesia.
- Support Harrison, Deere et al. (2024) on the impacts of fire and prospects for recovery in tropical peat forest ecosystems; includes accompanying datasets and licencing (CC-BY).

## Study site and provenance
- Location: NLPSF, Sebangau National Park, Central Kalimantan, Indonesia.
- Landscape context: ombrogenous peat-swamp forest with a history of selective logging and illegal hand-logging, canal-driven peat drainage, and fire risk during dry seasons.
- Long-term dataset: 16 years of data on ecological components (17 ecosystem properties and 21 biodiversity variables), enabling spatial and temporal fire-related analyses.
- Fire regime context: megafire periods identified using MODIS thermal anomaly data (2000–2020), with six megafire events used to examine direct and indirect fire effects.

## Datasets and scope
- Spatial assessment: 27 ecological components across 181 sampling locations, comparing three fire treatments (new burn, old burn, unburned).
- Temporal assessment: 16-year time-series (2003–2019) across 236 sampling locations for nine ecological components.
- Data types cover ecosystem properties (microclimate, vegetation, forest structure) and biodiversity (trees, Odonata, butterflies, herpetofauna, avian-focused soundscapes) plus other measures (pH, leaf litter production, phenology, fish, terrestrial vertebrates via camera traps).
- Units and metadata: nature and units of recorded values described in accompanying Metadata file; data are standardized for cross-study synthesis (e.g., effect sizes, GLMMs, occupancy models).

## Spatial assessment data collection (three fire treatments)
- Microclimate: Automatic temperature logging (DS1921G-F5 Thermochrons) across 2018 measurements, summarized as maximum daily temperature.
- Vegetation: 45 nested 10x10 m plots (15 per treatment) with transects; recorded canopy/grass/fern cover, densities of pitcher plants and Pandanaceae, lianas, seedlings, saplings, and trees; biomass estimated from DBH, height bands, and wood density.
- Trees: Taxonomic identification of live trees (n=200 per plot set); ~15% unresolved to species level and excluded.
- Odonata, Lepidoptera (butterflies), Herpetofauna: Standardized transects and canopy traps; timeframes and sampling schemes noted (months, transect counts, marking for recaptures, avoidance of resampling).
- Avian-focused soundscape: Autonomous recorders (9 locations, three treatments) recording dawn activity; four acoustic indices derived (Bioacoustic Index, Acoustic Complexity Index, Acoustic Diversity Index, Normalised Difference Soundscape Index) using Soundecology package.
- Fire regime characterization: Historical fire regime profile via MODIS (MCD14ML) with high-confidence detections; megafire months identified using 95th percentile thresholds for fire frequency and radiative power at both provincial and local scales.
- Other variables: River pH (7.6 km transect), leaf litter fall (leaf-fall as primary component), tree phenology (leaf flush and fruit/flower expression), fish communities, and terrestrial vertebrates via camera traps.
- Specialization filtering: Datasets filtered to forest specialist species to reduce generalist confounding effects (grouped by trees, Odonata, Lepidoptera, herpetofauna, fish, and terrestrial vertebrates).

## Temporal assessment data collection (time-series, 2003–2019)
- Sampling seasons: Defined per dataset to align with life histories and fire activity (3-month seasons for terrestrial vertebrates; 1-month for others).
- Fire covariates: Seasonal summaries of fire radiative power; computed time since last megafire and distance from previous megafire detections; covariates centered and scaled.
- Ecological trends: 
  - Ecosystem properties: river pH, leaf fall, leaf flush/phenology data (fruit/flowers/new leaves).
  - Biodiversity time-series: occupancy-detection data for fruit-feeding butterflies, freshwater fish, ground-dwelling birds, and medium-large mammals.
- Modelling approach: Bayesian GLMMs and occupancy models to capture temporal trends with season-specific intercepts and spatial random effects; random walks for occupancy intercepts to share information across seasons.
- Model comparisons: Two candidate temporal models per dataset—fire properties (frequency and intensity) and spatio-temporal proximity (distance/time since megafire); quadratic terms used where appropriate.
- Software: Analyses implemented in R with rstan (hierarchical meta-analysis) and JAGS (GLMMs and occupancy models).

## Fire regime characterization
- Data source: MODIS fire detections (Central Kalimantan and NLPSF boundary + buffer, 1 km resolution).
- Megafire definition: Months with fire frequency and cumulative radiative power exceeding the 95th percentile at both scales; consecutive months treated as a single megafire event.
- Identified megafire periods: October 2004, October 2006, October 2009, Sep–Oct 2014, Sep–Oct 2015, Aug–Sep 2019.

## Data quality, governance, and standards
- Training and consistency: Comprehensive observer training and ongoing refresher sessions; same field team leaders for each variable to ensure consistency.
- Data integrity: Systematic screening for outliers, typos, and missing data; cross-checking with field sheets; audio file quality checks to exclude disrupted recordings.
- Taxonomic consistency: Standardized nomenclature using APG (trees), Orr (Odonata), Cleary et al., Hirowatari et al. ( Lepidoptera), IUCN-based classifications for other taxa; cross-referenced with Fishbase and other taxonomic references.
- Metadata and provenance: 24 data files (23 data files + metadata); explicit grouping by species groupings and analytical inputs; metadata document links to each data file and describes column meanings.
- Licensing and reuse: Study datasets accompany a PNAS paper and are licenced CC-BY; includes well-documented methods for reuse and replication.

## Species groupings and forest specialization
- Forest specialist classifications provided for all taxa to support targeted analyses:
  - Birds, Mammals, and all taxa groups (SpGroups_Specialists_AllTaxa.csv).
  - Groupings for IUCN threat status and foraging/trophic guilds (Bird_Groups.csv; Mammal_Groups.csv).
- Grouping designations used across spatial and temporal analyses to isolate the responses of forest-dependent species from generalists.

## Data structure and access
- Total files: 24 (23 data files plus supplementary metadata).
- Data categories:
  - Species groupings and specialist designations (Bird_Groups.csv; Mammal_Groups.csv; SpGroups_Specialists_AllTaxa.csv).
  - Spatial analyses: Meta-analysis inputs (MetaAnalysis_Treatment_AllSpecies.csv; MetaAnalysis_Treatment_Specialists.csv), Spatial_GLMMs_AllSpecies.csv, Spatial_GLMMs_Specialists.csv.
  - Fire and detection data: MODIS_Central_Kalimantan_Fires.csv; MODIS_Field_research_area_Fire.csv.
  - Occupancy and covariates by taxa: OM_Detection_*.csv/.rds and OM_Covariates_*.csv.
  - Temporal analyses: Temporal_GLMM_Litterfall.csv; Temporal_GLMM_pH.csv; Temporal_GLMM_Phenology.csv; Temporal_GLMM_Covariates_*.csv.
- Data structure supports grouping by ecological component, data type (ecosystem property vs biodiversity), and species specialization, with inputs prepared for the spatial and temporal analytical procedures described above.