# Sentinel project bat and bird survey data, 20202023

## Overview
- Datasets from the Sentinel project assessing ecological impacts of agricultural expansion in Ghana and Zambia (Dec 2020–Mar 2023).
- Focus on bat and bird community structure and composition across land-use gradients; includes dietary observations for birds.
- Data organized for GIS use with coordinates, grid/ transect identifiers, and land-cover classifications.

## Study area, aims, and context
- Countries: Ghana (3 localities) and Zambia (5 localities).
- Ghana: Upper Guinean wet evergreen forests near cacao and rubber plantations.
- Zambia: Subtropical climate with dry miombo woodlands and evergreen Cryptocephalum forests near maize and cassava farming.
- Aims: characterize species presence and abundance across land-use types and investigate potential shifts in ecosystem services; part of broader assessment of agricultural expansion impacts.

## Survey methods and spatial scope
- Timeframe: December 2020 – March 2023.
- Sampling design: two-tier stratified random design using a 1 km × 1 km grid over each locality.
- Land-use classification within grid cells:
  - Not Applicable (NA): unsuitable for sampling (e.g., urban).
  - Agriculture Only: >95% agricultural land.
  - Forest edge: 25–75% forest cover.
  - Forest: >95% forest cover.
- Site selection: subset from each category (Agriculture, Forest edge, Forest); some sites later became inaccessible, requiring plan adjustments.
- At each site: random survey points along a transect, ≥200 m apart.
- Birds: 10-minute point counts at dawn within a 50 m radius; recordings of seen/heard species, group counts, and weather/vegetation context.
- Birds (sub-sample): mist nets for understory birds at some sites (nights with specific net configurations and timing).
- Bats: survey at same locations using mist nets and harp traps on separate nights; nets/traps operate around sunset for at least 4 hours with frequent checks.

## Data products and structure
- Data package: Sentinel_survey_data.zip containing two dataframes.
- Dataframe 1: Sentinel_Pointcount_data.csv
  - Bird point-count observations with fields including country, locality, grid, transect, point, site, geographic coordinates (Latitude, Longitude), collection date, observer, start time, species (common and scientific names), counts (under 50 m, over 50 m, total), observation type (heard/seen/both), weather variables (Temp, Cloud.Cover, Wind, Rain), land cover context (Land.Grid, Land.Point, Land.Site), canopy and visibility metrics (MaxCan, MinCan, MeanCan, MaxVis, MeanVis), and tree measurements within 10 m radius (TreeS, TreeM, TreeL, TreeTotal).
- Dataframe 2: Sentinel_Mistnetting_data.csv
  - Bat and bird mist-netting records with fields including country, locality, site, site type (e.g., forest, forest edge, agriculture, riverine, commercial), coordinates, collection date, specimen number, taxonomic class, scientific name, and common name.
- Data quality: missing values denoted as NA.
- Data consolidation: multiple inputters digitized field sheets; dataset was error-checked and validated.

## Data quality and QA considerations
- Data cleaning and transformation required to harmonize records from different inputters.
- Accessibility issues and permissions influenced site selection during surveying.
- Standardized methods and references used to support taxonomy and survey techniques.

## Data usage notes for GIS specialists
- Rich geospatial attributes enable mapping of species distributions across land-use gradients.
- Key GIS-ready fields: lat/long, grid, transect, and land-cover classifications at grid/point/site levels.
- Enables spatial analyses of species richness/abundance by land-use type, canopy/visibility context, and multiscale habitat characteristics.
- Data can be integrated with other spatial layers (e.g., land-use change, vegetation structure) for ecological and ecosystem-services assessments.

## References and methodological grounding
- Field and taxonomic references supporting bird and bat survey techniques and species identifications are listed in the dataset documentation.
- The data collection protocol aligns with standard survey methods for bird census and bat/mammal identification.

## Availability
- The dataset is provided as Sentinel_survey_data.zip, containing the two CSV dataframes described above.