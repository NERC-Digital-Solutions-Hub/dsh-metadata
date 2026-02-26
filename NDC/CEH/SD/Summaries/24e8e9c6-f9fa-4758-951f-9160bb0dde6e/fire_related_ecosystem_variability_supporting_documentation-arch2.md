# biodiversity in relation to fire in Sebangau National Park, Central Kalimantan, Indonesia, 2003-2019

## Aim and scope
- Provides methodological details for the collection, processing, and assessment of ecological components (17 ecosystem properties and 21 biodiversity variables) in relation to fire impacts.
- Supports the study “Impacts of fire and prospects for recovery in a tropical peat forest ecosystem” (Harrison et al. 2024, PNAS) and is licenced CC-BY.
- Aims to deliver consistent data formats and outputs to facilitate environmental health monitoring and policy performance assessment over time.

## Study site and context
- Natural Laboratory of Peat-swamp Forest special research zone (NLPSF), Sebangau National Park, Central Kalimantan, Indonesia.
- Long-term research history enabling 16 years of ecological data; ombrogenous, non-masting tropical peat-swamp forest with a legacy of selective logging (until 1997) and illegal hand-logging (until 2004) aided by canals causing peat drainage.
- Fire history creates a mosaic of unburned and burned areas; indirect fire impacts include haze exposure.

## Spatial and temporal assessment design
- Spatial assessment: three fire treatments compared to unburned controls:
  - New burn (N=72 locations)
  - Old burn (N=27)
  - Unburned forest (N=82)
- Temporal assessment: 16-year time-series (Sept 2003–Dec 2019) with at least two megafire events; 578 temporally-replicated surveys across 236 sampling locations for nine ecological components.
- Fire regime characterization: MODIS thermal anomalies (MCD14ML) data (2000–2020) to identify megafires (months with anomalous fire activity, using 95th percentile thresholds at provincial and local scales).

## Variables and components
- Ecosystem properties: microclimate (temperature), vegetation (canopy/fern/grass cover, densities of key plant groups), forest structure (tree height, aboveground biomass), river pH, leaf fall, leaf flush, and reproductive phenology (fruit/flower expression).
- Biodiversity groups: trees; Odonata (Anisoptera, Zygoptera); Lepidoptera: Papilionoidea (butterflies); herpetofauna (amphibians, reptiles); avian-focused soundscape indices (Bioacoustic Index, Acoustic Complexity Index, Acoustic Diversity Index, Normalised Difference Soundscape Index).
- Acoustic data collected with Song Meter SM4 units, focusing on avian frequency ranges (≤6 kHz) to reduce insect-dominated signals.

## Data collection methods (spatial and temporal)
- Spatial data collection per treatment:
  - Microclimate: temperature logged Aug–Sept 2018 using Thermochrons, every 30 minutes during daylight.
  - Vegetation: 45 plots (15 per treatment) with measurements of canopy cover, grass/fern density, and shrub/tree components; biomass estimates from all living trees; DBH-based biomass using pantropical allometric equations.
  - Odonata, Lepidoptera, Herpetofauna: standardized transects and canopy traps with careful mark-recapture/recapture considerations and diurnal/nocturnal surveys as appropriate.
  - Avian soundscape: nine locations with rotated recorder deployments; 2-hour daily samples during peak bird activity; four acoustic indices computed from 10-minute files.
- Temporal data collection:
  - Litterfall (leaf-fall) data from 16 traps along unburned transects (Dec 2005–Jan 2018); component separation and drying for field weights.
  - Phenology: monthly surveys (Sept 2003–Jan 2018) for fruit/flowers/leaf flush on plots; some months omitted due to fire disruption.
  - Butterflies: monthly canopy traps along unburned transects (2012–2018); paired traps sampling ground and canopy strata.
  - Fish: seasonal trapping in river (Sept 2014–Dec 2015); identification and release.
  - Terrestrial vertebrates: 174 camera-trap locations (2008–2020) for ground-dwelling birds and medium-large mammals; high effort with variable sampling nights.
- Forest specialist filtering: datasets filtered to forest specialist species (per taxon) to control for generalist compensations after disturbance.

## Data quality, validation, and taxonomic standards
- Observer training and consistency in field leadership to assure data quality.
- Outlier checks, data cleaning, and cross-checking with field notes; audio files audited for disruptive noise; exclusion of compromised recordings.
- Species identification guided by standard taxonomic references and expert consultation; Latin nomenclature standardized across datasets.

## Analytical framework
- Spatial analyses:
  - Effect sizes as standardized mean differences (Hedges g), with heteroskedasticity adjustments; multiple comparisons to controls adjusted for non-independence.
  - Hierarchical mixed-effects meta-analysis (random effects for data type, components, observations) to synthesize fire impacts.
  - GLMMs to quantify proportional changes between burn treatments and unburned controls; results expressed as percent change post-hoc.
- Temporal analyses:
  - Time-series partitioned into seasons; occupancy models for biodiversity to account for imperfect detection (multi-species occupancy with random effects and random walks for season-to-season continuity).
  - Covariates include fire regime metrics (frequency, intensity) and spatio-temporal proximity to megafires; two candidate models per time-series: fire properties vs proximity to megafire.
  - Analyses conducted in a Bayesian framework using rstan (hierarchical meta-analysis) and JAGS (GLMMs and occupancy models).
- Data and model outputs:
  - 24 data files (23 data files + metadata) structured to support grouping by forest specialists, input for spatial and temporal analyses, and fire-related covariates.
  - Key files include: MetaAnalysis_Treatment_AllSpecies.csv, MetaAnalysis_Treatment_Specialists.csv, Spatial_GLMMs_AllSpecies.csv, Spatial_GLMMs_Specialists.csv, occupancy detection data, and Temporal_GLMM outputs for litterfall, pH, and phenology, plus covariates.

## Data structure and accessibility
- Data package comprises 24 files:
  - Species groupings: Bird_Groups.csv, Mammal_Groups.csv, SpGroups_Specialists_AllTaxa.csv.
  - Spatial meta-analysis inputs: MetaAnalysis_Treatment_AllSpecies.csv, MetaAnalysis_Treatment_Specialists.csv.
  - Spatial GLMM inputs: Spatial_GLMMs_AllSpecies.csv, Spatial_GLMMs_Specialists.csv.
  - Fire data: MODIS_Central_Kalimantan_Fires.csv, MODIS_Field_research_area_Fire.csv.
  - Occupancy data: OM_Detection_Birds.rds, OM_Detection_Butterflies.csv, OM_Detection_Fish.csv, OM_Detection_Mammals.rds.
  - Occupancy covariates: OM_Covariates_Birds.csv, OM_Covariates_Butterflies.csv, OM_Covariates_Fish.csv, OM_Covariates_Mammals.csv.
  - Temporal GLMM outputs: Temporal_GLMM_Litterfall.csv, Temporal_GLMM_pH.csv, Temporal_GLMM_Phenology.csv.
  - Temporal covariates: Temporal_GLMM_Covariates_Litterfall.csv, Temporal_GLMM_Covariates_pH.csv, Temporal_GLMM_Covariates_Phenology.csv.
  - Metadata document describing each file’s columns and structure.

## Practical implications for environmental monitoring
- Provides a standardized, multi-taxon methodological framework to assess fire impacts on peatland ecosystems over space and time.
- Outputs enable cross-study comparisons through harmonised effect sizes and occupancy trajectories, supporting policy evaluation and restoration planning.
- Emphasises data re-use by storing comprehensive underlying datasets and covariates, facilitating integration with other environmental monitoring datasets.