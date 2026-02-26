# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- A data resource within the Carbon Storage in Intertidal Environments (C-SIDE) project funded by NERC.
- Focuses on physical and geochemical properties of saltmarsh soils from wide-diameter gouge cores collected in Essex, UK (2019).
- Sites represent different saltmarsh origins: natural, historic breach, and managed realignment; all within similar UK environmental regions for comparability.
- Spatial scope centered on Essex coastline with both geographic coordinates (lat/long, WGS84) and projected coordinates (X_easting, Y_northing).

## Data Content
- 19 cores from 8 sites; core diameter 60 mm; samples described and analyzed in the lab.
- Variables observed or simulated include:
  - Location information: Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_above_OD_m
  - Saltmarsh attributes: Saltmarsh name, Marsh_type (Natural, Managed Realignment, Historic Breach)
  - Sediment properties: Substrate (Troels-Smith), Dry_bulk_density_g_cm3, OC_perc (organic carbon content)
  - Sub-sampling details: Sample_depth_cm, Mid_Point_depth_cm
- Data are stored in CSV format (Physical_geochemical_properties_wide_cores_essex.csv).

## Spatial Data and Coordinate Reference
- Location data provided in both decimal degrees (WGS84) and projected coordinates (X_easting, Y_northing).
- Geographical extent defined by four corner coordinates:
  - 52.045333, 1.610887
  - 52.045333, -0.022240
  - 51.459975, 1.610887
  - 51.459975, -0.022240
- Site descriptions indicate coastal Essex locations suitable for cross-site comparisons.

## Methods and Data Quality
- Field sampling: 19 gouge cores collected across 8 sites; cores described during collection.
- Core processing: sliced into 1 cm sections (n = 1952 total segments).
- Laboratory analysis: samples dried at 60°C for 72 hours; carbon quantified via Elementar Soli TOC with temperature-gradient method (DIN 19539); calibration with CaCO3 and soil standards; isotopic QC with high OC sediment standard.
- Location accuracy: DGPS used for site locations; all equipment calibrated per University of St Andrews practices.
- Data quality notes: statistical treatment marked as NA; overall QA mentions calibration and standard procedures.

## Data Resource Structure and Metadata
- Data resource description includes:
  - Core_ID, Saltmarsh, Marsh_type
  - Lat_dec_deg, Long_dec_deg, X_easting, Y_northing
  - Elevation_above_OD_m, Sample_depth_cm, Mid_Point_depth_cm
  - Substrate, Dry_bulk_density_g_cm3, OC_perc
- Header mappings outlined (Description/Cell Format; Core_ID/Text; etc.), ensuring clarity for GIS integration.

## Temporal Scope and References
- Data collected in 2019.
- References supporting methods and context:
  - Dadey et al. (1992) on dry bulk density methods
  - DIN 19539 (2015/08) on TOC differentiation
  - Natali et al. (2020) on soil carbon pool stability
  - Smeaton et al. (2021) on marine sedimentary carbon stocks
  - Troels-Smith (1955) sediment classification

## Practical GIS Considerations
- Suitable for map-based visualisations of OC distribution, soil density, and substrate types across Essex saltmarsh sites.
- Can be integrated with other coastal datasets using consistent CRS (WGS84 lat/long or projected coords).
- Users should note data gaps (NA in statistical treatment) and the need for harmonised data standards when merging with other datasets.
- The dataset supports exploration of relationships between marsh type, depth, and geochemical properties along the Essex coastline.