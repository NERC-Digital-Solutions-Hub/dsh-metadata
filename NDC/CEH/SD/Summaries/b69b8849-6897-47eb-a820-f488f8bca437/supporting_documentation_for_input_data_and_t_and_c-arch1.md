# The energy and mass balance of Peruvian glaciers

## Overview
- A dataset created as part of the Peru GROWS and PEGASUS projects, funded by NERC and CONCYTEC, supporting the study of glacier energy and mass balance in Peru.
- Data underpin a paper on energy and mass balance of Peruvian glaciers and are derived from multiple field stations across the Cordillera Blanca and Cordillera Vilcanota.
- The dataset includes cleaned meteorological inputs, model code (Tethys-Chloris), and detailed data processing steps to enable point-scale glacier melt and mass-balance simulations.

## Data provenance and scope
- Weather data originate from on-glacier stations at Shallap Glacier (SG), Artesonraju Glacier (AG), Cuchillacocha Glacier (CG), Cuchillacocha Quilcay (CQ), Quelccaya Ice Cap (QIC), and Quisoquipina Glacier (QQG); plus nearby off-glacier donor stations used for data filling.
- Input variables cover: air temperature (Ta), relative humidity (RH), wind speed (Ws), incoming/outgoing shortwave radiation (S↓/S↑), incoming longwave radiation (Latm), precipitation (Pr), snow depth (SR50), and derived albedo (Ameas).
- Data were gathered from multiple institutions and portals; some datasets were modelled (e.g., WRF) or filled from nearby stations when gaps existed.

## Data cleaning and quality assurance
- Meteorological data underwent rigorous cleaning: removal of clearly erroneous values, cap corrections (e.g., RH limited to 100%), and radiation bounds (S↑, S↓ non-negative; S↑ ≤ S↓).
- Zero wind speeds were removed or replaced with hourly monthly diurnal averages to avoid bias in turbulent flux calculations.
- Large jumps and stagnation were inspected and corrected; gaps were filled using nearby stations, same-station data from other years, or model outputs (e.g., WRF) as described in the data tables.
- Specific, station-by-station cleaning and filling rules are detailed in the accompanying methods tables.

## Data corrections and filling (highlights)
- On-glacier and off-glacier relationships were used to fill missing data, with care to preserve diurnal/seasonal cycles.
- Precipitation data used a combination of on-glacier gauges and corrected daily sums from nearby stations, applying elevation-adjusted undercatch corrections where appropriate.
- Snow/wind/radiation corrections employed site-specific transfer relationships and, where necessary, model-derived inputs to maintain consistency across stations.
- Data for Shallap, Artesonraju, Cuchillacocha, Quelccaya, and Quisoquipina involved bespoke filling regimes due to gaps, with clearly documented donor relationships and correction procedures.

## The Tethys-Chloris model (TC) and run setup
- All TC modelling code is provided; primary workflow is via T_and_C_Peru_EIDC.m, which orchestrates data loading, site-specific parameterization (PARAM_Peru), and the main frame (MAIN_FRAME.m) for model runs.
- The model simulates energy and mass balance at hourly time steps on glacier surfaces (ice/snow) with configurable inputs:
  - Required inputs: Ta, RH, Ws, Rsw, Pr (and optional Latm); longwave may be provided or computed from cloudiness.
  - Albedo: either measured (Ameas) or modelled via snow/ice albedo parameterisations.
  - Pressure and instrument heights: populated from inputs or calculated.
  - Snow snowfall partitioning: uses either Ding et al. (2014) approach or the default partition within TC.
- Documentation notes cover model operation, input formatting, time zones, and site-specific radiation partitioning (Peru_Automatic_Radiation_Partition_I.m for most sites; CG-specific partition due to shading).
- The dataset includes extensive parameter lists and references (TC_Variable_and_Parameter_List.pdf; TeC_technical_reference.pdf).

## Data structure and units
- Provided as three folders to facilitate reproducible modelling:
  - Input_data: cleaned on-glacier meteorological timeseries in .mat and .csv formats, ready for T_and_C_Peru_EIDC.m. Includes:
    - Datetime, Ta (°C), Pr (mm h−1), U (fraction), Ws (m s−1), Rsw (W m−2), Rsw_out, Latm (W m−2), L_out, NetR, SR_50 (m), zatm_hourly_m (instrument heights), Ameas (albedo).
    - NaNs indicate missing data; not all variables available at every station.
  - Main_run_code: includes scripts for radiation partition, parameter files, and the main run file (T_and_C_Peru_EIDC.m; PARAM_Peru.m; Peru_Automatic_Radiation_Partition_I.m; Precipitation_partition_Ding.m).
  - T_and_C: extensive model function library covering aerodynamic resistance, albedo properties, canopy/biogeochemistry modules, radiation transfer, snow/ice processes, and the full TC modelling framework.
- Outputs (model-ready inputs) are prepared for the run file; final data corrections prior to modelling are performed within MATLAB.

## Practical implications for data analysts
- The dataset provides a reproducible, well-documented pipeline from raw meteorological observations to hourly glacier energy and mass-balance modelling.
- It highlights common challenges for analyst-led data work in complex field settings:
  - Gaps and scale mismatches addressed via donor stations and modelling, with transparent limitations (e.g., Shallap gap during a period with no overlap for certain datasets).
  - Off-glacier data used to fill near-surface conditions, with elevation and diurnal-cycle adjustments.
  - Under-ice shading and site-specific radiation partitioning handled through bespoke routines, particularly important for CG.
- The combination of cleaned inputs, detailed correction rules, and modular TC code enables replication, sensitivity checks, and extension to other glacier systems.

## References and related methodology
- Chubb et al. (2015) wind-induced precipitation gauge corrections.
- Ding et al. (2014) precipitation partition and snowfall processing.
- Fatichi et al. (2012a, 2012b) mechanistic ecohydrological modelling framework.
- Mastrotheodoros et al. (2020) climate/green-blue water dynamics context.
- Nitu et al. (2018) SPICE precipitation intercomparison context (undercatch corrections).
- Associated TC documentation: TC_Variable_and_Parameter_List.pdf; TeC_technical_reference.pdf.