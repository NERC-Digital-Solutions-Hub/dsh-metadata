# Metadata for published database Andrew Cunliffe

## Overview
- Metadata record describing a drone survey dataset by Andrew Cunliffe (generated 2020-06-05).
- Documents structured variables used to understand, reproduce, and reuse the dataset, covering identification, location, climate, ecology, plot geometry, biomass measurements, drone details, and acknowledgments.
- Aims to enable data discovery, quality assessment, and integration into data products for exploration and analysis.

## Identification and Contact Information
- survey_code: Unique ID encoding survey date, investigator initials, and site code (YYYYMMDD + initials + site code).
- PlotID: Unique harvest plot identifier within a survey.
- email: Primary investigator's email.
- Investigators: Names of investigators responsible for data collection.

## Location, Site Context, and Climate
- SiteName: Informal field-site name.
- Country: Country of sampling.
- SiteLatitude / SiteLongitude: Site coordinates in decimal degrees (WGS84).
- MAT: Mean annual temperature (°C).
- MAP: Mean annual precipitation (mm).
- CommunityDescription: General ecological community description at the site.

## Biological and Plot Data
- plant_functional_type: Target species’ plant functional type within the harvest plot.
- PlotOrder: Order of the target species within the harvest plot.
- PlotFamily / PlotGenus / PlotSpecies / PlotSubspecies: Taxonomic details of the target species.
- life_cycle_strategy: Life strategy (perennial, annual, biennial) of the target species in the plot.

## Geospatial, Geometry, and Plot Specifications
- EPSG: EPSG code for the coordinate reference system.
- UTM_zone: UTM zone for the CRS.
- Corner1_X/Y/Z, Corner2_X/Y/Z, Corner3_X/Y/Z, Corner4_X/Y/Z: Eastings, Northings, and Elevations of each harvest plot corner in meters.
- plot_area_from_coordinates_m2: Plot area derived from corner coordinates (m²).
- AGB (g): Dry above-ground biomass for the plot in grams (total).
- AGB_g_m2: Normalized dry above-ground biomass per square meter (g/m²); NB indicates when area of harvest frame is used instead of coordinate-derived area.
- HAG_plotmean_of_cellmax_m: Mean canopy height within the harvest plot (m).

## Data Collection, Processing, and Outputs
- Acknowledgements_Funding / Acknowledgements_Permission / Acknowledgements_Assistance: Funding sources, permissions, and individuals who assisted with data collection.
- Wind_speed: Typical wind speed observed during the survey.
- sky_conditions: Sky conditions during the survey (per Assmann et al., 2018).
- drone_and_sensor: Drone platform and camera sensor used.
- CameraShutterType: Shutter type (global or rolling) of the camera sensor.

## Data Products and Usage Considerations
- The dataset provides both raw and derived fields (e.g., AGB, AGB_g_m2, plot area) to support analysis and the creation of self-serve data products.
- Coordination and consistency notes:
  - Coordinate-based plot area may differ from frame-based area; NB indicates preference for area from harvest frames when available.
  - Standardized fields (CRS, units) facilitate data integration and reuse in dashboards or reports.
- The metadata supports provenance, reproducibility, and potential cross-site comparisons by detailing survey, site, biological, and methodological attributes.

## Access, Reuse, and End Note
- END OF REPORT: Indicates the metadata document concludes with the above fields and descriptions.