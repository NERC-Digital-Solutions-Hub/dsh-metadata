# BW_GUM_2018_2020.csv

## Overview
- A continuous time series of heat (latent and sensible) and trace gas (CO2 and CH4) fluxes obtained by eddy-covariance, plus gas concentrations and ancillary meteorological data.
- Location: Guma Lagoon, Okavango Delta, Botswana, targeting a Cyperus papyrus stand.
- Time period: 01/01/2018 to 31/12/2020; temporal resolution: half-hourly fluxes; missing data encoded as -9999.

## Data content and variables
- Fluxes and related variables:
  - H (sensible heat flux), LE (latent heat flux), co2_flux (CO2 flux), ch4_flux (CH4 flux)
  - Quality flags: qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (0 = good, 1 = fair, 2 = poor)
- Gas concentrations and environmental state:
  - co2_mole_fraction, h2o_mole_fraction, ch4_mole_fraction
  - VPD, wind_speed, wind_dir, ustar, stability
  - PAR, Rg, RH, Pair, Tair
- Units and detailed descriptions are provided in the accompanying variable table (Table 1).

## Study site and ecosystem context
- The Okavango Delta is a large inland delta (~40,000 km2) with annual flooding from Cubango and Quito rivers.
- Flooding and evapotranspiration shape vegetation; four physiographic zones (entry channel, permanent swamp, seasonal swamp, occasional swamp) with papyrus-dominated wetlands in permanent/swamps.
- Vegetation and hydrology influence GHG flux dynamics.

## Instrumentation and data collection
- Eddy-covariance principle: fluxes derived from covariance between vertical wind speed and gas concentrations.
- Instrumentation:
  - IRGASON (3D ultrasonic anemometer + open-path CO2/H2O)
  - LI-COR 7700 open-path CH4 analyser
  - Vaisala WXT520 weather station (air temperature, pressure, RH, wind speed/direction)
  - Skye Instruments pyranometer (total incoming radiation) and quantum detector (PAR)
  - Campbell Scientific CR3000 datalogger (10 Hz EC data; 10 s meteorological data)
- Deployment: mounted on a 3 m high tripod on a 3 m platform; effective measurement height ~5.5 m; canopy height ~2.5 m above water.
- Flux footprint mainly covers papyrus vegetation in the 60°–190° wind sector; data from other sectors (notably 180°–360°) should be used with caution due to non-homogeneous roughness elements.

## Data processing and quality assurance
- Raw data processed into half-hourly fluxes using EddyPro software v7.0.6.
- Quality-controlled by named personnel (quality flags indicate data reliability: 0 = good, 1 = fair, 2 = poor).

## Accessibility and metadata
- The dataset includes a comprehensive variable table with names, units, and descriptions to support reuse.
- Metadata and data processing steps (including processing software) are documented to assist discoverability and usability.

## References
- Cited works related to Okavango Delta hydrology, vegetation, methane emissions, hydrological dynamics, and papyrus wetlands.