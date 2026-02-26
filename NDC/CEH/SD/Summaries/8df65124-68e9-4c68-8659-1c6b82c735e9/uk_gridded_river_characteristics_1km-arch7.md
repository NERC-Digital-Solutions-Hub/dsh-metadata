# UK gridded physical river characteristics at 1km: Supporting Information

- Brief summary of the dataset
  - UKCEH provides a consistent set of 1km × 1km gridded datasets for hydrological and inundation modelling on the British National Grid.
  - Datasets cover outflow drainage directions, catchment areas, bankfull river widths, bankfull river depths, and NRFA gauging station locations on the 1km grid.
  - Derived values are produced for every UK land cell from higher-resolution data and various relationships.

- Data production methods
  - Outflow drainage directions and catchment areas are primary datasets, derived from high-resolution data and then aggregated to 1km cells.
  - Bankfull river widths and depths are estimated for all UK cells using regression relationships based on catchment characteristics and rainfall.
  - GB-specific observations are extrapolated to NI and parts of ROI; GB relationships are assumed to apply UK-wide where data are lacking.
  - QA includes visual checks against higher-resolution river networks; multiple coding schemes (ESRI and Unifhy) are provided for compatibility.

- River outflow drainage directions and catchment area
  - Drainage directions use the D8 method with eight directions; ESRI and Unifhy numbering schemes are provided.
  - Catchment area for each 1km cell is the count of upstream cells including the cell itself.
  - Derived from hydrologically corrected 50m IHDTM; manual corrections align 1km network with 50m network.

- Bankfull river widths
  - 1km bankfull widths derived from a regression using OS MasterMap Water Network Layer data, 50m IHDTM catchments, and catchment rainfall.
  - Equation: RW = 0.0042 × A^0.409 × SAAR^0.86, with A in km^2 and SAAR in mm.
  - GB-based fit (38600 sites) yields R^2 ≈ 0.80; coastal SAAR gaps filled by nearest-neighbor means.
  - Anomalies may occur; GB-wide regression applied UK-wide (including NI).

- Bankfull river depths
  - Similar regression approach using historical depth measurements (90 sites) to relate bankfull depth RD to A and SAAR.
  - Equation: RD = 0.02643 × A^0.202 × SAAR^0.402.
  - R^2 ≈ 0.57 with notable scatter at larger depths; coastal SAAR gaps filled by nearest-neighbor means.

- NRFA River flow gauging station locations on the 1km x 1km river network
  - NRFA provides daily/peak flow data from ~1500 stations; true station locations may differ from the discretised 1km network.
  - NRFA_gauging_station_locations_1km.csv links 1499 NRFA stations to 1km grid cells, with catchment area comparisons and overlap metrics.
  - Columns include OSGB reference, grid coordinates (col/row), 1km and IHDTM catchment areas, catchment overlap error, and overlap area percentage.
  - Includes Northern Ireland stations; some catchment overlap statistics are unavailable due to projection issues.

- Quality information
  - Spatial resolution is 1km; expected discretisation error around 0.5km (varies by area).
  - Outflow directions QA involves manual corrections to align with 50m IHDTM networks.
  - Catchment-area discretisation can misrepresent boundary fractions; NRFA file provides median area overlap error (≈1% median).
  - Bankfull width/depth estimates carry regression-based uncertainties (typical standard errors: width ~0.5 m, depth ~0.36 m).

- Dataset format
  - Gridded datasets stored as NetCDF files; NRFA gauging locations in CSV.
  - File names:
    - UK_outflow_drainage_directions_1km_ESRI.nc
    - UK_outflow_drainage_directions_1km_Unifhy.nc
    - UK_catchment_areas_1km.nc
    - UK_bankfull_river_widths_1km.nc
    - UK_bankfull_river_depths_1km.nc
    - NRFA_gauging_station_locations_1km.csv
  - Units: catchment area in km^2; bankfull widths/depths in metres.
  - Domain: 656 km × 1220 km on the British National Grid (0,0) to (656000,1220000); GB land mask extended to include Shetland and certain inland gaps; NI uses OSNI mask with some flow from ROI.

- How to use the data
  - Suitable for configuring hydrological components of gridded land-surface and hydrological models.
  - Datasets cover all UK land points; users can apply their own river/mask definitions (e.g., rivers by catchment area threshold).
  - Extended into tidal regions; estuary values are not representative of real tidal conditions.
  - Readable directly in ArcGIS to generate 1km-scale UK river networks for analysis or display.

- Acknowledgements
  - Supported by NERC awards NE/S017380/1 (Hydro-JULES) and NE/R016429/1 (UK-SCAPE).
  - Collaborators include UKCEH, BGS, NCAS; thanks to Oliver Robertson.

- References
  - Key methodological references for drainage directions, digital terrain models, and bankfull estimation methods (Paz et al. 2006; Jenson & Domingue 1988; Morris & Flavin 1990; Naden & McCartney 1991; Nixon 1959).