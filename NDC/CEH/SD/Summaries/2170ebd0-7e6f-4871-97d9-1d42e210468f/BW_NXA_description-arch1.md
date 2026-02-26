# This document describes the dataset submitted under filename BW_NXA_2018-2020.csv

## Overview
- Continuous time-series of heat (latent and sensible) and trace gas (CO2 and CH4) fluxes
- Measurements: eddy-covariance fluxes, gas concentrations, and ancillary meteorological data
- Location: Nxaraga, south edge of Chief's Island, Okavango Delta, Botswana
- Period: 2018-01-01 to 2020-12-31
- Temporal resolution: half-hourly; missing data indicated as -9999

## Dataset scope and purpose
- Purpose: quantify greenhouse gas fluxes from seasonal floodplains
- Recorded variables include:
  - Fluxes: H (sensible heat), LE (latent heat), co2_flux, ch4_flux
  - Quality flags: qc_H, qc_LE, qc_co2_flux, qc_ch4_flux
  - Gas mole fractions: co2_mole_fraction, ch4_mole_fraction, h2o_mole_fraction
  - Meteorology: VPD, wind_speed, wind_dir, ustar, stability, PAR, Rg, RH, Pair, Tair
- Metadata-style table of variable names, units, and descriptions is provided

## Instrumentation and measurement site
- Instruments:
  - Ecosystem respiration and gas analysis: Campbell Scientific IRGASON + LI-COR 7700 CH4 analyser
  - Meteorology: Vaisala WXT520
  - Incoming radiation: Skye pyranometer (PAR) and SKP215 detector
- Data logging: Campbell CR3000
  - EC variables sampled at 10 Hz; meteorological parameters at 10-second intervals
- Setup:
  - 3-meter mast; effective EC measurement height ~2.5 m
  - Flux footprint focused on Papyrus-dominated floodplain (seasonal swamp)
  - Wind-sector guidance: valid fluxes from 60°–190° (general area); 130°–270° specifically for seasonal floodplain
- Site context:
  - Floodplain features: papyrus mat, reeds, grasses; presence of hippos and elephants
  - Vegetation and wildlife influence on fluxes around riparian zones
- Maintenance and processing:
  - Installation and upkeep by researchers from okavango projects
  - Raw data processed to half-hourly fluxes with EddyPro v7.0.6
  - Quality control performed by project leads

## Data processing and quality indicators
- Missing data:
  - Occur due to instrument downtime; represented as -9999
- Quality flags:
  - qc_H, qc_LE, qc_co2_flux, qc_ch4_flux: 0 = good, 1 = fair, 2 = poor
- Data products:
  - Half-hourly fluxes and associated meteorological variables
  - Documentation includes a detailed variable description table

## Data quality caveats and considerations
- Flux estimates are valid primarily within specified wind sectors due to spatial heterogeneity and roughness elements
- Edges of footprint and non-standard wind directions may yield unreliable results
- Local environmental factors (seasonal flood dynamics, vegetation, wildlife activity) may influence flux measurements

## Applications and use cases
- Ideal for analysing GHG fluxes in tropical floodplain ecosystems
- Supports modeling of CO2 and CH4 dynamics in seasonal wetlands
- Useful for cross-site comparisons and understanding the influence of hydrology on gas exchange in the Okavango Delta

## References
- References 1–6 detailing hydrology, sedimentology, vegetation, and methane dynamics in the Okavango Delta and vicinity (as listed in the document)