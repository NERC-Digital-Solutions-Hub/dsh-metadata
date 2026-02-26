# This document describes the dataset submitted under filename BW_GUM_2018_2020.csv

- Provides a continuous time series of heat (latent and sensible) and trace gas (CO2 and CH4) fluxes measured by eddy-covariance, along with gas concentrations and ancillary meteorological data.
- Timeframe and resolution: 01/01/2018 to 31/12/2020, half-hourly intervals.
- Location: Guma Lagoon, Okavango Delta, Botswana (18°57'53.01"S, 22°22'16.20"E); study area over a Cyperus papyrus stand.
- Missing data: encoded as -9999.

## Data content and structure

- Measurements include:
  - Fluxes: sensible heat flux (H), latent heat flux (LE), CO2 flux (co2_flux), CH4 flux (ch4_flux).
  - Gas mole fractions: CO2, CH4, and water vapor (h2o_mole_fraction).
  - Meteorological and ancillary variables: wind_speed, wind_dir, ustar, stability, PAR, Rg (incoming radiation), RH, Pair (air pressure), Tair (air temperature), VPD.
- Quality flags:
  - qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (0 = good, 1 = fair, 2 = poor).
- Measurement specifics:
  - Sampling: 10 Hz for EC variables; 10-second interval for meteorology.
  - Data processed to half-hourly fluxes with EddyPro (v7.0.6) and quality-controlled by the project team.
- The document provides a Table 1 detailing variable names, units, and descriptions (including units like W m-2, μmol m-2 s-1, ppm, Pa, deg C).

## Study site context

- Okavango Delta overview: one of the world’s largest inland deltas, driven by pulsed river inflows and seasonal rainfall; broad hydrological and ecological diversity.
- Physiography and ecology: four zones (entry channel Panhandle, permanent swamp, seasonal swamp, occasional swamp); vegetation shifts with flooding (e.g., Cyperus papyrus in permanent swamps).
- Objective relevance: quantify greenhouse gas fluxes over a papyrus-dominated stand to inform carbon and methane dynamics in floodplain wetlands.

## Instrumentation, data collection, and processing

- Eddy-covariance instrumentation:
  - IRGASON (3D ultrasonic anemometer + open-path CO2 and H2O analyzer).
  - CH4 measurements with LI-COR 7700 open-path CH4 analyzer.
- Meteorological and environmental sensors:
  - Vaisala WXT520 for air temperature, pressure, RH, wind speed/direction.
  - Skye SKS1110 pyranometer and SKP215 quantum detector for PAR and total radiation.
- Setup:
  - Mounted on a 3 m tripod on a 3 m platform; measurement height ~5.5 m; papyrus mat canopy ~2.5 m tall.
  - Flux footprint primarily covers papyrus vegetation in the 60°–190° wind sector; data from other sectors (e.g., 180°–360°) should not be used due to heterogeneity.
- Data handling:
  - Data collected by CR3000 datalogger.
  - Maintenance: installation by Dr. Carole Helfter; monthly data collection by Dr. Mangaliso Gondwe.
  - Processing: EddyPro v7.0.6; quality control applied prior to release.

## Variables and metadata

- Table 1 (referenced) lists variable names, units, and descriptions including:
  - H, LE, co2_flux, ch4_flux; and their quality flags.
  - Gas mole fractions (co2_mole_fraction, ch4_mole_fraction, h2o_mole_fraction).
  - Meteorological and flux-related variables (VPD, wind_speed, wind_dir, ustar, stability, PAR, Rg, RH, Pair, Tair).
- Units provided for each variable (e.g., W m-2 for fluxes, μmol m-2 s-1 for gas fluxes, ppm for mole fractions, Pa for VPD, etc.).

## Data quality, caveats, and usage notes

- Quality flags indicate varying data reliability; users should filter or weight data according to qc_* values.
- Footprint and sector limitations imply spatial representativeness is best within the documented wind sector (60°–190°); extrapolation beyond this range may be inappropriate.
- Missing data indicated by -9999 should be handled as non-detects or gaps in analyses.
- The dataset is suited for quantifying greenhouse gas fluxes over a papyrus-dominated wetland patch and for examining environmental drivers under Okavango Delta hydrology.

## References and context

- The document cites foundational literature on Okavango Delta hydrology, geomorphology, vegetation, and methane emissions dynamics to contextualize the measurement site and observed fluxes.