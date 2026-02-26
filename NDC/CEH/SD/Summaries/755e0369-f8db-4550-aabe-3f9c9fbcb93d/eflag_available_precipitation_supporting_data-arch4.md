# Enhanced Future FLows and Groundwater (eFLaG): Gridded simulations of available precipitation for Great Britain Supporting Information Document

## Overview
- Nationally consistent simulations of available precipitation (rainfall + snowmelt) for Great Britain at 1 km resolution.
- Two data streams:
  - Observational data covering January 1961 – December 2018.
  - Climate projections driven by Regional Climate Model (RCM) projections covering December 1980 – November 2080.
- Data used as common driving data for all eFLaG models (river flow, groundwater levels, groundwater recharge) with a focus on future drought projections.

## Observational data
- Source: HadUK-Grid precipitation and HadUK-Grid minimum/maximum temperature.
- Characteristics: UK-wide gridded observations interpolated to a uniform 1 km grid; aligned with UKCP18 projections for climate monitoring and research.
- Role: Provides baseline meteorology for bias correction and precipitation downscaling.

## Climate projections
- Based on UKCP18 ensemble: 12 high-resolution RCM-PPE members (12 km) covering December 1980 – November 2080.
- Method: Perturbed-parameter runs of HadGEM3-GC3.05/HadREM3-GA705 to represent climate model parameter uncertainty (same emissions scenario, RCP8.5).
- Notable caveats:
  - All members share the same high-emissions scenario and general model structure; do not represent full climate uncertainty.
  - RCM time series are on a 360-day year with 12 months; no artificial zero-rain insertion used in this dataset.

## Data processing: bias correction and downscaling
- Bias correction workflow (per month and ensemble member):
  1) Average HadUK-Grid observed rainfall to 12 km for consistency with RCM data.
  2) Compute monthly change factors between RCM simulations and HadUK-Grid observations for 1981–2010.
  3) Smooth change factors to reduce spatial discontinuities.
  4) Apply bias correction factors to RCM monthly timeseries and downscale from 12 km to 1 km based on SAAR distribution.
- Temperature:
  - Minimum/maximum daily temperature scaled from 12 km to 1 km using lapse rate and elevation data.
- Downscaling detail: 12 km to 1 km spatial downscaling guided by distribution of Standard-period Average Annual Rainfall (SAAR).
- Result: Bias-corrected, downscaled daily precipitation and temperature fields aligned with HadUK-Grid for observational consistency.

## Snow module and available precipitation
- A snow module converts precipitation into available precipitation (rainfall + snowmelt) using snow-melt dynamics.
- Applicable separately to observational and RCM-based simulations.
- Snow module parameters provided (Table 1) include lapse rate, snow threshold temp, melt factor, drainage thresholds, storage constants, retention capacity, and snow under-catch factor.

## Data structure and file organization
- Total dataset: 264 NetCDF files.
- Observational stream:
  - 12 NetCDF files covering 1961–2018, split into 5-year periods (final file covers 2016–2018 with limited years).
  - File naming example: avail_precip_obs_196101_196512.nc.
- RCM stream:
  - 252 NetCDF files (21 periods × 12 ensemble members).
  - 12 ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15.
  - Time coverage: December 1980 – November 2080, split into 21 files per member; first/last files have fewer time-steps due to calendar structure.
  - File naming example: avail_precip_rcm01_198012_198412.nc.
- Granularity: 1 km Gridded data on the British National Grid; units: kg m^-2 (equivalent to mm day^-1).

## Quality control
- Visual QA performed to ensure data values are reasonable and consistent with expectations.

## Data usage and applications
- Used as common driving data for:
  - Hydrological models: Grid-to-Grid, PDM, GR4J, GR6J.
  - Groundwater models: Aquimod (groundwater levels) and ZOODRM (groundwater recharge).
- Purpose: Provide consistent, transparent, and usable precipitation inputs to support drought projections and hydrological risk assessments.

## Uncertainties and limitations
- Bias correction relies on historical comparisons and may not capture all future biases or non-stationarities.
- All RCM PPE members share the same emission scenario (RCP8.5) and underlying model structure, limiting full climate uncertainty representation.
- 360-day calendar in RCM data requires careful interpretation when pairing with observed 365/366-day calendars.
- Initial and final time-period files have fewer time-steps; intermediate files are longer five-year blocks.
- Downscaling assumes SAAR-based distribution; real extremes may deviate.

## Access, metadata, and references
- Data format: NetCDF with explicit 1 km resolution, gridded on the British National Grid.
- Documentation and methodological references include UKCP18 science overview, HadUK-Grid publications, and snow/melt modeling studies (citations listed in the document).