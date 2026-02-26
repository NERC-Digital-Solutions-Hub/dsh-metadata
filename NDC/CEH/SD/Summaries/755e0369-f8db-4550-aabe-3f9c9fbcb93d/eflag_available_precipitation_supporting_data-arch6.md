# Enhanced Future FLows and Groundwater (eFLaG): Gridded simulations of available precipitation for Great Britain Supporting Information Document

- Purpose and scope
  - Provides nationally consistent simulations of available precipitation (rainfall + snowmelt) for Great Britain at 1 km resolution.
  - Includes observational-data-driven (1961–2018) and bias-corrected, downscaled climate-projection (1980–2080) simulations.
  - Serves as the common driving data for eFLaG hydrological projections (river flow, groundwater levels, groundwater recharge).

- Data sources
  - Observational data: HadUK-Grid precipitation and daily min/max temperature; aligned to UKCP18 projections; 1 km daily products.
  - Climate projections: UKCP18 Regional Climate Model perturbed-parameter ensemble (12 PPE members) based on HadGEM3-GC3.05/HadREM3-GA705; 12 km resolution, 1980–2080; 360-day calendar.

- Data processing workflow
  - Bias correction
    - Convert HadUK-Grid precipitation to 12 km to match RCM resolution.
    - Compute monthly change factors between RCM and HadUK-Grid over 1981–2010 for each month and member.
    - Smooth change factors to reduce spatial discontinuities.
    - Apply monthly bias-correction factors to RCM timeseries.
  - Downscaling
    - Downscale bias-corrected 12 km precipitation to 1 km using the distribution of SAAR (Standard-period Average Annual Rainfall).
  - Temperature handling
    - Scale 12 km temperature data to 1 km using lapse rates and elevation data.

- Snow module and available precipitation
  - Apply a snow model to convert precipitation into available precipitation (rainfall + snowmelt) using daily min/max temperatures.
  - Parameters and process described in Table 1 (lapse_rate, tsnow, tmelt, mfac, etc.).

- Data structure and accessibility
  - Total dataset: 264 NetCDF files.
  - Observational data: 12 files covering 1961–2018 (split into 5-year periods; final file covers 2016–2018).
  - RCM data: 252 files (21 periods × 12 PPE members) covering 1980–2080; 360-day year; 12 PPE members include 01, 04–13, 15.
  - File naming conventions:
    - Observations: avail_precip_obs_196101_196512.nc (example format).
    - RCM: avail_precip_rcm01_198012_198412.nc (example format).
  - Spatial and units
    - 1 km gridded data on British National Grid.
    - Available precipitation units: kg m^-2, equivalent to mm day^-1.

- Quality control and validation
  - Visual QA performed to ensure data values are reasonable.

- Context and references
  - eFLaG project funded by the Met Office as part of the UK Climate Resilience Programme; aims to provide hydrological projections from multiple models using a common driving dataset.
  - Outputs used as driving data for various eFLaG components (river flow, groundwater levels, groundwater recharge).
  - Related literature and dataset references provided for bias correction, downscaling, and snow-module methodologies.