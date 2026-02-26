# Metadata for published database Andrew Cunliffe <andrewmcunliffe@gmail.com> Generated on 2020-06-05

## Scope and purpose
- Metadata describing a drone survey dataset to support discovery, mapping, and reuse in GIS.
- Distinguishes fields at two levels: survey-level identifiers and harvest plot-level attributes.
- Enables integration of data across plots and surveys, with provenance, data collectors, and funding/permissions documented.

## Key fields and data model
- survey_code: unique ID for each drone survey (date code YYYYMMDD + investigator initials + three-letter site code).
- PlotID: unique ID for each harvest plot within a survey.
- email, Investigators: contact and responsible individuals for the dataset.
- SiteName, Country: descriptive site information.
- SiteLatitude, SiteLongitude: site position in decimal degrees (WGS84).
- MAT, MAP: mean annual temperature (°C) and mean annual precipitation (mm).
- CommunityDescription: ecological description of the site.
- plant_functional_type: functional type of the target species.
- PlotOrder: order of the target species within the harvest plot.
- PlotFamily, PlotGenus, PlotSpecies, PlotSubspecies: taxonomic details.
- life_cycle_strategy: perennial, annual, or biennial life strategy.
- EPSG, UTM_zone: coordinate reference system identifiers.
- Corner1_X/Y/Z, Corner2_X/Y/Z, Corner3_X/Y/Z, Corner4_X/Y/Z: harvest plot corners in meters (easting, northing, elevation).
- AGB: dry above-ground biomass (g).
- AGB_g_m2: normalised above-ground biomass per square meter.
- plot_area_from_coordinates_m2: plot area derived from corner coordinates (with NB note).
- HAG_plotmean_of_cellmax_m: mean canopy height within the plot (m).
- Acknowledgements_Funding, Acknowledgements_Permission, Acknowledgements_Assistance: governance and support details.
- Wind_speed: typical wind speed observed during the survey.
- sky_conditions: sky conditions during the survey.
- drone_and_sensor: UAS platform and camera sensor used.
- CameraShutterType: shutter type (global or rolling).
- END OF REPORT: document terminator.

## Spatial, environmental, and technical context
- Spatial coordinates provided at both site level (lat/long) and plot level (UTM-based corner coordinates), with an EPSG and UTM zone specified to support GIS interoperability.
- Environmental context includes MAT, MAP, wind, and sky conditions.
- Technical metadata includes drone platform, sensor, and imaging parameters relevant to GIS analyses.

## Data standards and interpretation notes
- Use of EPSG and UTM zone facilitates accurate GIS projection and reprojection.
- Plot area can be calculated from coordinates or used from predefined plot frames; NB clarifies preference when both are available.
- Units are stated for biomass (g), area (m2), canopy height (m), temperature (°C), and precipitation (mm).

## Provenance, access, and attribution
- Investigators, email contact, and site information provide traceability.
- Acknowledgements_Funding, Acknowledgements_Permission, and Acknowledgements_Assistance document supporting actors and permissions.
- Clear documentation ends with END OF REPORT.