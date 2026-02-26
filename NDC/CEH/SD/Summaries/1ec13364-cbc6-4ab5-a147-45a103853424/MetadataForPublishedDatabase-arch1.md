# Metadata for published database Andrew Cunliffe <andrewmcunliffe@gmail.com> Generated on 2020-06-05

## Overview
- Metadata schema for a published drone survey biomass dataset.
- Captures identifiers, personnel, site context, environmental conditions, taxonomic details, geometry, measurements, and acknowledgements.
- Emphasizes data provenance, coordinate systems, and calculation specifics to support reproducibility and data integration.

## Key data fields and structure
- Identifiers and contact
  - survey_code: unique survey ID (date code + investigator initials + 3-letter site code)
  - PlotID: unique harvest plot ID within a survey
  - Investigators: primary investigators responsible for data collection
  - email: contact for the dataset
- Site and geographic context
  - SiteName, Country
  - SiteLatitude, SiteLongitude (WGS84)
  - MAT (mean annual temperature), MAP (mean annual precipitation)
  - CommunityDescription: ecological context
- Taxonomy and plant attributes
  - plant_functional_type
  - PlotOrder
  - PlotFamily, PlotGenus, PlotSpecies, PlotSubspecies
  - life_cycle_strategy: perennial, annual, or biennial
- Spatial reference and geometry
  - EPSG, UTM_zone
  - Corner1_X/Y/Z, Corner2_X/Y/Z, Corner3_X/Y/Z, Corner4_X/Y/Z (plot corners in meters, elevations)
  - plot_area_from_coordinates_m2: area calculated from corner coordinates
  - AGB_g_m2: normalised dry above-ground biomass per m2 (note on calculation basis)
  - AGB: total dry above-ground biomass (g)
  - HAG_plotmean_of_cellmax_m: mean canopy height within the harvest plot
- Data quality and methodological context
  - breeze/wind and sky_conditions observed during survey
  - drone_and_sensor, CameraShutterType: UAS platform and imaging specifications
  - Acknowledgements_Funding, Acknowledgements_Permission, Acknowledgements_Assistance
  - NB: When used, plot area from coordinates may be superseded by the harvest-plot-frame area for AGB calculations
- Metadata and dissemination
  - End of report marker indicates completion of metadata record

## Data collection and provenance
- Records the primary investigators, their contact, and affiliated site information to ensure traceability.
- Documents environmental conditions and imaging setup to support reproducibility of biomass measurements.

## Measurements and calculations
- Biomass metrics include AGB (g) and AGB_g_m2 (g per m2), with a note on preferred area basis for calculations.
- Canopy height captured as HAG_plotmean_of_cellmax_m to characterize vertical structure.
- Plot area may be derived from coordinates or from established harvest-plot frame dimensions.

## Spatial and reference details
- Uses EPSG and UTM_zone for spatial referencing.
- Coordinates provided for plot corners to define geometry and area.
- Latitude/Longitude given in WGS84 for site localization.

## Usage considerations for analysts
- Ensure correct alignment of coordinate reference system (EPSG/UTM) when integrating with other datasets.
- Be aware of the NB note on AGB_g_m2 calculation baseline (area basis) when comparing biomass metrics across plots.
- Leverage the contact information and funding/permission fields to assess data provenance and data access constraints.
- Use the documented drone and sensor details to assess compatibility with other remote-sensing datasets.