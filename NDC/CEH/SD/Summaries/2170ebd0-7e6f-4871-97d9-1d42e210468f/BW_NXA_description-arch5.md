# This document describes the dataset submitted under filename BW_NXA_2018-2020.csv

## Overview
- Continuous half-hourly time series of heat (latent and sensible) and trace gas (CO2 and CH4) fluxes estimated by eddy-covariance, gas concentrations, plus ancillary meteorological data.
- Data period: 01/01/2018 to 31/12/2020.
- Missing data represented as -9999.
- Context:Nxaraga, south edge of Chief's Island, Okavango Delta, Botswana; purpose is to quantify greenhouse gas fluxes from seasonal floodplains.

## Dataset scope and purpose
- Measures greenhouse gas fluxes from seasonal floodplains using eddy-covariance methods.
- Includes energy fluxes (H, LE) and gas fluxes (co2_flux, ch4_flux) with associated quality flags.
- Also provides environmental variables and gas mole fractions to support interpretation and processing.

## Location and site context
- Okavango Delta: large inland delta with seasonal flooding influenced by Cubango/Quito river discharge and rainfall.
- Site specifics: 3 m EC mast on the SW edge of Chief's Island; effective measurement height 2.5 m.
- Flux footprint and sector limitations:
  - Seasonal floodplain fluxes: wind sectors 130°–270°.
  - Papyrus vegetation area: flux footprint 60°–190°.
  - Data from other wind sectors should not be used due to roughness elements compromising spatial homogeneity.

## Instrumentation and data collection
- Eddy-covariance system: Campbell Scientific IRGASON (3D sonic anemometer + open-path CO2/H2O analyzer) and LI-COR 7700 CH4 analyzer.
- Meteorology: Vaisala WXT520 (air temperature, pressure, RH, wind speed/direction).
- Radiation: Skye Instruments pyranometer (PAR) and quantum detector.
- Logger: Campbell Scientific CR3000; EC variables sampled at 10 Hz; meteorological parameters at 10 s.
- Site maintenance and processing:
  - Instrumentation installed by Dr. Carole Helfter.
  - Monthly data collection and maintenance by Dr. Mangaliso Gondwe.
  - Raw data processed to half-hourly fluxes using EddyPro v7.0.6; quality controlled by Dr. Helfter.

## Data processing and quality control
- Processing: EddyPro 7.0.6 to derive half-hourly fluxes.
- Quality control: implemented by principal investigator; includes quality flags for all flux and related variables.
- Variables included with descriptions and units (see table in document):
  - H (sensible heat flux), LE (latent heat flux)
  - co2_flux (CO2 flux), ch4_flux (CH4 flux)
  - QC flags: qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (0 = good, 1 = fair, 2 = poor)
  - Gas mole fractions: co2_mole_fraction, h2o_mole_fraction, ch4_mole_fraction
  - Meteorological and environmental: VPD, wind_speed, wind_dir, ustar, stability, PAR, Rg, RH, Pair, Tair

## Data structure and variables (highlights)
- Fluxes: H, LE, co2_flux, ch4_flux with corresponding qc flags.
- Gas constituents: co2_mole_fraction, h2o_mole_fraction, ch4_mole_fraction (ppm/ppthou).
- Atmospheric and flux context: VPD, wind_speed, wind_dir, ustar, stability.
- Radiation and climate context: PAR, Rg, RH, Pair, Tair.
- Data conventions:
  - Flux signs: negative values denote fluxes toward the surface.
  - Missing data: encoded as -9999.

## Dataset provenance and governance considerations
- Clear documentation of instrument types, measurement heights, footprint limits, and data processing steps enhances data discoverability and reuse.
- Metadata provides explicit variable names, units, and descriptive descriptions to support interoperability.
- Data quality is tracked via QC flags to inform users about reliability (good, fair, poor).
- Governance notes for data stewards:
  - Track dataset versioning and processing history (EddyPro version and QC procedures).
  - Document any embargoes, access restrictions, or licensing not specified in the source.
  - Ensure proper attribution to contributors (investigators and data processors) and maintain metadata fidelity for discoverability and reuse.