# Metadata for published database

## Overview
- Describes the metadata schema for a drone survey dataset, enabling traceability, re-use, and data governance.
- Captures identifiers, site context, ecological details, spatial geometry, sensor/collection methods, and acknowledgments.

## Key metadata elements

- Identifiers and contact
  - survey_code: Unique ID for each drone survey (YYYYMMDD date code + investigator initials + three-letter site code)
  - PlotID: Unique ID for each harvest plot within a survey
  - email: Primary investigator's email
  - Investigators: Names of primary investigators responsible for data collection

- Site and geographic context
  - SiteName: Informal field site name
  - Country: Sampling country
  - SiteLatitude / SiteLongitude: Study site coordinates (WGS84)
  - MAT: Mean annual temperature (°C)
  - MAP: Mean annual precipitation (mm)
  - CommunityDescription: Ecological community description at the site

- Biological and ecological data
  - plant_functional_type: Target species’ plant functional type
  - PlotOrder: Order of the target species within the harvest plot
  - PlotFamily / PlotGenus / PlotSpecies / PlotSubspecies: Taxonomic details of the target species
  - life_cycle_strategy: Life cycle (perennial, annual, biennial)
  - AGB: Dry above-ground biomass (g)
  - AGB_g_m2: Normalised dry above-ground biomass (g per m2)

- Spatial data and plot geometry
  - EPSG: EPSG code of the UTM CRS
  - UTM_zone: UTM zone of the CRS
  - Corner1_X/Y/Z … Corner4_X/Y/Z: Coordinates (Eastings, Northings, Elevation) of each plot corner
  - plot_area_from_coordinates_m2: Plot area derived from corner coordinates
  - Note: AGB_g_m2 may be used in preference to plot_area_from_coordinates_m2 when calculating biomass per area

- Sensor, collection methods, and environmental conditions
  - wind_speed: Typical wind speed during the survey
  - sky_conditions: Sky conditions during the survey
  - drone_and_sensor: Unmanned aerial system platform and camera sensor used
  - CameraShutterType: Shutter type (global or rolling)

- Data products and quality indicators
  - HAG_plotmean_of_cellmax_m: Mean canopy height within the harvest plot
  - AGB (and AGB_g_m2) provide biomass metrics derived from sensor data or field measurements

- Governance, acknowledgments, and permissions
  - Acknowledgements_Funding: Funding sources
  - Acknowledgements_Permission: Permissions granted for data collection
  - Acknowledgements_Assistance: Individuals who assisted with data collection

## Data structure and interoperability
- Metadata fields collectively enable data discovery, provenance, and interoperability across studies.
- Standardized identifiers, precise spatial and environmental context, and detailing of methods support quality assurance and reproducibility.

## Relevance to monitoring frameworks
- Provides a concrete example of comprehensive metadata needed to evaluate and monitor environmental health datasets.
- Helps address common governance challenges by ensuring data availability, traceability, and clear data provenance in monitoring workflows.