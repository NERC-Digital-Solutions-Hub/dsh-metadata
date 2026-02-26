# This document describes the dataset submitted under filename BW_NXA_2018-2020.csv

## Overview
- Continuous time series of heat (latent and sensible) and trace gas (CO2 and CH4) fluxes obtained by eddy-covariance, along with gas concentrations and ancillary meteorological data.
- Data interval: half-hourly for 2018-01-01 to 2020-12-31.
- Missing data indicated as -9999 due to instrumentation downtime.
- Includes CO2 and CH4 fluxes, gas mole fractions, and standard meteorological variables (temperature, humidity, pressure, PAR, radiation, wind, etc.).

## The Okavango Delta context
- One of the world’s largest inland deltas (≈40,000 km2) in northern Botswana; seasonally flooded with a pulse-discharge hydrology.
- Flooding regime controlled by river discharge and rainfall; evaporation dominates water loss.
- Delta divided into physiographic zones: entry channel, permanent swamp, seasonal swamp, occasional swamp.
- Vegetation and habitat (papyrus channels, grasses) influence fluxes; notable wildlife activity (hippos, elephants) and grazing in floodplains.

## Instrumentation and measurements site
- Fluxes measured using eddy-covariance: IRGASON (3D sonic anemometer + open-path CO2/H2O analyzer) and LI-COR 7700 CH4 analyzer.
- Meteorology from Vaisala WXT520; solar radiation from Skye pyranometer; PAR from a quantum detector.
- Data logging: Campbell Scientific CR3000; EC data at 10 Hz; meteorological data at 10-second intervals.
- Mounting: 3-meter mast (effective measurement height ~2.5 m) on Chief’s Island edge; flux footprint focused on papyrus-dominated floodplain vegetation.
- Data processing and QA: EddyPro software (v7.0.6); quality control performed by Dr. Helfter.

## Data structure and variables
- Fluxes and related metrics:
  - H (Sensible heat flux), LE (Latent heat flux)
  - co2_flux (CO2 flux, μmol m^-2 s^-1)
  - ch4_flux (CH4 flux, μmol m^-2 s^-1)
  - qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (quality flags; 0 = good, 1 = fair, 2 = poor)
- Gas concentrations and related metrics:
  - co2_mole_fraction (ppm), h2o_mole_fraction (ppthou), ch4_mole_fraction (ppm)
  - VPD (Pa)
- Meteorological and environmental context:
  - wind_speed (m s^-1), wind_dir (deg)
  - ustar (m s^-1), stability (dimensionless)
  - PAR (μmol m^-2 s^-1), Rg (W m^-2)
  - RH (%), Pair (hPa), Tair (°C)

## Data quality, usage notes, and caveats
- Missing data denoted by -9999.
- Quality flags indicate data reliability; users should filter by qc_ fields as appropriate.
- Footprint limitations: data from certain wind sectors should be excluded due to non-homogeneous roughness elements (trees/shrubs); flux estimates are most reliable within specified sectors (e.g., 60°–190° for the main floodplain, 130°–270° for the seasonal floodplain).
- Ecological context (vegetation, large herbivores) may influence fluxes and should be considered when interpreting results.

## Provenance and references
- Instrumentation and site setup documented by the researchers (Dr. Carole Helfter; Dr. Mangaliso Gondwe).
- Data processed with EddyPro; QA performed during data curation.
- References related to the Okavango Delta and instrumentation are provided for background and methodological context.