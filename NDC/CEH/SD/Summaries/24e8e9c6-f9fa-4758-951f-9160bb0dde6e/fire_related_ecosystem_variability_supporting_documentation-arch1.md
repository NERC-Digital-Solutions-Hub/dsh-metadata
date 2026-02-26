# biodiversity in relation to fire in Sebangau National Park, Central Kalimantan, Indonesia, 2003-2019

## Overview
- Methodological details for collecting, processing, and evaluating ecological components related to fire impacts.
- Covers 17 ecosystem properties and 21 biodiversity variables.
- Associated with Harrison, Deere et al. (2024) on impacts of fire and recovery prospects in a tropical peat forest; licensed CC-BY.

## Study setting and data scope
- Location: Natural Laboratory of Peat-swamp Forest special research zone (NLPSF), Sebangau National Park, Central Kalimantan, Indonesia.
- Long-term context: peat-swamp forest with history of logging (up to 1997) and illegal hand-logging (until 2004); mosaic of burned and unburned areas; haze impacts.
- Temporal span: ecological time-series from 2003 to 2019; 16-year span with multiple megafire events; datasets include at least two megafires per series.
- Fire regime characterization: MODIS thermal anomalies (MCD14ML) from 2000–2020; megafires defined as months with anomalous fire activity (95th percentile) at both provincial and NLPSF boundary scales; six megafire periods identified (2004, 2006, 2009, 2014-2015, 2019).

## Data collected (spatial assessments)
- Treatments: new burn (N=72 locations), old burn (N=27), unburned forest (N=82); data compared against unburned controls.
- Microclimate: temperature, max daily values; measured Aug-Sep 2018 with Thermochrons.
- Vegetation: 45 nested plots (15 per treatment) with transects; canopy and ground cover, grass/fern density, and densities of pitcher plants, Pandanaceae, lianas, seedlings, saplings, and trees; biomass estimated for aboveground live biomass.
- Trees: taxonomic identities for ~200 live trees per plot; ~15% unresolved to species.
- Odonata (dragonflies/damselflies): 22 transects; separate Anisoptera and Zygoptera analyses; standard mark-recapture-like approach to minimize recaptures.
- Lepidoptera (butterflies): canopy traps along transects; fruit-baited traps sampling ground and canopy levels; monthly sampling 2018-2019.
- Herpetofauna: amphibians and reptiles on six 1-km transects; diurnal and nocturnal surveys over three days.
- Avian-focused soundscape indices: four indices (Bioacoustic Index, Acoustic Complexity Index, Acoustic Diversity Index, Normalised Difference Soundscape Index) from 9 locations using Song Meter recorders; recordings during bird activity window; 2-hour daily samples.
- Terrestrial vertebrates: ground-dwelling birds and medium-large mammals via 174 camera-trap locations; typical deployment ~274 CTN per unit; extensive presence data used for occupancy.
- Fish: riverine fish surveys via 20 traps along river banks; species-level identification and counting.
- Data units: standardized across datasets; detailed in accompanying Metadata file.

## Data collected (temporal assessments)
- Time-series biodiversity: nine ecological components tracked across 578 temporally-replicated surveys at 236 locations; includes fruit-feeding butterflies, freshwater fish, ground-dwelling birds, and medium-large mammals.
- Ecosystem properties time-series: river pH, litter-fall (leaf fall), and tree phenology (leaf flush and fruit/flower expression) tracked monthly from 2003–2019 (with some gaps due to fire disruptions).
- Occupancy data: species detections (birds, fish, mammals, butterflies) used in occupancy models that account for imperfect detection.
- Seasonality: primary sampling occasions defined by life-history and fire activity (3 months for terrestrial vertebrates; 1 month for other groups).

## Data processing, quality control, and classification
- Observer training and ongoing quality control; consistency maintained by using the same field leaders for each variable.
- Data screening for outliers, typos, and missing values; spectrogram inspection to remove disrupted audio files; cross-checks with team members.
- Taxonomic standardization: nomenclature aligned to APG, IUCN, FishBase, and other authoritative guides; local/common names corrected to Latin names.
- Forest specialists classification: groups designated as forest specialists vs. generalists across taxa (trees, odonata, Lepidoptera, herpetofauna, fish, terrestrial vertebrates) based on habitat dependence and sensitivity to disturbance.

## Analytical framework
- Spatial assessments:
  - Ecological components summarized as means by fire treatment; temperature as maximum daily values.
  - Biodiversity metrics as species counts/abundances averaged across temporal replicates.
  - Species richness bias-corrected for uneven sampling; pairwise burn vs unburned comparisons using standardized mean differences (Hedges g) with heteroscedasticity adjustments.
  - Hierarchical mixed-effects meta-analysis to synthesize fire impacts across datasets; random effects for data type, ecological components, and observations.
  - Generalized linear mixed-effects models (GLMMs) to quantify proportional changes between burn treatments and unburned controls.
- Temporal assessments:
  - Time-series partitioned into seasons (sampling seasons) for modeling; detection histories built for biodiversity datasets.
  - Seasonal covariates: seasonal summaries of fire radiative power; covariates across buffers scaled via scale optimization.
  - Bayesian GLMMs for ecosystem properties with season-specific random intercepts and spatial random effects.
  - Multispecies occupancy models for biodiversity, incorporating imperfect detection, with random walk priors for temporal smoothing and season-specific detection processes.
  - Two candidate models for drivers: fire properties (frequency and intensity) and spatio-temporal proximity (space/time distance from megafires); models include quadratic terms where appropriate.
- Software and frameworks: Bayesian analysis implemented in rstan and JAGS invoked through R (v4.x).

## Data structure, files, and accessibility
- 24 data files total: 23 data files plus a metadata document; metadata describes columns and data provenance.
- Key groupings and inputs:
  - Species groupings: Bird_Groups.csv, Mammal_Groups.csv, SpGroups_Specialists_AllTaxa.csv.
  - Meta-analysis inputs: MetaAnalysis_Treatment_AllSpecies.csv, MetaAnalysis_Treatment_Specialists.csv.
  - Spatial inputs: Spatial_GLMMs_AllSpecies.csv, Spatial_GLMMs_Specialists.csv.
  - Fire regime data: MODIS_Central_Kalimantan_Fires.csv, MODIS_Field_research_area_Fire.csv.
  - Occupancy data: OM_Detection_Birds.csv, OM_Detection_Butterflies.csv, OM_Detection_Fish.csv, OM_Detection_Mammals.rds.
  - Covariates for occupancy: OM_Covariates_*.csv.
  - Temporal GLMM inputs: Temporal_GLMM_Litterfall.csv, Temporal_GLMM_pH.csv, Temporal_GLMM_Phenology.csv, plus covariates files.
- Output aim: provide matched inputs for hierarchical meta-analysis, GLMMs, and multispecies occupancy models used in the associated study (Harrison et al. 2024).

## Relevance to data-driven questions
- Enables analysis of how fire (including megafire events) alters a wide range of ecosystem properties and biodiversity components in tropical peat forests.
- Supports cross-taxonomic synthesis and the isolation of forest-specialist responses versus generalist responses.
- Combines spatial contrasts (burn treatments vs unburned) with long-term temporal dynamics to assess recovery prospects and potential drivers of change.
- Provides a rigorous, transparent data pipeline with quality controls, standardized metrics, and accessible metadata suitable for replication and further analysis.