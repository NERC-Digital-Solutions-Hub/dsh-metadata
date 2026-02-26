# Sentinel project bat and bird survey data, 20202023

## Overview
- Part of the Social and Environmental Trade-Offs in African Agriculture (Sentinel) project, funded by UK Research and Innovation via the Global Challenges Research Fund.
- Aim: assess ecological impacts of agricultural expansion in Ghana and Zambia by analyzing bat and bird community structure and composition along land-use gradients; also investigate dietary habits to understand potential shifts in ecosystem services.

## Study locations and period
- Data collection: December 2020 to March 2023.
- Ghana: 3 localities within the Upper Guinean wet evergreen forests, surrounded by cacao and rubber plantations.
- Zambia: 5 localities with subtropical climate, including dry miombo woodlands and evergreen Cryptocephalum forests, surrounded by maize and cassava cultivation.

## Sampling design
- Two-tier stratified random design within each locality:
  - Start with a 1 km × 1 km grid to define potential study areas.
  - Classify grid cells into five land-use categories: NA (not applicable), Agriculture Only, Forest edge, Forest.
  - A subset of sites from Agriculture, Forest edge, and Forest categories were sampled; some sites later became inaccessible and had plan adjustments.
- Within each site:
  - Survey points randomly selected along transects, at least 200 m apart.
  - Birds surveyed using standardized point counts at dawn for ~3 hours per site.
  - A subset of sites used mist nets to sample understory birds.
  - Bats surveyed at the same locations using mist nets and harp traps on separate nights; nets operated from sunset for a minimum of 4 hours, with regular checks.

## Survey methods

- Birds
  - Point counts: 10-minute counts within a 50 m radius; observers note whether birds are seen or heard, estimate numbers, identify to species, and record whether perched or flying; additional detections beyond 50 m recorded separately.
  - Pre-count quiet period (~1 minute) to reduce disturbance; weather and vegetation conditions recorded at each point.
  - Mist netting at a subset of sites: 180 m of net lanes, four 30 mm mesh nets (6–18 m), netting conducted 5:30–10:00 with flexibility for weather; birds netted and identified to species, sexed/aged where possible, briefly handled and released.
- Bats
  - Surveyed at the same sites used for bird mist netting.
  - Equipment: mist nets and harp traps; nets/ traps deployed for nights with checks every 15–30 minutes.
  - Identification guided by regional references; bats captured are identified to species, then released.

## Data description and structure
- Data package: Sentinel_survey_data.zip, containing two dataframes.
  - Sentinel_Pointcount_data.csv: Bird point-count observations per 10-minute interval.
  - Sentinel_Mistnetting_data.csv: Mist netting records for bats and birds.
- Missing data are designated as NA.
- Bird point-count dataframe includes:
  - Location and timing: Country, Locality, Grid, Transect, Point, Site, Latitude, Longitude, Collection.date, Time.Started, Observer.Initials.
  - Species observations: Common.name, Species.name; counts (Perch.Under.50m, Flyover.Under.50m, Total.Under.50m, Over.50m, Total); Observation.Type; weather and habitat covariates (Temp, Cloud.Cover, Wind, Rain; Land.Grid, Land.Point, Land.Site).
  - Habitat and structural context: MaxCan, MinCan, MeanCan; MaxVis, MeanVis; TreeS, TreeM, TreeL, TreeTotal.
- Mist netting dataframe includes:
  - Location and timing: Country, Locality, Site, Site.type, Latitude, Longitude, Collection.date.
  - Specimen information: Specimen.number, Class; Scientific.name, Common.name.
- Data fields align with standard bird survey and mist-netting variables and include references for taxonomic and methodological context.

## Data quality and provenance
- Data consolidated by multiple inputters; dataset cleaned, validated, and error-checked.
- Metadata support traceability and discoverability, with clear documentation of variable meanings and data collection methods.

## Potential analyses and applications
- Compare bird and bat species richness and community composition across land-use categories (Agriculture, Forest edge, Forest).
- Model relationships between land-cover attributes (Land.Grid/Point/Site), canopy height, visibility, and detection rates.
- Examine temporal patterns and weather covariates (Temp, Cloud.Cover, Wind, Rain) on detectability and activity.
- Explore dietary insights and species-level patterns from bat and bird community data to assess ecosystem service implications.
- Spatial analyses across locality grids to identify hotspots and gradients of biodiversity in relation to agricultural expansion.