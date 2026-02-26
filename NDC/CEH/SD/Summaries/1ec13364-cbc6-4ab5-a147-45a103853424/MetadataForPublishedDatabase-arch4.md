# Metadata for published database

## Overview
- Metadata schema and definitions for a drone survey dataset curated by Andrew Cunliffe (generated 2020-06-05).
- Documents the fields used to describe each survey, harvest plot, and ecological context to support data discovery, provenance, and reuse.

## Key metadata fields and their purpose
- Identification and contact
  - survey_code: unique code for each drone survey (date + investigator initials + site code)
  - PlotID: unique id for each harvest plot within a survey
  - email: primary investigator's email
  - Investigators: names of primary investigators responsible for data collection
- Site information
  - SiteName: informal field site name
  - Country: country of sampling
  - SiteLatitude / SiteLongitude: geographic coordinates (WGS84)
  - MAT: mean annual temperature (°C)
  - MAP: mean annual precipitation (mm)
  - CommunityDescription: ecological community context
- Target species and plot details
  - plant_functional_type: plant functional type for the target species
  - PlotOrder: order of the target species within the plot
  - PlotFamily / PlotGenus / PlotSpecies / PlotSubspecies: taxonomic details
  - life_cycle_strategy: perennial, annual, or biennial
- Spatial referencing and geometry
  - EPSG: EPSG code of the UTM CRS
  - UTM_zone: UTM zone
  - Corner1_X/Y/Z ... Corner4_X/Y/Z: coordinates and elevation of each harvest plot corner
  - plot_area_from_coordinates_m2: plot area derived from corner coordinates (m2)
- Biophysical measurements
  - AGB: dry above-ground biomass in g
  - AGB_g_m2: normalized dry above-ground biomass (g/m2)
  - NB note: when used, harvest plot frame area is preferred for calculation
  - HAG_plotmean_of_cellmax_m: mean canopy height within the plot (m)
- Data governance and collaboration
  - Acknowledgements_Funding / Acknowledgements_Permission / Acknowledgements_Assistance: funding, permissions, and assistance sources
- Data collection context
  - Wind_speed: typical wind speed during the survey
  - sky_conditions: sky conditions observed (per Assmann et al., 2018)
  - drone_and_sensor: UAS platform and camera sensor used
  - CameraShutterType: global or rolling shutter
- Additional metadata
  - life_cycle_strategy, plot_area_from_coordinates_m2, and other listed fields provide context for data interpretation and reuse

## Data governance and reuse implications for Data Leaders
- Supports data provenance and audit trails through investigator, contact, and funding/permission fields.
- Facilitates discoverability and interoperability via standardized coordinates, CRS (EPSG/UTM), and taxonomic fields.
- Enables quality assessment by detailing measurement units (°C, mm, g, m) and documented calculation methods (e.g., AGB_g_m2 vs. plot area frames).
- Aids data sharing across networks by describing site-level environmental context (MAT, MAP) and ecological description.

## Observations on data quality, standards, and gaps
- Clear definitions of each field aid consistency and reuse; some fields reference external standards or methods (e.g., sky_conditions per Assmann et al., 2018).
- Lacks explicit data values, validation rules, and versioning information.
- Coordinate-based geometry requires consistent CRS usage (EPSG/UTM) and accurate corner coordinates to ensure plot area calculations.
- Some metadata (e.g., missing values handling, data quality metrics) could be expanded to strengthen governance and interoperability.

## Practical takeaways for implementation and governance
- Use the metadata as a blueprint for dataset cataloging, ensuring each survey and plot is fully described for downstream users.
- Establish standard data validation rules for coordinates, taxonomic fields, and biomass calculations.
- Maintain documentation on calculation methods (e.g., how AGB_g_m2 is derived) and any area assumptions (frames vs. coordinates).
- Ensure data access and permissions are clearly recorded to support responsible data sharing and collaboration.