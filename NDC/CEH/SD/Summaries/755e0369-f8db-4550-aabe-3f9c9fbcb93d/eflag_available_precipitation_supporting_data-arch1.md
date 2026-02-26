# Enhanced Future FLows and Groundwater (eFLaG): Gridded simulations of available precipitation for Great Britain Supporting Information Document

## Overview
- Provides nationally consistent 1 km gridded simulations of available precipitation (rainfall + snowmelt) for Great Britain.
- Two data streams: observational data (Jan 1961–Dec 2018) and Regional Climate Model (RCM) projections (Dec 1980–Nov 2080).
- Data used as common driving input for eFLaG hydrological projections, supporting drought-focused river, groundwater, and recharge models.

## Data sources

- Observational data
  - HadUK-Grid precipitation and min/max temperature; 1 km daily resolution.
  - Aligned with UKCP18 projections for monitoring and climate change research.

- Climate projections
  - UKCP18 RCM ensemble projections (12 members) over UK, derived from HadGEM3-GC3.05 and HadREM3-GA705.
  - 360-day calendar (12 months of 30 days) with time series not inherently aligned to 365/366-day year.
  - Part of a perturbed-parameter ensemble (PPE) to represent climate model parameter uncertainty under RCP8.5.

## Methodology

- Bias correction and downscaling
  - Observed rainfall data aggregated to 12 km to match RCM resolution.
  - For each month and grid cell, compute change factors between RCM precipitation and HadUK-Grid observations over 1981–2010.
  - Smooth bias-correction factors to reduce spatial discontinuities.
  - Apply monthly bias correction factors to RCM time series and downscale from 12 km to 1 km based on the distribution of SAAR (Standard-period Average Annual Rainfall).

- Temperature adjustments
  - Minimum and maximum daily temperatures from RCM members downscaled to 1 km using lapse rates and elevation data.

- Available precipitation (snow module)
  - Converts precipitation into rainfall plus snowmelt (available precipitation) using daily min/max temperatures.
  - Applied separately to observational-based and bias-corrected/downscaled RCM data.
  - Snow module parameters defined in Table 1 (see below).

## Data products and structure

- Total dataset: 264 NetCDF files.
  - Observational simulations: 12 files covering 1961–2018, split into roughly 5-year periods.
  - RCM simulations: 252 files per ensemble member (21 periods × 12 members), covering 1980–2080; first/last files have fewer time-steps due to calendar alignment.
- File naming conventions
  - Observational: avail_precip_obs_YYYYMM_YYYYMM.nc (e.g., avail_precip_obs_196101_196512.nc).
  - RCM: avail_precip_rcmXX_YYYYMM_YYYYMM.nc (XX = ensemble member 01–12,13,15; e.g., avail_precip_rcm01_198012_198412.nc).
- Spatial and units
  - 1 km gridded data in British National Grid.
  - Available precipitation units: kg m^-2 (equivalent to mm day^-1).
- Scope
  - Data encompasses GB-wide 1 km grid for the specified periods, designed to drive hydrological modelling in eFLaG.

## Snow module and parameters

- Snowmelt model converts precipitation to rainfall and snowmelt (available precipitation) based on daily temperatures.
- Key parameters (from Table 1):
  - lapse_rate: 0.0059 (temperature lapse with elevation)
  - tsnow: 1.0 °C (threshold above which precipitation may be rain)
  - tmelt: 0.0 °C (threshold for snowmelt)
  - mfac: 6.0 (melt factor)
  - tdrel: 0.0 °C (drainage release threshold)
  - k1, k2: 0.5, 0.9 ( storage time constants)
  - Scfac: 0.18 (critical water retention capacity)
  - snowfrac: 1.1 (under-catch factor for rainfall as snow)

## Quality control and provenance

- Visual QA conducted to ensure reasonable values.
- Bias correction and downscaling steps validated against observed meteorology and prior methodologies.
- Data produced to support consistent driving inputs for multiple hydrological models within eFLaG.

## Usage and context

- Serves as common driving data for:
  - River flow projections (Grid-to-Grid, PDM, GR4J, GR6J)
  - Groundwater levels (Aquimod)
  - Groundwater recharge (ZOODRM)
- Aims to support drought projections and climate resilience planning through harmonised, high-resolution precipitation data.

## Limitations and notes

- All RCM ensemble members share the same high-emission scenario (RCP8.5) and similar climate model structure; does not capture full climate uncertainty.
- 360-day year in RCMs leads to calendar differences with observed time series; leap days are not automatically added in the RCM data.
- Bias correction is based on 1981–2010 comparisons and may not remove all biases inherent in climate projections.

## References

- References to foundational methods and datasets underpinning HadUK-Grid, UKCP18, bias correction approaches, SAAR-based downscaling, and snowmelt modelling, including key works by Bell et al., Guillod et al., Hollis et al., Kay & Crooks, Lowe et al., Murphy et al., Prudhomme et al., Teutschbein & Seibert, and the eFLaG project documentation.