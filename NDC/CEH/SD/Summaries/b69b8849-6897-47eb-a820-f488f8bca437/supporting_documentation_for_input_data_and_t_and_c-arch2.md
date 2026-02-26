# The energy and mass balance of Peruvian glaciers

## Overview
- Data from the Peru GROWS and PEGASUS projects, funded by NERC and CONCYTEC; Peruvian portion aligned with Glacier Research Circles.
- Associated with the paper: The energy and mass balance of Peruvian glaciers (accepted in Journal of Geophysical Research: Atmospheres).
- Purpose: provide hourly, on-glacier meteorological inputs and modelling framework (Tethys-Chloris) to quantify melt and mass balance at five Peruvian glaciers.
- Outputs are prepared for standardised analysis, with datasets and code intended for reuse and integration with other environmental data and policy-relevant assessments.

## Data collection and sites
- On-glacier weather stations used for modelling:
  - Shallap Glacier (SG), Artesonraju Glacier (AG), Cuchillacocha Glacier (CG), Quisoquipina Glacier (QQG), Quelccaya Ice Cap (QIC).
- Supporting off-glacier/donor data used to fill gaps and extend time series where appropriate.
- Data sources include multiple universities and national agencies; some inputs also include WRF (Weather Research and Forecasting) model outputs.
- Modelling period focuses on site-specific on-glacier data, with certain periods modelled using relationships to off-glacier data or WRF.

## Data cleaning and correction
- Rigorous quality control prior to analysis:
  - Remove clearly erroneous data; cap or correct values to plausible ranges.
  - Remove zero wind speeds (to avoid non-physical fluxes); fill gaps with monthly diurnal averages.
  - Inspect large jumps in variables (e.g., air temperature >10°C changes, RH >40% changes) and remove if erroneous.
  - Remove consecutive identical values (six in a row, except where valid).
- Gaps filled using nearest-off-glacier data, same-station data from other years, or WRF outputs; aim to preserve diurnal and seasonal cycles.
- Specific notes per station (SG, AG, CG, CQ, Morder, Santiago) detailing donor data and correction methods for each variable (Ta, RH, WS, S↓, S↑, L↓, L↑, Pr, SR50).
- Precipitation corrections include undercatch adjustments for snow/ice conditions (notably for CQ and Santiago data) and conversion of daily sums to hourly values when needed.
- Data corrections are documented in tables and accompanied by site-specific validation checks where possible.

## Tethys-Chloris model
- All model code is provided for transparency and reuse.
- Main run workflow:
  - T_and_C_Peru_EIDC.m drives the modelling, with PARAM_Peru.m configuring non-site-specific parameters and Automatic_Radiation_Partition_I.m files handling radiation partitioning.
  - Main_run_code includes site-specific radiation partitioning, precipitation partitioning (Ding et al.), and the primary model run file MAIN_FRAME.m.
- Input requirements and flexibility:
  - Requires hourly Ta, RH, Ws, Rsw, Pr (and optionally Latm/L↑ for longwave, cloudiness, albedo).
  - Optional inputs for longwave radiation and albedo; model can compute these if not provided.
  - Instrument heights can be static or hourly (zatm_hourly_on flag).
  - Snow/ice parameters, snow density, initial conditions, and other snow/ice physics are configurable via PARAM_Peru and model files.
- Notes for users:
  - The model is described for clean ice/snow surfaces; site-specific input paths and parameters must be updated for new sites.
  - Output flux directions follow the technical reference and are adjusted in subsequent analysis code to be downward-positive.
  - Full parameter and model structure details are in TC_Variable_and_Parameter_List.pdf and TeC_technical_reference.pdf.

## Data structure and units
- Three main folders with data and code:
  - Input_data: cleaned on-glacier meteorological inputs (mat files for model, and CSV files for run-time inputs).
    - CSV fields include: Datetime, Ta (°C), Pr (mm h-1), U (fraction), Ws (m s-1), Rsw (W m-2), Rsw_out, Latm (W m-2), L_out, NetR, SR_50 (m), zatm_hourly_m (m), Ameas (albedo).
    - NaNs indicate missing data; not all variables available at every station.
  - Main_run_code: site-specific run files (e.g., CG_Automatic_Radiation_Partition_I.m, Peru_Automatic_Radiation_Partition_I.m, Precipitation_partition_Ding.m, T_and_C_Peru_EIDC.m).
  - T_and_C: extensive library of model functions (numerous modules for radiation, albedo, hydrology, soil, vegetation, etc.).
- Data availability:
  - Input_data contains on-glacier inputs after cleaning/filling, with corresponding CSVs prepared for direct use in the modelling run.
  - Documentation clarifies unit conventions and variable definitions to aid standardised analyses and cross-study comparability.

## Reproducibility, use, and integration
- Clear instructions to run the model, including updating pathnames, input data, time zones, coordinates, and site parameters.
- Outputs follow standard environmental modelling conventions and can be used for time-series analyses, dataset integration, and policy monitoring when coupled with other climate/environmental datasets.
- Emphasises the importance of making underlying data accessible and usable by others to enable broader scrutiny and reuse.

## References and methodological basis
- Precipitation partitioning and undercatch corrections based on:
  - Ding et al. (2014) precipitation partition algorithm.
  - Chubb et al. (2015) wind-induced undercatch corrections for unshielded gauges.
- Ecohydrological modelling framework:
  - Fatichi et al. (2012a, 2012b) mechanistic ecohydrological modelling.
  - Mastrotheodoros et al. (2020) related climate-impacts findings.
- SPICE/WMO references for precipitation intercomparison context (Nitu et al. 2018) and related methodologies.