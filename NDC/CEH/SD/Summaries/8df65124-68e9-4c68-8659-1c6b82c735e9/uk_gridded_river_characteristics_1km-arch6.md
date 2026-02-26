# UK gridded physical river characteristics at 1km: Supporting Information

- A UKCEH dataset providing a consistent set of 1km × 1km gridded river characteristics for hydrological and inundation modelling on the British National Grid.
- Components include: outflow drainage directions, catchment areas, bankfull river widths, bankfull river depths, and NRFA gauging station locations on the 1km grid.

## What is included
- Outflow drainage directions (D8) at 1km resolution (two numbering schemes: ESRI and Unifhy).
- Catchment areas in square kilometres derived from drainage directions.
- Bankfull river widths (metres) on a 1km grid.
- Bankfull river depths (metres) on a 1km grid.
- NRFA river gauging station locations linked to the 1km grid (NRFA_gauging_station_locations_1km.csv).

## How each variable is produced
- Outflow drainage directions and catchment areas
  - Derived from high-resolution data (50m IHDTM) with the D8 method.
  - Manual QA corrections compared to the 50m network to ensure alignment near gauging stations.
  - Catchment area is the count of upstream 1km cells draining to each cell (includes the cell itself).
- Bankfull river widths
  - Based on OS MasterMap Water Network Layer (WNL) widths for Great Britain.
  - For each 1km cell, select a representative WNL width by comparing 50m IHDTM catchment area to the 1km catchment area; when multiple widths exist, use the maximum to avoid minor tributaries.
  - Use a GB-wide power-law regression to derive 1km widths for all UK cells:
    RW = 0.0042 * A^0.409 * SAAR^0.86
    - A: catchment area (km^2)
    - SAAR: Standard Average Annual Rainfall (mm, 1961–1990)
  - SAAR gaps filled with the mean of the nearest cells.
  - Regression fit: R^2 = 0.80 (based on 38,600 sites).
- Bankfull river depths
  - Based on regression using 90 historical depth measurements across GB.
  - Regression form: RD = 0.02643 * A^0.202 * SAAR^0.402
  - SAAR gaps filled as above.
  - Regression fit: R^2 = 0.57 (notable scatter, especially for larger rivers).
- Northern Ireland and ROI
  - GB-derived relationships are applied to NI and ROI sub-catchments where direct observations are sparse or unavailable.
- NRFA gauging stations on the 1km grid
  - 1499 NRFA stations linked to the most appropriate 1km grid cell(s) by aligning upstream catchments with the 1km network.
  - NRFA_gauging_station_locations_1km.csv provides:
    - OSGB grid reference, column/row, 1km catchment area, IHDTM catchment area, percentage error in catchment, overlap area, and percentage overlap error.
  - NI stations have catchment overlap statistics unavailable due to reprojection issues.

## Data quality and limitations
- Spatial discretisation error around 0.5 km (varies by area).
- Manual QA applied to drainage directions; some corrections near gauging stations.
- Catchment delineation in 1km cells is coarse; some cells may be too large or too small.
- NRFA catchment overlap errors range with a median around 7% but can be higher (0.8–44% typical).
- Bankfull width/depth estimates have associated uncertainty:
  - Widths: approximate standard error ~0.5 m.
  - Depths: approximate standard error ~0.36 m.
- Estuary/tidal areas: datasets extend into tidal regions, but river depth/width values in estuaries are not representative of tidal conditions.

## Dataset formats and domain
- Gridded data: NetCDF files
  - UK_outflow_drainage_directions_1km_ESRI.nc
  - UK_outflow_drainage_directions_1km_Unifhy.nc
  - UK_catchment_areas_1km.nc
  - UK_bankfull_river_widths_1km.nc
  - UK_bankfull_river_depths_1km.nc
- NRFA gauging stations: CSV
  - NRFA_gauging_station_locations_1km.csv
- Domain: 656 km × 1,220 km on the British National Grid (0,0) to (656000,1220000) metres
- Masks: CHESS land mask for GB (with some added cells) and OSNI for NI
- Practical note: values are suitable for configuring hydrological components in gridded land-surface models; users can apply their own masks (e.g., catchment-area-based river masks).

## How to use
- Read into GIS/analysis environments (e.g., ArcGIS) to generate 1km UK river networks for analysis or visualization.
- Use as input for hydrological model components; be mindful of estuarine limitations where depth/width are not representative.
- The NRFA_gauging_station_locations_1km.csv file helps align gauging data with the 1km network and assess catchment delineation accuracy.

## Acknowledgements and references
- Supported by NERC Hydro-JULES (NE/S017380/1) and UK-SCAPE (NE/R016429/1).
- Related references include methods for extracting river networks from digital data and early hydrological terrain models (Paz et al. 2006; Jenson & Domingue 1988; Morris & Flavin 1990; Naden & McCartney 1991; Nixon 1959).