# Enhanced Future Flows and Groundwater (eFLaG): Gridded simulations of available precipitation for Great Britain Supporting Information Document

- This document presents nationally consistent simulations of available precipitation (rainfall plus snowmelt) for Great Britain at 1 km resolution, covering two main data streams:
  - Observationally derived data: January 1961 – December 2018
  - Model-projected data: December 1980 – November 2080 (UKCP18 Regional Climate Model ensemble)
- The dataset was developed for the eFLaG project to provide common driving data for hydrological projections (river flow, groundwater levels, groundwater recharge) and drought risk assessment.

## Data sources

- Observational data
  - HadUK-Grid precipitation and minimum/maximum temperature derived from UK land surface observations
  - Interpolated to a uniform 1 km grid; aligned with UKCP18 projections for monitoring and climate research purposes
- Climate projections
  - UKCP18 Regional Climate Model ensemble (RCM PPE) for the UK
  - 12 high-resolution members on a 12 km grid, covering 1980–2080
  - Uses perturbed-parameter runs of HadGEM3-GC3.05/HadREM3-GA705; all members share the same high-emissions scenario (RCP8.5)
  - Data calendar is a 360-day year (12 months of 30 days)

## Data processing and bias correction

- Bias correction and downscaling workflow
  - Step 1: Regrid HadUK-Grid observed rainfall from 1 km to 12 km for consistency with the RCM data
  - Step 2: For each month and grid cell, compute change factors between RCM-simulated precipitation and HadUK-Grid observations over 1981–2010
  - Step 3: Smooth the change factor grids to reduce spatial discontinuities
  - Step 4: Apply the monthly bias correction factors to the RCM precipitation timeseries
  - Step 5: Downscale the bias-corrected 12 km precipitation to 1 km based on the distribution of Standard-period Average Annual Rainfall (SAAR)
  - Temperature: scale 12 km HadUK-Grid temperatures to 1 km using lapse rate and elevation data
- Snow module
  - Converts precipitation to available precipitation (rain + snowmelt) using daily min/max temperatures
  - Parameters defined in Table 1 of the document (snow thresholds, melt factors, storage dynamics, etc.)
  - Applied separately to both observed-derived and bias-corrected/downscaled RCM data
- Quality control
  - Visual QA performed to verify reasonableness of outputs

## Data products and structure

- Total dataset contains 264 NetCDF files
  - Observational data (avail_precip_obs)
    - 12 NetCDF files covering 1961–2018, split into 5-year periods for manageable file sizes
    - Filenames follow the pattern: avail_precip_obs_YYYYMM_YYYYMM.nc
  - RCM-based data (avail_precip_rcm)
    - 252 NetCDF files (21 time periods × 12 ensemble members)
    - 12 ensemble members labeled 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
    - Period: December 1980 – November 2080, split into 21 files per member
    - Note: Initial and final files have fewer time steps; middle files span 5-year blocks
    - Filenames follow the pattern: avail_precip_rcmMM_YYYYMM_YYYYMM.nc (e.g., avail_precip_rcm01_198012_198412.nc)
- Spatial and data format
  - 1 km gridded data on the British National Grid
  - Available precipitation units: kg m^-2, equivalent to mm day^-1
- Temporal specifics
  - RCM data maintain a 360-day year; observed data use standard calendar
  - Temperature and precipitation bias corrections are designed to align RCM outputs with HadUK-Grid observations

## Data quality, limitations, and caveats

- Bias correction limitations
  - Based on a simple monthly-mean correction; preserves monthly bias structure but cannot capture all non-stationarities
  - Derived from 1981–2010 comparison window; assumes bias consistency over time
- Temporal calendar caveats
  - RCMs use 360-day years; direct alignment with observed 365/366-day calendars requires careful interpretation
- Uncertainty representation
  - 12 PPE members provide parameter-driven uncertainty but share the same emissions scenario (RCP8.5) and backbone model structure; do not span full climate uncertainty
- Snow and snowmelt modelling
  - Snow module parameters are fixed (Table 1); results depend on daily temperature thresholds and melt factors
- Data scope and purpose
  - Dataset is intended as a common driving dataset for hydrological modelling and drought projections, not as a complete climate ensemble of all uncertainties

## Usage and governance considerations for Data Stewards

- Provenance and metadata
  - Document the observational and model sources, bias-correction workflow, downscaling method, and snow-module parameters
  - Record calendar treatment (360-day year vs. standard calendar) and its implications for analysis
- Data management
  - Large file volumes (264 NetCDF files); maintain clear file naming conventions and time-period splits
  - Ensure reproducibility by archiving bias-correction steps and parameter choices
- Interoperability and governance
  - Use as a standardized driving dataset across hydrological models (e.g., river flow, groundwater recharge, groundwater levels)
  - Be explicit about limitations (bias-correction approach, calendar differences, and emission scenario constraint) when communicating results
- Data quality monitoring
  - Maintain QA processes beyond initial visual checks; periodically re-validate with updated HadUK-Grid data or new UKCP18-related projections
- Accessibility and citation
  - Reference primary sources for the data and methods (e.g., Hannaford et al., 2022; Hollis et al., 2019; Murphy et al., 2018) and ensure users credit the dataset appropriately

## References

- Bell, V.A., Kay, A.L., Davies, H.N., Jones, R.G., 2016
- Bell, V.A., Kay, A.L., Jones, R.G., Moore, R.J., 2007
- Guillod, B.P., et al., 2018
- Hannaford, J., et al., 2022
- Hollis, D., et al., 2019
- Kay, A.L., Crooks, S.M., 2014
- Lowe, J.A., et al., 2019
- Met Office, Hollis, D., et al., 2022
- Murphy, J.M., et al., 2018
- Prudhomme, C., et al., 2012
- Teutschbein, C., Seibert, J., 2012