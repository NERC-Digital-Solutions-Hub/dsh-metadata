# Enhanced Future FLows and Groundwater (eFLaG): Gridded simulations of available precipitation for Great Britain Supporting Information Document

## Summary
- Provides nationally consistent simulations of available precipitation (rainfall + snowmelt) for Great Britain.
- Two data streams: observational-based (January 1961 – December 2018) and Regional Climate Model (RCM) projections (December 1980 – November 2080).
- Data are 1 km gridded across Great Britain, used as driving data for eFLaG hydrological projections (river flow, groundwater levels, groundwater recharge) with a focus on drought scenarios.

## Observational Data
- Source: HadUK-Grid precipitation and min/max temperature (HadUK-Grid derived from UK land surface observations).
- Resolution and period: 1 km daily products; 1961–2018.
- Purpose: Consistent baseline for monitoring UK climate and supporting UKCP18 alignment.

## Climate Projections
- Source: UKCP18 UK-wide ensemble of Regional Climate Model (RCM) projections (HadGEM3-GC3.05 / HadREM3-GA705).
- Structure: 12 ensemble members (PPE) at 12 km resolution covering 1980–2080.
- Calendar: 360-day year (twelve 30-day months); data not adjusted to 365/366-day calendar to avoid artificial modifications.
- Uncertainty: PPE represents parameter uncertainty but all members share the same high-emissions scenario (RCP8.5) and underlying model structure.

## Data Processing and Bias Correction
- Bias correction: Simple monthly-mean bias correction using HadUK-Grid 1 km observations.
  - Steps:
    1) Aggregate HadUK-Grid to 12 km to match RCM resolution.
    2) For each month and grid cell, compute change factors between RCM and HadUK-Grid (1981–2010).
    3) Smooth change factors to reduce spatial discontinuities.
    4) Apply monthly bias correction to RCM timeseries and downscale to 1 km based on SAAR distributions.
- Temperature: Minimum/maximum daily temperatures biased by scaling from 12 km to 1 km using lapse rate and elevation data.

## Snow Module and Available Precipitation
- Purpose: Convert precipitation into available precipitation (rainfall + snowmelt) accounting for snow processes.
- Method: Snow module using daily min/max temperatures to separate rainfall and snowmelt; applied to both observed and bias-corrected RCM streams.
- Snow module parameters (Table 1): lapse_rate 0.0059 °C m⁻¹; tsnow 1.0 °C; tmelt 0.0 °C; mfac 6.0 mm °C⁻¹ day⁻¹; tdrel 0.0 °C; k1=0.5 day⁻¹; k2=0.9 day⁻¹; Scfac 0.18; snowfrac 1.1 (under-catch factor for gauged rainfall as snow; not applied to RCM data).

## Quality Control and Data Structure
- Quality control: Visual QA to verify reasonable value ranges.
- Data structure:
  - Total of 264 NetCDF files.
  - Observational simulations: 12 files (one per 5-year period) covering 1961–2018 (note: final file spans 2016–2018, 3 years).
  - RCM simulations: 252 files (21 periods × 12 ensemble members) covering 1980–2080; some early/late files have fewer time steps; RCM data uses 360-day years.
  - File naming examples:
    - Observed: avail_precip_obs_196101_196512.nc
    - RCM: avail_precip_rcm01_198012_198412.nc
  - Grid and units: British National Grid; 1 km resolution; units of kg m⁻2 (equivalent to mm day⁻1); coordinates begin at 0 E, 0 N.

## Data Access and Application
- Purpose: Common driving data for eFLaG hydrological models (river flow: Grid-to-Grid, PDM, GR4J, GR6J; groundwater levels (Aquimod); groundwater recharge (ZOODRM)).
- Usage: Enables nationally consistent hydrological projections and drought assessments across the UK.

## Limitations and Considerations
- Climate uncertainty: PPE members share the same high-emission scenario (RCP8.5) and model structure; does not represent full spectrum of climate uncertainty.
- Calendar alignment: 360-day year retained to preserve original time series; previous practices of inserting extra days were not applied here.

## References and Supporting Figures
- Key references for methods and data sources (e.g., HadUK-Grid, UKCP18, bias correction methodologies, snow module parameters).
- Figure 1: Flow diagram of the methodology.
- Figure 2: Bias correction grids by month and PPE member.
- Table 1: Snowmelt model parameters.