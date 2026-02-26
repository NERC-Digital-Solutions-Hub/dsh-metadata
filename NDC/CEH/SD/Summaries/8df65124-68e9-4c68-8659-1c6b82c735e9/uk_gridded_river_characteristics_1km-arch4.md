# UK gridded physical river characteristics at 1km: Supporting Information

- Purpose: Provides a consistent set of 1km × 1km gridded UK river characteristics for hydrological and inundation modelling on the British National Grid.
- Contents: Four gridded datasets (outflow drainage directions, catchment areas, bankfull river widths, bankfull river depths) plus an accompanying NRFA gauging station locations table on the 1km grid.
- Data sources: Derived from high-resolution data and historical measurements; uses regression-based estimates to produce nationwide coverage.

## Datasets included
- Outflow drainage directions (1km ESRI and 1km Unifhy)
- Catchment areas (1km)
- Bankfull river widths (1km)
- Bankfull river depths (1km)
- NRFA gauging station locations on the 1km river network (CSV)

## Data production and methodology
- Primary datasets and workflow:
  - Outflow drainage directions and catchment areas are treated as primary datasets; bankfull widths and depths are derived via regression relationships.
  - High-resolution data estimate outflow directions and catchment areas; power-law relationships are used to estimate bankfull widths and depths for all UK land cells.
- Spatial domain and coverage:
  - 656 km × 1220 km domain on the British National Grid; covers GB and Northern Ireland with some Republic of Ireland flow-into-NI areas approximated.
- Key relationships:
  - Bankfull width RW derived from: RW = 0.0042 × A^0.409 × SAAR^0.86, where A is catchment area (km²) and SAAR is Standard Average Annual Rainfall (mm, 1961–1990).
  - Bankfull depth RD derived from: RD = 0.02643 × A^0.202 × SAAR^0.402.
- Data sources for widths/depths:
  - Widths: OS MasterMap Water Network Layer (GB) used to inform a GB-wide regression fit.
  - Depths: historical measurements from multiple sources (Naden & McCartney 1991; Nixon 1959; NRFA; EA cross-sections).
- Special notes:
  - SAAR values missing for some coastal cells are infilled with the nearest-neighbour mean.
  - GB-derived relationships are assumed to apply to NI and some ROI catchments where direct observations are scarce.

## Outflow drainage directions and catchment area
- Drainage direction: D8 method with eight directions; two coding schemes provided (ESRI and Unifhy).
- Corrections: manual QA via visual comparison against 50m IHDTM river network; adjustments near gauging stations.
- Catchment areas: derived from drainage directions and represent the number of upstream 1km cells draining to each cell (including the cell itself).

## Bankfull river widths
- Derived from regression using OS MasterMap widths and catchment characteristics; width in metres on 1km grid.
- Selection process: choose best OS MasterMap width per 1km cell by comparing 50m IHDTM-derived catchment area to the 1km catchment area; when multiple widths exist, the maximum width is used to avoid including minor tributaries.
- Coverage: GB-derived regression applied UK-wide; coastal SAAR gaps infilled from nearest cells.
- Validation: RW estimates show good overall agreement with OS MasterMap data, but with scatter due to local variations.

## Bankfull river depths
- Derived using a regression similar to width, based on 90 historical depth measurements across catchment sizes (16–9868 km²) and varying SAAR.
- Depths in metres on the 1km grid; SAAR gaps infilled by nearest-neighbour mean.
- Validation: moderate fit (R² ≈ 0.57) with noticeable scatter, especially at larger depths.

## NRFA River flow gauging station locations on the 1km network
- NRFA provides daily, monthly, and flood-peak data from ~1500 stations.
- Location mapping: an accompanying NRFA_gauging_station_locations_1km.csv links 1km grid cells to the most appropriate upstream NRFA gauging station locations by minimizing catchment-area differences.
- Contents: OSGB grid reference, 1km grid column/row, 1km and IHDTM catchment areas, percentage errors in catchment overlap, and overlap metrics.
- NI caveat: catchment overlap statistics not available for some NI stations due to grid reprojection differences.

## Quality information
- Spatial discretisation error: expected around 0.5 km; some areas may be higher.
- QA: manual corrections for outflow directions; catchment areas are discrete at 1km resolution (no fractional cell delineation).
- Gauging station overlap: median catchment overlap error around 7%, with a typical range 0.8–44%.
- Width/depth uncertainty: regression-derived values have plausible errors (bankfull width ~0.5 m; bankfull depth ~0.36 m) due to scatter and data limitations.

## Dataset format and file naming
- Grid datasets: NetCDF format
  - UK_outflow_drainage_directions_1km_ESRI.nc
  - UK_outflow_drainage_directions_1km_Unifhy.nc
  - UK_catchment_areas_1km.nc
  - UK_bankfull_river_widths_1km.nc
  - UK_bankfull_river_depths_1km.nc
- Gauging stations: NRFA_gauging_station_locations_1km.csv
- Domain: 0 to 656000 (E), 0 to 1220000 (N) on the British National Grid (in metres)
- Land mask: CHESS GB mask with additional cells; NI uses OSNI mask with extra NI-flow cells
- Notes: Tidal regions extended for coverage, but estuary values are not representative of real tidal channels

## How to use the data
- Applications: Configuring hydrological components of gridded land-surface and hydrological models; read directly into ArcGIS for 1km UK river networks.
- User responsibilities:
  - Apply your own mask to delineate rivers based on catchment area or other observations.
  - Be cautious with estuarine/tidal regions where bankfull estimates are not representative.
- Availability across the UK: All 1km cells across the domain have values; covered areas include GB and NI with some ROI approximations.

## Acknowledgements
- Funding and project context: Hydro-JULES (NERC NE/S017380/1) and UK-SCAPE (NERC NE/R016429/1).
- Collaborative contributors and related methodological references cited for drainage direction extraction and digital terrain modelling.

## References (selected)
- Davies, H. & Bell, V. (2009); Jenson & Domingue (1988); Morris & Flavin (1990)
- Naden & McCartney (1991); Nixon (1959)