# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE program, Work Package 2, investigates climate-change impacts on water quantity across Britain.
- Provides Grid-to-Grid (G2G) hydrological model estimates of river flow on a 1 km × 1 km grid across Great Britain, driven by observation-based meteorology (1980–2011).
- Outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow.
- Data are designed for use in map-based GIS analyses and cross-comparison with observed flows.

## What is included
- Gridded river flow estimates (G2G) driven by observed data
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹)
  - Annual minima of 7-day mean river flow (m³ s⁻¹)
- Spatial resolution and coverage
  - 1 km × 1 km grid across Great Britain
  - Non-sea, non-tidal cells with catchment area ≥ 50 km²
- Complementary dataset
  - G2G estimates driven by UKCP18 Regional (12 km) climate projections (for comparison)
- Supporting spatial datasets
  - Digitally-derived catchment areas on a 1 km grid
  - Estimated locations of flow gauging stations on a 1 km grid plus station information
- Data provenance
  - Observed driving data: CEH-GEAR (precipitation), MORECS (potential evaporation), Met Office temperature
  - Temporal downscaling and spatial configuration per Bell et al. 2009/2016 series

## Grid-to-Grid model (G2G) and inputs
- G2G features
  - National-scale hydrological model with 1 km × 1 km resolution and 15-minute time steps
  - Outputs natural river flows for gauged and ungauged rivers
  - Calibrated at a national scale using universal parameter values; no catchment-specific calibration
  - Accounts for urban/suburban land cover effects on run-off
- Required inputs
  - Daily precipitation (1 km, CEH-GEAR)
  - Monthly potential evaporation (PE) for short grass (MORECS)
  - Daily min and max temperature (1 km, Met Office)
- Snow module (optional)
  - Uses daily min/max temperatures for snow processes
- Data processing notes
  - Precipitation distributed evenly within each daily time-step
  - PE distributed monthly over time-steps, downscaled to 1 km
  - Temperature downscaled through the day using a sine curve
- Model scope
  - Outputs are for non-tidal, non-sea grid cells with catchment area ≥ 50 km²

## Data formats and files
- NetCDF-4 data files, one file per variable
  - Monthly mean river flow: G2G_GB_mmflow_obs_1980_2011.nc
  - Annual maxima of daily mean river flow: G2G_GB_amaxflow_obs_1980_2011.nc
  - Annual minima of 7-day mean river flow: G2G_GB_aminflow_obs_1980_2011.nc
- Time period and availability
  - Data span: December 1980 to November 2011 (varies by file)
- Spatial domain and cell addressing
  - 700 km × 1000 km domain aligned to the GB National Grid
  - Grid cell values represent the centre of the 1 km × 1 km cell
  - Missing value: -9999
  - Time stamps: days since 1900-01-01
  - Monthly values assigned to the first day of each month
  - Annual maxima/minima assigned to the start year of the corresponding 12-month period
- Additional datasets to aid interpretation
  - Catchment areas: UKSCAPE_G2G_GB_CatchmentAreaGrid.nc (km²)
  - Gauging station locations: UKSCAPE_G2G_GB_NRFAStationIDGrid.nc (aligned to 1 km grid)
  - Station details: UKSCAPE_GB_NRFAStationIDs.csv
  - NRFA gauging stations: ~1038 locations (0 = land, -9999 = sea in grid)

## Spatial coverage and resolution
- Output domain: Great Britain (non-tidal rivers)
- Spatial resolution: 1 km × 1 km grid
- Effective domain: specified coordinate range on the GB National Grid
- Data are geared toward comparison with observed NRFA river flows and with other G2G datasets

## Usage and analysis
- Primary uses
  - Compare G2G river-flow estimates with observed NRFA river flows
  - Analyze historic river-flow patterns (1980–2011) for policy, planning, and risk assessment
  - Combine with UKCP18-driven (12 km) projections for climate-change impact studies
- Data integration
  - NetCDF files can be read into standard GIS/analysis tools
  - Spatial and station grids enable linking model outputs to gauging data

## Data quality and limitations
- Calibration
  - G2G uses nationally applicable parameter values; no catchment-specific calibration
- Performance variation
  - Best performance in natural-flow-dominated catchments; less accurate under strong anthropogenic influence or complex sub-surface hydrology
- Discretisation effects
  - Some small catchments may have catchment area assignments that differ from observed NRFA catchments
  - Potential mismatches between observed NRFA catchments and the 1 km grid discretisation
- Temporal and mask adjustments
  - Changes to land-sea mask and minor network discretisations compared with prior MaRIUS datasets
- Data provenance and reproducibility
  - Acknowledges modeling choices and data sources; differences highlighted relative to MaRIUS G2G datasets

## Related datasets
- UKCP18 Regional climate projections (12 km) for cross-comparison with observed-driving results
- MaRIUS G2G datasets (historical) for reference and consistency checks
- NRFA river-flow observations for validation and benchmarking

## Acknowledgements and references
- Funded by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCAPE programme
- Contributions from researchers including Nuria Bachiller-Jareno, Ting Zhang, and Oliver Robertson
- Key references include Bell et al. 2009, 2016, 2018; Rudd et al. 2017; Formetta et al. 2018; Davies & Bell 2009; Tanguy et al. 2016; Met Office HadUK-Grid data (Hollis et al. 2019)