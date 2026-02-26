# Supporting documentation

## Overview
- A dataset of modelled vegetation carbon output from the JULES land surface model, plus monthly temperature and rainfall, at 1.5 km resolution.
- Four simulations: two climate projections under constant present-day CO2 and under a CO2 pathway following the SRES A1B scenario.

## Data provenance and background
- Simulations driven by HadRM3-PPE-UK ensemble data downscaled from 25 km to 1.5 km.
- Uses two climate projections and two CO2 scenarios (constant present-day CO2 and SRES A1B CO2 pathway).
- HadRM3-PPE-UK configurations include a standard parameter set (climate sensitivity 3.5 K) and an ensemble member with higher sensitivity (7.1 K).
- Present-day CO2 prescribed at 386.5 ppm; SRES A1B CO2 pathway applied.

## Quality control and access
- JULES is a community-developed model (UK Met Office and Centre for Ecology & Hydrology).
- Data produced with JULES version vn4.9; model configuration available in Rose suite u-ao645, branch transient_25km_drive.
- Access requires registration to the JULES repository (https://code.metoffice.gov.uk/trac/jules) and Rose suite portal (https://code.metoffice.gov.uk/trac/rosesu).

## Data structure and file organization
- Data provided in NetCDF (.nc) files.
  - Each file contains a grid of latitudes/longitudes, a time series of monthly midpoints, and the dataset values.
  - 35K and 71K directories correspond to different climatologies; within each, subdirectories for Const_CO2 and CO2 (two CO2 scenarios).
  - Each subdirectory contains three .nc files (one for each variable: vegetation carbon, temperature, rainfall).
  - Example filename: Temp_35K_Const_CO2.nc (temperature for 3.5 K, constant CO2 simulation).
- The dataset comprises monthly outputs for vegetation carbon, temperature, and rainfall across the specified spatial and temporal resolution.

## Variables and spatial-temporal details
- Variables: vegetation carbon output, temperature, rainfall.
- Spatial resolution: 1.5 km grid.
- Temporal resolution: monthly time steps.
- Climate contexts: four simulations (combinations of two climate projections and two CO2 pathways) across two climatologies.

## References
- Nakicenovic, N., Alcamo, J., Davis, G., (2000) IPCC Special Report on Emission Scenarios (SRES) A1B scenario.
- HadRM3-PPE-UK ensemble base data from the Hadley Centre (2008).

## Practical notes for GIS use
- Suitable for creating map-based visualisations of vegetation carbon, temperature, and rainfall at fine 1.5 km resolution.
- Data are model-derived and subject to uncertainties from climate projections, CO2 pathways, and downscaling.
- Use NetCDF format to integrate with common GIS and remote-sensing workflows; ensure proper handling of time and climatology-specific file naming.