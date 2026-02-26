# Enhanced Future FLows and Groundwater (eFLaG): Gridded simulations of available precipitation for Great Britain Supporting Information Document

- Purpose and scope
  - Presents nationally consistent simulations of available precipitation (rainfall + snowmelt) for Great Britain.
  - Includes observational-data-driven simulations (Jan 1961–Dec 2018) and UKCP18-driven projections (Dec 1980–Nov 2080), both at 1 km resolution over GB.
  - Used as common driving data for eFLaG hydrological models (river flow, groundwater levels, groundwater recharge) with a focus on future drought projections.

- Observational data
  - Source: HadUK-Grid precipitation and min/max temperature (Met Office et al., 2022).
  - Characteristics: 1 km daily gridded data across the UK; aligned with UKCP18 projections for consistency.
  - Purpose: foundation for bias correction and downscaling of climate projections; supports monitoring and climate research.

- Climate projections and ensemble
  - Source: UKCP18 regional climate model projections ( HadGEM3-GC3.05 / HadREM3-GA705 ), 12 PPE members.
  - Periods: 1980–2080 (climate time-series); data provided on a 360-day year (12 months of 30 days).
  - Coverage: UK-wide, 1 km downscaled from 12 km.
  - Uncertainty: PPE reflects parameter uncertainty within the same model framework and emissions scenario (RCP8.5); does not span full climate uncertainty.

- Data processing and bias correction
  - Bias correction workflow:
    - Aggregate HadUK-Grid to 12 km to match RCM resolution.
    - Compute month- and grid-cell-specific change factors between RCM and HadUK-Grid (1981–2010 period) for each ensemble member.
    - Smooth change factors to reduce spatial discontinuities.
    - Apply bias-correction factors to RCM monthly precipitation time series, producing bias-corrected precipitation.
  - Downscaling and temperature handling:
    - Downscale bias-corrected 12 km data to 1 km using SAAR distribution.
    - Temperature (min/max) scaled from 12 km to 1 km using lapse rate and elevation data.
  - Snow and available precipitation:
    - Apply a snow module to separate precipitation into rainfall and snowmelt (available precipitation) based on daily min/max temperatures.
    - Module parameters documented in Table 1 (lapse rate, snow threshold, melt factors, drainage constants, etc.).
  - Output: time series of available precipitation (rainfall + snowmelt) for both observed and RCM-driven simulations.

- Quality control
  - Visual QA steps to ensure spatial plausibility and reasonable values across the gridded dataset.

- Data structure and access
  - Total files: 264 NetCDF files.
  - Observational simulations: 12 NetCDF files covering 1961–2018, split into ~5-year periods.
  - RCM simulations: 252 NetCDF files (21 periods × 12 ensemble members); ensemble members are labeled 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15.
  - Time coverage and file layout:
    - Observations: 1961-01 to 2018-12 (split into 5-year chunks; final file covers 2016-2018 and may contain fewer time-steps).
    - RCM: 1980-12 to 2080-11; files split with 4-year initial period and 11-month final period in the first/last files; intermediate files cover 5-year blocks.
  - Spatial reference: British National Grid; grid origin at lower-left corner (0,0).
  - Spatial resolution: 1 km.
  - Data units: available precipitation values in kg m^-2, equivalent to mm day^-1.
  - File naming conventions:
    - Observations: avail_precip_obs_YYYYMM_YYYYMM.nc (e.g., avail_precip_obs_196101_196512.nc).
    - RCM: avail_precip_rcmXX_YYYYMM_YYYYMM.nc (e.g., avail_precip_rcm01_198012_198412.nc; XX is the ensemble member number).
  - Documentation and figures:
    - Figure 1: flow diagram of methodology.
    - Figure 2: bias-correction grids by month and ensemble member.
    - Table 1: snowmelt model parameters (e.g., lapse_rate, tsnow, tmelt, mfac, etc.).

- Practical considerations for GIS specialists
  - The data provides a common, gridded driving field for hydrological and groundwater modelling, enabling map-based visualization of available precipitation and its drivers.
  - Temporal nuance: 360-day year in RCM outputs; when integrating with other datasets, consider aligning calendars or applying appropriate conversions.
  - Bias correction and downscaling introduce uncertainties; the RCM-based products reflect parameter uncertainty (PPE) but share a single emissions scenario (RCP8.5).
  - Workflow implications: NetCDF format is GIS-friendly but may require conversion or extraction for certain software; ensure coordinate reference system and metadata are correctly handled during import.
  - Snow component: accounts for snowmelt processes, which is important for hydrological visualizations and drought assessments.

- References and supporting components
  - Foundational papers and data sources linked to the bias correction, snow module, and UKCP18 framework.
  - Additional materials include the flow diagram (Figure 1), bias-correction details (Figure 2), and the snowmelt parameter table (Table 1).