# Introduction to the project

- The dataset accompanies the Peru GROWS and PEGASUS projects, funded by NERC and CONCYTEC, and is linked to a paper on the energy and mass balance of Peruvian glaciers. Weather station inputs come from multiple Peruvian sites and are complemented by modelled data (WRF) and quality checks.
- The Peruvian component was conducted under an established call and contract framework, with collaborations from several universities and institutions. The focus is on using on-glacier weather data to drive the Tethys-Chloris ecohydrological model for point-scale glacier melt and mass-balance calculations.

## Station locations and instrumentation

- Modelling is performed at on-glacier stations at five Peruvian sites:
  - Shallap Glacier (Cordillera Blanca)
  - Artesonraju Glacier and Artesonraju Moraine
  - Cuchillacocha Glacier and Cuchillacocha Quilcay
  - Quisoquipina Glacier
  - Quelccaya Ice Cap
- Additional data from nearby off-glacier stations used for filling gaps when needed. Instruments measure a range of meteorological variables (air temperature, relative humidity, wind speed, shortwave/longwave radiation, precipitation, etc.) at specified heights and configurations.

## Data cleaning and quality control (2.3-related)

- Meteorological data were cleaned and quality-checked prior to analysis:
  - Clearly erroneous data removed; corrections applied to keep variables within plausible ranges.
  - Zeros in wind speed removed due to sensor freezing or measurement limits; replaced with hourly monthly averages.
  - Large jumps in temperature or humidity flagged and inspected; persistent anomalies removed.
  - Recording gaps addressed with nearby stations or model outputs where possible; some time series remain with gaps due to short data records (e.g., Shallap).
- Detailed correction rules and station-specific handling are documented (Tables 1–4 in the text).

## Data corrections and filling steps (summarised)

- Continuous timeseries were created by filling gaps from on-glacier data or corrected off-glacier data to reflect on-glacier conditions.
- For Shallap: multiple gaps and limited overlap led to a modelled gap (Dec 2011–May 2012) during snow-free conditions.
- For Cuchillacocha: on-glacier data overlapped with off-glacier data for ~14 days; relationships were derived primarily from winter conditions; summer corrections accounted for longer day length.
- Precipitation corrections involved adjusting for elevation differences and undercatch (notably for snow) using established correction factors and partition algorithms (Ding et al., Chubb et al. references). Daily totals were distributed hourly using site-specific ratios and, where necessary, modelled using WRF outputs.
- Wind, radiation, and other variables were filled using Donor station data (with bias adjustments) or model outputs, with site-specific transfer rules to preserve diurnal and seasonal cycles.

## Tethys-Chloris model (TC) framework

- All TC modelling code used for the Peru application is provided:
  - Main entry: T_and_C_Peru_EIDC.m
  - Parameter setup: PARAM_Peru.m
  - Radiation and precipitation partition routines: Peru_Automatic_Radiation_Partition_I.m and Precipitation_partition_Ding.m
- Model is hourly and runs on clean ice/snow surfaces; site-specific inputs include Ta, U, Ws, Rsw, and Pr; longwave radiation is optional (computed if not provided).
- Albedo can be specified or modelled; snow/ice albedo parameterisations are available; longwave input can be provided or cloudiness inferred.
- Model parameters cover surface roughness, snow densities, snow and ice depths, and other physical properties; many parameters are configured in main model files and parameter lists.
- Outputs follow a standard convention for flux directions, later adjusted in downstream analysis to downward-positive forms.

## Data structure and units (folders and contents)

- Data are organized into three folders:
  - Input_data: cleaned and filled on-glacier meteorological inputs (to be read by T_and_C_Peru_EIDC.m). Includes:
    - Datetime, Ta (°C), Pr (mm h-1), U (fraction), Ws (m s-1), Rsw (W m-2), Rsw_out, Latm (W m-2), L_out, NetR, SR_50 (snow/ice surface), zatm_hourly_m, Ameas (albedo), and other available variables.
    - Some NaNs indicate missing data; not all stations had all variables.
  - Main_run_code: site-specific run files (e.g., T_and_C_Peru_EIDC.m) and parameter files (PARAM_Peru.m); radiation partition and precipitation partition routines.
  - T_and_C: model functions for aerodynamic resistance, albedo properties, radiation transfer, snow/ice processes, and numerous other components required by the TC model.
- The dataset includes both .mat (for MATLAB-based running) and .csv (with corrected inputs in usable units) files. Each station has station-specific inputs and metadata (e.g., instrument heights, sensor types, measurement details).

## How to run and use the data

- To run the model, update input paths in T_and_C_Peru_EIDC.m and ensure necessary inputs (Ta, U, Ws, Rsw, Pr) are provided.
- Time zone, latitude/longitude, and elevation must be set appropriately; longwave can be provided or cloudiness inferred.
- Albedo can be provided or modelled; snow albedo parameters are in Albedo_Snow_Properties.m; cloudiness and cloud-related radiation inputs are managed via the Automatic Radiation Partition files.
- Instrument heights may be static or hourly (zatm_hourly); switch controls are available to enable hourly input.
- The model uses several precipitation partition schemes; for the Peru run, the Ding et al. (2014) approach is used by default, with options to switch.
- Full parameter and model structure details are provided in the supporting documents (TC_Variable_and_Parameter_List.pdf and TeC_technical_reference.pdf).

## Notes and references

- The data and modelling approach reference a range of studies on ecohydrological modelling, snow/ice processes, and precipitation corrections, including:
  - Chubb et al. (2015) on wind-induced precipitation undercatch
  - Ding et al. (2014) precipitation type partitioning
  - Fatichi et al. (2012a, 2012b) ecohydrological modelling
  - Mastrotheodoros et al. (2020) related work
  - Nitu et al. (2018) SPICE precipitation intercomparison context
- Key datasets include on-glacier weather data, off-glacier donor data, and WRF-modeled inputs for gaps and high-elevation sites.