# UK gridded physical river characteristics at 1km: Supporting Information

## Data contents
- A consistent set of 1km × 1km resolution UK gridded datasets for hydrological and inundation modelling, including:
  - Outflow drainage directions
  - Catchment areas
  - Bankfull river widths
  - Bankfull river depths
  - NRFA (National River Flow Archive) gauging station locations aligned to the 1km grid
- NRFA gauging station locations provided as a CSV linking each gauging station to the most suitable 1km river network cell, with upstream catchment area and overlap metrics

## Data production methods
- Primary datasets (outflow drainage directions and catchment areas) are derived from high-resolution data; bankfull widths and depths are estimated for all UK land cells using regression relationships
- Bankfull river widths (RW) derived from OS MasterMap Water Network Layer widths and a UK-wide regression:
  - RW = 0.0042 × A^0.409 × SAAR^0.86
  - A = catchment area (km²), SAAR = Standard Average Annual Rainfall (mm)
  - Regression fit: R² ≈ 0.80 (based on ~38,600 sites)
- Bankfull river depths (RD) estimated from a regression using catchment area and SAAR:
  - RD = 0.02643 × A^0.202 × SAAR^0.402
  - Regression fit: R² ≈ 0.57 (based on 90 measurements)
- Outflow drainage directions use the D8 method with two coding schemes (ESRI and Unifhy/HydroJULES)
- Catchment area for each 1km cell represents the number of upstream 1km cells draining to that cell (including the cell)
- GB-derived relationships are applied to NI and some ROIs, due to data gaps (assumes GB relationships hold elsewhere)

## NRFA gauging stations locations on the 1km grid
- 1,499 NRFA gauging stations linked to the most appropriate 1km grid cell
- Location selection process minimizes upstream catchment area differences between IHDTM and 1km delineations
- Provides: OSGB grid reference, grid column/row, 1km catchment area, IHDTM catchment area, and error metrics for catchment area and overlap
- Note: For Northern Ireland stations, catchment overlap statistics are not available due to reprojection issues

## Data quality and uncertainty
- Spatial discretisation error: approx. 0.5 km across the UK
- Outflow drainage directions: QA by visual inspection against high-resolution IHDTM network
- Catchment-area delineation: 1km representations cannot fractionally split catchments; typical errors are discussed via the gauging station overlap metrics (median overlap error ~7%, range 0.8%–44%)
- Bankfull width: regression-based estimates show scatter around observed values; typical standard error around 0.5 m
- Bankfull depth: regression-based estimates with notable scatter, especially at larger depths; typical standard error around 0.36 m
- Overall, the datasets are designed to provide national-scale values with explicit error and QA notes, suitable for model configuration and sensitivity analyses

## Dataset formats and access
- 1km × 1km datasets stored in NetCDF:
  - UK_outflow_drainage_directions_1km_ESRI.nc
  - UK_outflow_drainage_directions_1km_Unifhy.nc
  - UK_catchment_areas_1km.nc
  - UK_bankfull_river_widths_1km.nc
  - UK_bankfull_river_depths_1km.nc
- NRFA gauging station locations stored as CSV:
  - NRFA_gauging_station_locations_1km.csv
- Domain and grid details:
  - 1km grid over a 656 km × 1220 km area on the British National Grid (0,0) to (656000,1220000) meters
  - Includes GB with added cells for Shetland and NI-related flow, referencing the CHESS land mask and OSNI data for NI
- Data are designed for direct use in hydrological models and can be read into ArcGIS to generate river networks

## How to use the data
- Use for configuring hydrological components of gridded land-surface models and hydrological models
- Apply a user-defined mask to delineate rivers (e.g., grids with catchment area > 20 km²)
- Exercise caution in tidal/estuarine regions: depth and width values in these areas are not representative of actual tidal rivers
- The NRFA gauging station table helps align observed gauge data with the 1km network for validation and model evaluation

## Acknowledgements and references
- Funded by the Natural Environment Research Council (NE/S017380/1) Hydro-JULES programme and NE/R016429/1 UK-SCAPE programme
- Acknowledges contributions from Oliver Robertson
- Key references include methods for extracting river networks from digital elevation data and historical river depth measurements (Paz et al. 2006; Jenson & Domingue 1988; Morris & Flavin 1990; Naden & McCartney 1991; Nixon 1959)