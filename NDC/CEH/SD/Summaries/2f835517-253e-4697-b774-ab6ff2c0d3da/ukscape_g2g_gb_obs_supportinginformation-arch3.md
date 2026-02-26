# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE is a five-year program funded by the Natural Environment Research Council to study climate change impacts on water quantity across Britain.
- The Grid-to-Grid (G2G) hydrological model provides 1 km x 1 km gridded estimates of natural river flows for gauged and ungauged rivers across Great Britain, using observed meteorological data.
- Datasets cover monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow for water years Oct-Sep (and Dec-Nov for minima), on a 1 km grid for Great Britain (1980–2011).
- A complementary dataset exists for flows driven by UKCP18 Regional projections (12 km grid).
- Two auxiliary spatial datasets accompany the flows: digitally-derived catchment areas per 1 km grid cell and estimated locations of river gauging stations.

## What is included
- Grid-to-Grid model outputs for Great Britain driven by observed data (1980–2011):
  - Monthly mean river flow (m3 s−1)
  - Annual maxima of daily mean river flow (m3 s−1)
  - Annual minima of 7-day mean river flow (m3 s−1)
- Spatial domain: 1 km x 1 km grid across GB, non-tidal river cells with catchment area ≥ 50 km2.
- Additional datasets for interpretation and validation:
  - Digitally-derived catchment area grid (km2) draining to each 1 km grid cell
  - Estimated NRFA gauging station locations on the 1 km grid and station metadata

## G2G model at a glance
- A national-scale hydrological model at 1 km grid with a 15-minute time-step, designed to provide spatially consistent natural river flow estimates.
- Prioritizes using spatial data over calibration of catchment-specific parameters; uses nationally applicable values where needed.
- Incorporates effects of urban and suburban land cover on runoff.
- Performance is strongest for catchments with natural flow regimes and weaker where artificial abstractions/discharges or complex subsurface hydrology dominate.

## Data inputs and structure
- Meteorological inputs:
  - Daily precipitation (CEH-GEAR)
  - Monthly potential evaporation (MORECS)
  - Daily min/max temperature (HadUK-Grid)
- Spatial inputs (as in Bell et al. 2009): topography and soil data; optional snow module inputs (temperature time-series)
- Outputs are provided as NetCDF4 files per variable:
  - G2G_GB_mmflow_obs_1980_2011.nc (monthly mean river flow)
  - G2G_GB_amaxflow_obs_1980_2011.nc (annual maxima of daily mean river flow)
  - G2G_GB_aminflow_obs_1980_2011.nc (annual minima of 7-day mean river flow)
- Metadata conventions:
  - 700 km × 1000 km domain on GB National Grid
  - 1 km grid cells with catchment area ≥ 50 km2
  - Time stamps: days since 1900-01-01; monthly flows assigned to first day of month; annual maxima/minima aligned to start of corresponding 12-month period
  - Missing values denoted by -9999

## How to use and relate to monitoring efforts
- Datasets can be compared with observed river flows from NRFA to assess model performance and to support validation of hydrological indicators.
- Can be used alongside UKCP18-driven G2G datasets for scenario analysis and monitoring of potential climate-change impacts on river flows.
- The accompanying gauging-station grid enables targeted validation at NRFA sites; caveats apply for smaller catchments where discretisation may misalign with observed catchment boundaries.
- Useful for updating or cross-validating existing monitoring frameworks (e.g., MaRIUS-G2G-MORECS monthly data) with a shorter historical window (1980–2011) and updated network discretisation.

## Limitations and caveats
- Some residual differences between G2G outputs and observed NRFA flows may arise from catchment discretisation, especially for small catchments.
- G2G uses simplified, globally applicable parameter values rather than catchment-specific calibration; performance is sensitive to anthropogenic influences and sub-surface hydrology complexity.
- Public sharing of underlying base data and metadata is essential for transparency and governance, but users should be aware of potential mismatches between modeled and observed delineations.

## Data governance, sharing, and provenance
- Data are provided under CEH gridded dataset conventions with documented metadata to support reproducibility and governance in monitoring frameworks.
- Acknowledges support from the Natural Environment Research Council (award NE/R016429/1) and contributors.
- References to foundational methodological work and prior MaRIUS G2G datasets support interpretation and methodological transparency.

## Acknowledgements and references
- Core references include Bell et al. (2009, 2016, 2018), Rudd et al. (2017), Formetta et al. (2018), Hough and Jones (1997), Met Office HadUK-Grid (2019), and Davies & Bell (2009).