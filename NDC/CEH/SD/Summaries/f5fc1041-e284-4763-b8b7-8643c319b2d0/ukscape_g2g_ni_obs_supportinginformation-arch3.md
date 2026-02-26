# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE programme provides Grid-to-Grid (G2G) hydrological model outputs at 1 km x 1 km resolution for Northern Ireland (NI) driven by observed meteorological data (1980–2011).
- Outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow.
- Datasets are designed to support analysis alongside projections driven by UKCP18 climate scenarios and comparison with observed gauged flows.

## Grid-to-Grid (G2G) model description
- National-scale hydrological model configured for NI and nearby catchments draining to NI rivers, aligned with the GB national grid.
- Produces natural (unregulated) river flow estimates for gauged and ungauged rivers; generally spi­atially biased by lack of lake/reservoir storage effects in the model.
- Calibration: uses nationally-consistent parameters rather than catchment-specific calibration; urban/suburban land cover effects incorporated via routing and land-cover data.
- Performance: generally good across NI with caveats downstream of Lough Neagh where regulation caps flows; best for natural-flow-dominated catchments.

## Model inputs
- Precipitation: Daily 1 km grids (CEH-GEAR).
- Potential Evaporation (PE): Monthly 40 km grids (MORECS) for short grass.
- Temperature: Daily min/max grids (Met Office).
- Data processing: precipitation and PE reprojected to the 1 km GB grid; temporal downscaling and infilling applied where data gaps exist.
- Spatial data: topography and soil data consistent with prior G2G configurations.

## How the data are structured and formats
- Outputs provided as NetCDF4 files per variable with 1 km x 1 km grid cells (non-tidal, catchment area ≥ 50 km²; missing data marked as -9999).
- Timeframes:
  - Monthly mean river flow (m³ s⁻¹), 1980 Dec–2011 Nov.
  - Annual maxima of daily mean river flow (m³ s⁻¹), 1981–2011.
  - Annual minima of 7-day mean river flow (m³ s⁻¹), 1980 Dec–2011 Nov.
- Spatial domain: NI on GB National Grid (187 km x 170 km) with grid cell centers representing each pixel; coordinates given in metres.
- Time stamping: monthly means assigned to the first day of each month; annual maxima/minima assigned to the start year of the corresponding 12-month period.

## Auxiliary datasets included
- Digitally-derived catchment areas for each 1 km grid cell (km²).
- Lake identification grid (1 km) marking majority lake cells (>70% water coverage) with manual adjustments for Lough Erne.
- Estimated locations of NRFA gauging stations on the 1 km grid to align G2G outputs with observed gauges (43 stations).
- A CSV version of NRFA station IDs to complement the grid-based identifiers.

## Using the data and interpretation
- The G2G outputs can be compared with observed flows from the National River Flow Archive (NRFA) to assess model performance.
- Can be analyzed alongside the companion NI dataset driven by UKCP18 Regional climate projections (for scenario-based flow changes).
- Practitioners should consider lake/reservoir storage effects are not included; some river flows in lake-affected cells may not reflect true downstream behavior.

## Limitations and caveats
- Lakes and reservoirs are not modeled; lake cells are treated as rivers in flow calculations.
- Small catchments may exhibit greater discretisation errors due to 1 km grid resolution and catchment-area alignment.
- Some data gaps were infilled; users should review metadata for specific infill methods and uncertainties.
- NRFA catchment area at the grid cell level may differ from observed NRFA catchments, particularly for smaller basins.

## Data governance and accessibility considerations for monitoring work
- Data originate from the NERC Environmental Information Data Centre (NERC EIDC); dataset is associated with open sharing and transparency principles typical of monitoring frameworks.
- Metadata and supporting datasets (catchment areas, lake grids, NRFA station mappings) enhance traceability and verifiability of the monitoring outputs.
- Clear documentation of file naming, coordinate system, and time conventions aids reproducibility and integration into broader monitoring dashboards and governance processes.
- Acknowledges limitations and provides references for model methods and prior validations, supporting rigorous interpretation within monitoring frameworks.