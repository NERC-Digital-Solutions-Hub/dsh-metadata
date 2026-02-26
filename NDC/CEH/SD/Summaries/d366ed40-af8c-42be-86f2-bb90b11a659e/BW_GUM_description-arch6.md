# This document describes the dataset submitted under filename BW_GUM_2018_2020.csv

## Overview
- Continuous time-series dataset of heat fluxes (latent and sensible), trace gas fluxes (CO2 and CH4), gas concentrations, and ancillary meteorological data.
- Location: Guma Lagoon, Okavango Delta, Botswana (18°57'53.01"S; 22°22'16.20"E).
- Study objective: quantify greenhouse gas fluxes over a Cyperus papyrus stand.
- Temporal coverage: 01/01/2018 to 31/12/2020.
- Temporal resolution: half-hourly fluxes; raw data collected at 10 Hz (EC) and 10 s (meteorology); processed into half-hourly values.
- Data completeness: missing data recorded as -9999 due to instrument downtime.
- Data processing: half-hourly fluxes produced using EddyPro software (v7.0.6) with quality control.

## Data Content and Variables
- Fluxes
  - H: sensible heat flux (W m^-2); qc_H quality flag (0 good, 1 fair, 2 poor)
  - LE: latent heat flux (W m^-2); qc_LE quality flag
  - co2_flux: carbon dioxide flux (μmol m^-2 s^-1); negative values indicate fluxes towards the surface; qc_co2_flux
  - ch4_flux: methane flux (μmol m^-2 s^-1); negative values indicate fluxes towards the surface; qc_ch4_flux
- Gas concentrations and humidity
  - co2_mole_fraction: CO2 mole fraction (ppm)
  - h2o_mole_fraction: water vapour mole fraction (ppthou)
  - ch4_mole_fraction: CH4 mole fraction (ppm)
  - VPD: vapour pressure deficit (Pa)
  - RH: relative humidity (%)
  - Pair: atmospheric pressure (hPa)
  - Tair: air temperature (°C)
- Meteorological and radiation variables
  - wind_speed: wind speed (m s^-1)
  - wind_dir: wind direction (degrees)
  - ustar: friction velocity (m s^-1)
  - stability: atmospheric stability parameter
  - PAR: photosynthetically active radiation (μmol m^-2 s^-1)
  - Rg: total incoming radiation (W m^-2)
- Additional context
  - Data is limited to the flux footprint 60°–190° due to presence of roughness elements (trees/shrubs) outside this sector to satisfy spatial homogeneity assumptions of eddy-covariance theory.

## Study Site Context
- The Okavango Delta is a large, seasonal inland delta subject to pulsed river discharge and heavy evapotranspiration; flood dynamics control vegetation and hydro-ecology.
- The study area focuses on a Cyperus papyrus stand within a papyrus mat near Guma Lagoon, with canopy height around 2.5 m.
- The flux footprint and vegetation structure influence energy balance and greenhouse gas emissions captured in the dataset.

## Instrumentation and Data Processing
- Eddy-covariance system: IRGASON (ultrasonic anemometer + open-path CO2/H2O analyzer) and LI-COR 7700 CH4 analyzer.
- Environmental sensors: Vaisala WXT520 (air temperature, pressure, humidity, wind), Skye pyranometer (PAR), Skypa quantum detector (PAR), CR3000 data logger (10 Hz EC; 10 s meteorology).
- Mounting: sensors on a 3 m tripod on a 3 m platform; effective measurement height ~5.5 m; footprint focused on papyrus stand.
- Data processing and QC: processed into half-hourly fluxes with EddyPro v7.0.6; quality controlled by Dr Helfter; monthly maintenance by Dr M. Gondwe.
- Data availability note: missing data labeled as -9999; quality flags indicate data reliability (0 = good, 1 = fair, 2 = poor).

## Data Quality and Use Considerations
- Quality flags accompany flux variables to guide data usability.
- Restriction to specific wind sector (60°–190°) to maintain spatial homogeneity; avoid using data from other sectors due to proximate roughness elements.
- Users should handle -9999 as missing values and consider flag quality when analyzing fluxes or aggregating data.

## Potential Data Products and Uses (Data Support Perspective)
- Self-serve dashboards and time-series views of H, LE, CO2 flux, and CH4 flux with associated meteorological context.
- Aggregations (daily, monthly, seasonal) and flux partitioning analyses over the papyrus stand.
- Correlations and cross-plots between gas fluxes and environmental drivers (PAR, Rg, Tair, RH, VPD, wind variables).
- Comparative analyses with other Okavango Delta datasets (hydrology, vegetation dynamics) to explore land-water interactions and greenhouse gas dynamics.
- Data integration guidance: treat qc flags and -9999 appropriately; align timestamps; ensure consistency of units; consider footprint limitations when comparing with other sites.

## Access, Metadata, and References
- Dataset filename: BW_GUM_2018_2020.csv
- References (background for context and methodology):
  - Gumbricht et al. (2004, 2004) on channels, wetlands, and hydrology of the Okavango Delta
  - Gumbricht et al. (2001) on topography and tectonics implications
  - Gondwe & Masamba (2014) on methane diffusion dynamics
  - McCarthy et al. (1998) on hydrology and geohydrology
  - Bonyongo et al. (2000) on papyrus wetland vegetation