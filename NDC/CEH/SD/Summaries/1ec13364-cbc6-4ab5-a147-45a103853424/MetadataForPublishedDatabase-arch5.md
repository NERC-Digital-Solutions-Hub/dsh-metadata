# Metadata for published database Andrew Cunliffe

## Summary
- Defines the metadata fields and structure used to describe a drone-based biomass survey dataset, including identification, location, environmental context, biological target details, spatial references, measurements, observational metadata, and acknowledgements.

## Key metadata fields

- Identification and contact
  - survey_code: unique ID for each drone survey (date code YYYYMMDD + investigator initials + three-letter site code)
  - PlotID: unique ID for each harvest plot within a survey
  - email: email of the primary investigator responsible for the dataset
  - Investigators: names of primary investigators responsible for collecting the dataset

- Site and environmental context
  - SiteName: informal field-site name
  - Country: country of sampling
  - SiteLatitude: latitude (decimal degrees, WGS84)
  - SiteLongitude: longitude (decimal degrees, WGS84)
  - MAT: mean annual temperature (°C)
  - MAP: mean annual precipitation (mm)
  - CommunityDescription: general ecological community description at the site

- Target species and plot identity
  - plant_functional_type: plant functional type of the target species within the harvest plot
  - PlotOrder: order of the target species within the harvest plot
  - PlotFamily: family of the target species
  - PlotGenus: genus of the target species
  - PlotSpecies: species of the target species
  - PlotSubspecies: subspecies of the target species
  - life_cycle_strategy: life strategy (perennial, annual, biennial)

- Geospatial reference
  - EPSG: EPSG code of the UTM coordinate reference system
  - UTM_zone: UTM zone of the CRS
  - Corner1_X/Y/Z, Corner2_X/Y/Z, Corner3_X/Y/Z, Corner4_X/Y/Z: coordinates (Eastings/Northings/Elevation) of the harvest plot corners in meters

- Biomass and canopy measurements
  - AGB: dry mass of above-ground biomass in grams
  - AGB_g_m2: dry aboveground biomass normalized to g per m^2 (note: plot area from coordinates preferred when available)
  - HAG_plotmean_of_cellmax_m: mean canopy height within the harvest plot (m)

- Observational and methodological metadata
  - Wind_speed: typical wind speed observed during the survey
  - sky_conditions: sky conditions during the survey
  - drone_and_sensor: UAS platform and camera sensor used
  - CameraShutterType: shutter type (global or rolling)

- Plot geometry and area
  - plot_area_from_coordinates_m2: plot area calculated from corner coordinates (m^2)

- Acknowledgements and permissions
  - Acknowledgements_Funding: funding sources for data collection
  - Acknowledgements_Permission: entities granting permission for data collection
  - Acknowledgements_Assistance: people who assisted with data collection

## Data governance and standards notes
- Field definitions emphasize standardized naming, units, and geospatial references (WGS84, EPSG, UTM) to support data discovery, interoperability, and reuse.
- Metadata captures both ecological context and technical details necessary for validation, replication, and downstream analyses.

## Practical implications for Data Stewards
- Use these definitions to validate submissions for completeness and consistency.
- Ensure accurate geospatial references (EPSG, UTM_zone, corner coordinates) and unit reporting.
- Verify contact and investigators information for appropriate authorship and responsibility.
- Maintain provenance and acknowledgement records to support attribution and permissions.