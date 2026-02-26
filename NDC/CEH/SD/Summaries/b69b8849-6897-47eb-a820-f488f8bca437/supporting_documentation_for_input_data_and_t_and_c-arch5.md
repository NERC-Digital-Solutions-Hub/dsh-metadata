# The energy and mass balance of Peruvian glaciers

## Overview
- Dataset arises from the Peru GROWS and PEGASUS projects, funded by NERC and CONCYTEC (Newton-Paulet Fund).
- Associated with a paper on glacier energy and mass balance in Peru; data inputs include meteorological observations and modeled outputs.
- Weather data were collected at multiple glaciers in Peru and processed for use in a Tethys-Chloris ecohydrological model to compute melt and mass balance at a point scale.

## Data provenance and scope
- Projects: Peru GROWS and PEGASUS; weather and glacier data used for mass-balance modelling.
- Location: Five Peruvian glaciers/ice caps (Shallap, Artesonraju, Cuchillacocha, Quisoquipina, Quelccaya) with on-glacier and off-glacier stations.
- Data products include cleaned meteorological timeseries, model inputs, and documentation of data corrections and filling steps.

## Data collection and station details
- Stations and instrumentation described for on-glacier deployments, with coordinates, elevations, and variables measured (Ta, RH, wind speed, radiation components, precipitation, etc.).
- Modelled periods cover specific windows for each site (e.g., Artesonraju Glacier 2006–2013; Cuchillacocha Glacier 2014–2018; Quelccaya 2016–2018; Quisoquipina 2011–2016; Shallap and related sites with varying coverage).
- Data cleaning and quality checks applied prior to modelling; some variables measured off-glacier were used with site-specific corrections to represent on-glacier conditions.

## Data cleaning and quality control
- Steps applied to meteorological data:
  - Removal of clearly erroneous values; corrections to keep variables within reasonable ranges.
  - Zero wind speeds removed due to instrument freezing risks and energy-balance implications; gaps filled with monthly diurnal averages.
  - Large jumps and repeated identical values flagged and inspected; erroneous records removed.
- Specific cleaning rules (Table 1) include:
  - Relative humidity capped at 100%.
  - Incoming/outgoing shortwave radiation corrected to non-negative and physically consistent values.
  - Wind speed values ≤ 0 removed.
- Table 2 and Table 3 provide station metadata and instrument details (sensor types, heights, precision, and modelled periods).

## Data corrections and filling
- Data gaps filled using:
  - On-glacier data where available; off-glacier data corrected to represent on-glacier conditions.
  - Relationships with donor stations (e.g., Shallap data filled from nearby Shallap Moraine data; various donor relationships for Ta, RH, WS, S↓, S↑, L↓, and Pr).
  - WRF model outputs used for filling where observations were missing (e.g., S↓, Pr at several sites).
- Precipitation corrections include undercatch adjustments for snow using site-specific ratios (e.g., 0.63 under certain conditions) and conversion from daily to hourly sums when needed.
- Specific notes per site:
  - Shallap: multiple gaps; long gap in 2011–2012; not filled due to lack of overlap with other Shallap datasets.
  - Cuchillacocha: limited on-glacier data; relies on relationships with off-glacier data during winter conditions; adjustments for diurnal cycle and daylength effects.
  - Artesonraju: fills using relationships with nearby stations; Pr sourced from multiple stations and WRF when necessary.
  - Quelccaya and Quisoquipina: mixed measured and modelled data; Pr corrections and undercatch adjustments applied as appropriate.
- Donor relationships specify the exact combination of stations and the time alignment used to derive each variable.

## Data structure and units
- File structure includes three folders:
  - Input_data: Cleaned on-glacier meteorological data in .mat and .csv formats; includes variables such as Ta (°C), Pr (mm h−1), U (fraction), Ws (m s−1), Rsw (W m−2), Rsw_out, Latm (W m−2), L_out, NetR, SR_50, zatm_hourly_m, Ameas (albedo). NaNs indicate missing data.
  - Main_run_code: Peruvian Tethys-Chloris setup files, including T_and_C_Peru_EIDC.m (main run file) and PARAM_Peru.m (site-agnostic parameters) plus Automatic_Radiation_Partition_I.m and Precipitation_partition_Ding.m for radiation and precipitation partitioning.
  - T_and_C: A large collection of model functions (snow/ice albedo, radiation, hydrology, soil and vegetation processes, numerical kernels) and the main frame.
- Notes for running the model:
  - Inputs required: Ta, U, Ws, Rsw, Pr (precipitation); also latitude, longitude, elevation, and time zone.
  - Optional longwave radiation (Latm) can be provided or Cloudiness computed from S↓; albedo (Ameas) can be provided or modelled; air pressure can be provided or calculated.
  - Instrument heights can be static or time-varying depending on station type.
  - Snow snowfall threshold (Th_Pr_sno) and snow density/depth initial conditions are in PARAM_Peru.
  - Model outputs follow a defined flux sign convention and are later normalized for analysis.

## Tethys-Chloris model (application details)
- All model code for point-scale simulations is provided; run via T_and_C_Peru_EIDC.m.
- Model inputs include Ta, U, Ws, Rsw, Pr, Latm, Ameas, and other radiation/albedo parameters; cloudiness can be inferred if Latm is not provided.
- Albedo handling:
  - Ameas can be supplied or albedo computed from ice and snow parameterizations; options exist to force modelled albedo.
- Longwave radiation:
  - If Latm is not provided, cloudiness derived from S↓ is used; longwave emissivity and related parameters set in specific functions.
- Precipitation partition:
  - Details provided in Precipitation_partition.m (and supported by Ding 2014 partition method for undercatch corrections).
- Supporting references and parameter lists are included (TC_Variable_and_Parameter_List.pdf, TeC_technical_reference.pdf).

## Data quality, limitations, and notes for data stewards
- Gaps exist in Shallap data (late 2011–2012) and limited overlap between Shallap on-glacier and Shallap moraine datasets, limiting filling options for some variables.
- Cuchillacocha data rely heavily on relationships with off-glacier data during the dry/winter season due to short on-glacier records.
- Precipitation data include undercatch corrections and rely on measurements from multiple stations and WRF outputs; corrections involve assumptions (e.g., elevation-dependent lapse rates and hourly scaling of daily totals) that introduce uncertainties.
- Data products aim to preserve diurnal and seasonal cycles while reconciling differences between on-glacier and nearby off-glacier observations.
- Comprehensive metadata and data dictionaries are provided within the folder structure and the accompanying tables (e.g., Tables 1–4 describe corrections, stations, and filling steps).

## References
- Chubb et al. 2015; Ding et al. 2014; Fatichi et al. 2012; Mastrotheodoros et al. 2020; Nitu et al. 2018 (SPICE/WMO context).