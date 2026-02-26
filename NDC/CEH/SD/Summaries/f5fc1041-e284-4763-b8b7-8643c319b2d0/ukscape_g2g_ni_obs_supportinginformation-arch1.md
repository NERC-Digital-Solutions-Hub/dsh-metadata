# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by observed data (1980 to 2011)

- Purpose and scope
  - UK-SCAPE program, Work Package 2: research on climate-change impacts on water quantity (river flow) across Britain.
  - Provides Grid-to-Grid (G2G) hydrological model estimates of natural river flows for Northern Ireland (NI) at 1km x 1km resolution, driven by observed meteorology (1980–2011), with a complementary dataset for NI driven by UKCP18 Regional projections.
  - Outputs enable comparison with observed river flows and with climate-projected scenarios; supports analysis of catchment-scale hydrology.

- What is included
  - Gridded outputs on a 1km x 1km grid for NI (non-tidal, catchment area >= 50 km²):
    - Monthly mean river flow (m³ s⁻¹)
    - Annual maxima of daily mean river flow (m³ s⁻¹)
    - Annual minima of 7-day mean river flow (m³ s⁻¹)
  - Time period: 1980–2011 (water years structure described in data)
  - Spatial context: NI domain on GB National Grid (187 km x 170 km, centered on NI), plus datasets to aid interpretation (catchment areas, lake cells, NRFA gauging station locations)

- Grid-to-Grid (G2G) model overview
  - National-scale hydrological model, typically 15-minute time-step; configured for NI and some ROI catchments.
  - Outputs natural river flows for gauged and ungauged rivers; emphasizes spatial consistency over parameter calibration by catchment.
  - Urban/suburban land-cover effects on runoff are implicitly represented via parameterization; calibration is not individualized to catchments.
  - Performance notes: good for catchments with natural regimes; reduced performance where artificial abstractions/discharges or complex sub-surface hydrology prevail; NI-specific assessment shows generally good performance, with caveats downstream of Lough Neagh.

- Model inputs and processing
  - Meteorological inputs:
    - Daily 1km precipitation (CEH-GEAR)
    - Monthly 40km potential evaporation (PE) for short grass (MORECS)
    - Daily min/max temperature (Met Office)
  - Data handling and downscaling:
    - Precipitation re-projected to 1km GB grid; distributed evenly across daily time-steps.
    - PE distributed evenly across monthly time-steps.
    - Temperature downscaled within day using a sine curve.
    - PE and temperature data infilled where missing to cover required NI extent.
  - Spatial data used for model configuration follows established CEH/UKSCAPE data (topography, soils, etc.).

- Outputs and file formats
  - Primary outputs (NetCDF4, one file per variable):
    - G2G_NI_mmflow_obs_1980_2011.nc — monthly mean river flow
    - G2G_NI_amaxflow_obs_1980_2011.nc — annual maxima of daily mean river flow
    - G2G_NI_aminflow_obs_1980_2011.nc — annual minima of 7-day mean river flow
  - Time and coordinate details:
    - Time stamps: days since 1900-01-01; monthly means assigned to first day of the month; annual maxima/minima assigned to the start year of the 12-month period
  - Spatial domain and metadata:
    - NI domain: 1km x 1km grid on GB National Grid; non-tidal rivers with catchment area ≥50 km²; grid extents given in dataset documentation
    - Cells with no data are set to missing (-9999)
  - Additional supporting datasets (NetCDF4 or CSV as appropriate):
    - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc — catchment area (km²) draining to each 1km cell
    - UKSCAPE_G2G_NI_LakeGrid.nc — majority lake cells (binary grid; 1=land, 2=lake, -9999=sea)
    - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv — estimated 1km grid cell locations that best represent NRFA gauging stations (for model-observation comparisons)
  - Interpretation aids:
    - Three datasets help relate grid cells to catchment areas, lake presence, and observed gauging stations for validation and interpretation of model outputs

- How to use the datasets
  - Compare G2G-derived NI flows with observed NRFA river flows to assess model realism.
  - Compare with NI flows driven by UKCP18 Regional (12km) climate projections to explore climate-change scenarios.
  - Use catchment-area, lake-grid, and NRFA-station location grids to align model outputs with observed data and to identify appropriate comparison points.
  - Important modeling caveats:
    - Lakes and reservoir storage are not accounted for; lake cells are treated as river cells, potentially misrepresenting storage effects.
    - NRFA-station mapping to 1km grid cells may imperfectly match catchments, especially for smaller basins due to discretisation.
    - No catchment-by-catchment calibration; the model relies on globally applicable parameter values, which may influence accuracy in complex or highly regulated areas (e.g., around Lough Neagh).

- Limitations and caveats
  - Not accounting for lake storage/regulation can bias downstream flows in lake-influenced areas.
  - Potential misalignment between NRFA catchments and 1km G2G grid catchments, particularly for small basins.
  - Absence of catchment-specific calibration; general practice in G2G may perform best for natural-flow regimes.
  - Data gaps in required meteorological drivers are infilled; some parts of ROI/NI may rely on imputed data.

- Acknowledgements and references
  - Funded by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.
  - Supporting references include Bell et al. (2009, 2016), Kay et al. (2021), and related data sources (CEH-GEAR, MORECS, HadUK-Grid, Land Cover Map 2015).

- Access and citation
  - Dataset described here is provided as part of the NERC EDS Environmental Information Data Centre; DOI and related references are listed in the corresponding dataset record.