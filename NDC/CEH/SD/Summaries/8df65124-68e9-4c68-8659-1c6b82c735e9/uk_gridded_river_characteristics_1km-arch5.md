# UK gridded physical river characteristics at 1km: Supporting Information

## Overview
- UKCEH dataset providing a consistent 1km × 1km gridded suite for hydrological and inundation modelling on the British National Grid.
- Products include: outflow drainage directions, catchment areas, bankfull river widths, bankfull river depths, and NRFA gauging station locations on the 1km grid.
- Data derived from high-resolution inputs with regression relationships used to estimate GB-wide values for national coverage.

## Data production and methods
- Outflow drainage directions and catchment areas
  - Derived from high-resolution data (50m IHDTM) and corrected via manual QA against the 50m river network.
  - D8 method with eight directions; ESRI and Unifhy coding schemes provided.
  - Catchment area represents upstream 1km cells draining to each cell, including the cell itself.

- Bankfull river widths
  - Derived from OS MasterMap Water Network Layer (GB) widths and a GB-wide regression linking width to catchment area and rainfall.
  - Regression: RW = 0.0042 × A^0.409 × SAAR^0.86; SAAR is 1961–1990 rainfall; R^2 ≈ 0.80.
  - For NI and some Irish sub-catchments, GB relationships are applied; missing SAAR values imputed from nearest cells.
  - Anomalies possible; width estimates cross-validated with OS data.

- Bankfull river depths
  - Regression-based estimates using ~90 historical depth measurements across GB.
  - Regression: RD = 0.02643 × A^0.202 × SAAR^0.402; R^2 ≈ 0.57.
  - SAAR gaps filled from nearest cells; larger rivers show greater scatter due to measurement challenges.

- NRFA river flow gauging station locations on the 1km network
  - Links 1499 NRFA stations to the nearest suitable 1km grid location; adjustments minimize upstream area mismatch.
  - Outputs include: OSGB reference, grid row/column, 1km and IHDTM catchment areas, percentage errors in catchment area and catchment overlap.
  - NI stations have catchment overlap statistics unavailable due to grid reprojection.

## Datasets and formats
- File formats
  - NetCDF: UK_outflow_drainage_directions_1km_ESRI.nc, UK_outflow_drainage_directions_1km_Unifhy.nc, UK_catchment_areas_1km.nc, UK_bankfull_river_widths_1km.nc, UK_bankfull_river_depths_1km.nc
  - CSV: NRFA_gauging_station_locations_1km.csv
- Units
  - Catchment area: square kilometres (km^2)
  - Bankfull widths and depths: metres (m)
- Domain and coverage
  - 656 km × 1220 km UK land domain on the British National Grid
  - Includes GB with added cells for Shetland and select inland gaps; NI covered via OSNI grid references
  - Estuary and tidal regions extended for continuity but not representative of true tidal river values

## Quality and uncertainty
- Spatial discretisation error: approximately 0.5 km; some areas more affected.
- Outflow directions: QA’d visually against 50m IHDTM; manual corrections applied as needed.
- Catchment delineation: 1km discretisation cannot represent fractional cell boundaries; NRFA overlap/area differences provided to gauge accuracy (median catchment overlap error around 7%).
- Bankfull width/depth: regression-based estimates show scatter; typical standard errors ~0.5 m for width and ~0.36 m for depth.
- Notes on limitations: estuarine areas may be underestimated; dataset designed for model configuration rather than precise in-water measurements.

## How to use the data
- Suitable for configuring hydrological components of gridded land surface and hydrological models.
- All datasets cover UK land points; users can apply their own masks to delineate rivers (e.g., catchments > threshold).
- Data can be read directly into ArcGIS to generate 1km river networks; estuarine values should be treated cautiously.
- Spatial datasets extend into tidal regions; caution with interpretation in estuaries.

## Acknowledgements
- Support from Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.
- Additional support from NE/R016429/1 as part of the UK-SCAPE programme.

## References (key)
- Davies, H. & Bell, V. (2009); Jenson & Domingue (1988); Morris & Flavin (1990)
- Naden & McCartney (1991); Nixon (1959)