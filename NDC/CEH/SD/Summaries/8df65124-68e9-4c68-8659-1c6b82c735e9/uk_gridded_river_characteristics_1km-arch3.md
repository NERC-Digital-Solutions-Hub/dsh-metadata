# UK gridded physical river characteristics at 1km: Supporting Information

## Overview
- A UKCEH dataset providing consistent 1km × 1km gridded river characteristics for hydrological and inundation modelling on the British National Grid.
- Datasets cover outflow drainage directions, catchment areas, bankfull river widths, bankfull river depths, and NRFA gauging station locations on the 1km grid.
- Derived from a mix of high-resolution data and regression-based estimates, with explicit notes on applicability in GB, NI, and ROI contexts.

## Data components
- Outflow drainage directions (1km, D8 based) and associated catchment areas.
- Bankfull river widths (1km) derived from OS MasterMap Water Network Layer (GB) plus a GB-wide width–catchment–SAAR regression.
- Bankfull river depths (1km) derived from a regression using catchment area and SAAR, calibrated with historic depth measurements.
- NRFA (National River Flow Archive) gauging station locations aligned to the 1km network (1499 stations), with upstream catchment area comparisons and overlap metrics.
- Spatial domain: 656 km × 1220 km on the British National Grid, including GB with Shetland inset and added NI data; tidal extensions included but not representative of estuarine depths.

## Data production methods
- Primary datasets: outflow drainage directions and catchment areas derived from high-resolution data; used to support subsequent width and depth estimation.
- DR directions:
  - Derived via Paz et al. (2006) method and applied by Davies & Bell (2009) from a 50m IHDTM.
  - Manual QA aligns 1km network to 50m IHDTM; D8 scheme with ESRI and Unifhy codings.
- Bankfull river widths:
  - Based on GB OS MasterMap Water Network Layer (WNL) data; select a single best width per 1km cell by comparing WNL-derived catchments to 1km catchment drainage areas.
  - When multiple widths exist, maximum width is chosen to represent the 1km cell and avoid minor tributaries.
  - Regression width equation: RW = 0.00042 × A^0.409 × SAAR^0.86, where A is catchment area (km^2) and SAAR is Standard Average Annual Rainfall (mm, 1961–1990). R^2 = 0.80 (n ≈ 38,600 sites).
  - SAAR gaps imputed from the nearest cells.
- Bankfull river depths:
  - Regression using 90 historical measurements across GB; relates bankfull depth RD to A and SAAR.
  - Depth equation: RD = 0.002643 × A^0.202 × SAAR^0.402. R^2 = 0.57.
  - SAAR gaps imputed as for widths.
- NRFA gauging stations:
  - Locations adjusted on the 1km grid so upstream catchments align with the NRFA station catchments.
  - Includes metrics for catchment area differences and overlap between 50m IHDTM and 1km delineations; NI data have limited overlap statistics due to grid reprojection.
- Quality control:
  - Manual QA and corrections of drainage directions; 1km catchment areas discretisation yields some cells slightly oversized or undersized; median catchment-area mismatch error ~1% for gauging stations; overlap error median ~7%.

## Quality information and limitations
- Spatial discretisation error: approximately 0.5 km; greater in some areas.
- Width/depth regressions have inherent scatter; estimated standard errors ~0.5 m for width and ~0.36 m for depth.
- Estuarine/tidal regions: depths and widths in these areas are not representative of actual tidal rivers.
- NI/ROI limitations: GB-derived relationships used where direct measurements are unavailable; potential biases in non-GB regions.
- Metadata and governance: explicit QA steps described; data provenance and transformation processes are documented, but formal governance metadata (beyond QA notes) is not exhaustively specified.

## Dataset format and access
- NetCDF files:
  - UK_outflow_drainage_directions_1km_ESRI.nc
  - UK_outflow_drainage_directions_1km_Unifhy.nc
  - UK_catchment_areas_1km.nc
  - UK_bankfull_river_widths_1km.nc
  - UK_bankfull_river_depths_1km.nc
- CSV file:
  - NRFA_gauging_station_locations_1km.csv
- Key details:
  - Units: catchment areas in km^2; bankfull widths and depths in metres.
  - Outflow directions use D8; two coding schemes (ESRI and Unifhy).
  - Gauging station file includes OSGB grid references, 1km cell coordinates, catchment-area data, and overlap/error metrics.
  - Domain: 656 × 1220 grid extent on the British National Grid; data extended into tidal regions but caution advised for estuarine interpretation.
- Usage: suitable for configuring hydrological components in gridded land-surface models; ArcGIS-ready and allow custom river masks based on catchment area or other criteria.

## How this supports monitoring frameworks
- Provides a reproducible, nationally scaled set of river characteristics to scrutinise hydrological policy outcomes and inform future decisions.
- Enables transparency through explicit data derivation methods, QA steps, and documentation of uncertainties and limitations.
- Facilitates data-driven decision-making by offering consistent inputs for models, with clear indicators of data gaps (e.g., NI/ROI coverage via GB-derived relationships) and potential discretisation errors.

## Acknowledgements
- Supported by NERC grants NE/S017380/1 (Hydro-JULES) and NE/R016429/1 (UK-SCAPE).
- Contributions acknowledged from Oliver Robertson; key references include methods for extracting river networks and hydrological digital terrain modeling.