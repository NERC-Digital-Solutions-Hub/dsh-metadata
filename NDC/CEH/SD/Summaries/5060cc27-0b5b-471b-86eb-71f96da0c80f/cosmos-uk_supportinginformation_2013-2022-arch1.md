# Supporting documentation for COSMOS-UK. Stanley et al. (2023). Daily and sub-daily hydrometeorological and soil data (2013-2022) [COSMOSUK]. NERC Environmental Information Data Centre.

## Overview
- A comprehensive COSMOS-UK data collection covering 51 sites from October 2013 to December 2022.
- Includes sub-hourly (30-minute) and daily hydrometeorological and soil data, along with extensive metadata and quality control information.
- Data are distributed across 258 files, encompassing site metadata, sub-hourly data and flags, daily data, and derived variables (e.g., VWC, PE, SWE, albedo, GCC).
- Data hosted via COSMOS-UK website and the NERC Environmental Information Data Centre (EIDC).

## Data structure and contents
- Sub-hourly data (30-minute resolution) and related metadata:
  - File: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022.csv
  - Metadata: COSMOS-UK_HydroSoil_SH_2013-2022_Metadata.csv
  - Variables include radiative fluxes (LWIN, LWOUT, SWIN, SWOUT, RN), precipitation (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), atmospheric pressure (PA), air temperature (TA), wind (WS, WD, UX, UY, UZ), humidity (Q, RH), snow depth (SNOW_DEPTH), soil temperature and moisture at multiple depths (TDTx, VWC sensors, STP_TSOILx, TDTx_VWC), heat fluxes (G1, G2), snow and albedo-related metrics (SNOW, SWE, ALBEDO), and derived variables (PE, GCC, COSMOS_VWC, CTS_MOD_CORR, D86_75m, SNOW_DEPTH).
  - Timestamp end of each 30-minute period; values logged hourly to central system.
  - Missing values coded as -9999.
- Daily data (resolution: daily):
  - File: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022.csv
  - Metadata: COSMOS-UK_HydroSoil_Daily_2013-2022_Metadata.csv
  - Derived and summarized variables at daily scale: volumetric water content (VWC) derived from CRNS counts, potential evapotranspiration (PE) via Penman-Monteith, snow water equivalent (SWE), net radiation (RN), and other components (precipitation sums, air temperature, RH, wind, etc.). Albedo and GCC are included as daily items.
- QC and data flags:
  - Sub-hourly QC Flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv
  - Sub-hourly Data Flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Flags.csv
  - Daily Flags: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022_Flags.csv
  - Flag codes and meanings documented in the tables accompanying Section 3.6 and 3.7.
- Instrumentation details and site-specific setups are described in Section 7, with comprehensive listing of instruments and configurations across sites and over time.

## Quality control and flags
- Two-stage quality control (QC):
  - Automatic QC: processing script applies tests to relevant variables; failing data are flagged and removed.
  - Daily visual QC: manual review of plots.
- QC flags:
  - Each QC test yields a dedicated flag value; flags for failed tests are summed to a unique value per data point.
  - QC flags are stored in separate QC flag files (structure mirrors data files with _QCFLAG suffix).
  - Net radiation (RN) and absolute humidity (Q) are not QC’d because they are derived from QC’d inputs.
- Data flags:
  - Four data flags: M (Missing), U (Unchecked), I (Infilled), E (Estimated).
  - Data flag files accompany the data files and indicate data quality and infilling status (e.g., infilled values).
- Data provenance:
  - QC flags explain why data were removed; data flags indicate infilling or estimation status of data values.

## Derived data and methods
- Volumetric water content (VWC):
  - Derived from corrected cosmic-ray neutron sensor (CRNS) counts (CTS_MOD_CORR), with corrections for background cosmic ray intensity, altitude, atmospheric pressure (PA), and absolute humidity (Q).
  - Calibration methods include site-specific N0, universal hydrogen molar fraction (hmf), and neutron transport models; COSMOS-UK uses site-specific N0 calibration with lattice water and soil organic carbon corrections.
  - VWC aggregation and daily values described; 30-minute counts are telemetered hourly and daily averages produced.
- SWE and snow days:
  - Snow days identified via albedo thresholds (average albedo 10:00–14:00 GMT: >50% indicates snow day; <35% end).
  - SWE estimated from the difference between measured daily counts and snow-free count estimates (Method 1, Wallbank et al. 2020); generates daily SWE values alongside snow-free VWC.
- Potential evapotranspiration (PE):
  - Derived from sub-hourly data using Penman-Monteith (FAO 56, 1998); requires RN, G (mean of G1 and G2), TA, RH, WS, and PA.
- Green colour content (GCC):
  - Derived from PhenoCam imagery; green proportion computed after masking; daily GCC is the maximum of daily images.
  - Note: GCC data have not undergone quality control.
- Completeness:
  - Site- and variable-level completeness metrics are provided (e.g., Met, Soil, and VWC completeness categories).

## Infilling
- Infilling fills gaps in time series for selected variables using interpolation:
  - Linear interpolation or order-2 polynomial interpolation, chosen based on gap size and surrounding data.
  - Gap criteria: up to 10 consecutive values; method choice depends on surrounding data points and RMSE testing.
  - RMSE-based evaluation performed by simulating artificial gaps to select the best interpolation method for each variable.

## Completeness
- A dedicated table reports data completeness for each site across data groups (Met, Soil, and VWC); VWC completeness pertains to CRNS-derived soil moisture. Specific percentages are provided in the table within the document.

## Instrumentation
- Core instruments across the COSMOS-UK network:
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (VWC) with counts corrected for atmospheric pressure, humidity, and cosmic ray intensity.
  - Radiometer (upward/downward) for net radiation (RN) and shortwave/longwave components.
  - Rain gauges (OTT Pluvio 1) and tipping bucket (RainE) for precipitation measurements.
  - Time Domain Transmissometry (TDT) soil moisture sensors and soil temperature sensors at multiple depths.
  - Soil heat flux plates (0.03 m depth).
  - Automatic weather station (AWS) for air temperature and humidity; barometric pressure sensor; wind sensors (3D sonic and integrated windsonic).
  - PhenoCam system for GCC derived from images.
  - PhenoCam and associated masks provide site-specific greenness indices.
- Instrumentation varies by site and over time (see Tables 7.1–9 in the document for setup types and site-specific configurations).

## Changes to data
- The dataset undergoes ongoing review and reprocessing when improvements are made. Major changes include:
  - Feb 2023: Hollin Hill VWC reprocessed due to calibration issues; correction factors applied; heat flux values at 00:30 and 01:00 removed.
  - 2021–2023: updates to gamma values, N0_MOD, bulk density recalibration, D86_75m correction, and various recalibrations.
  - Jul 2020–2022: VWC calibration updates; CRNS counts infilled from secondary tubes; NMDB data infilling; improvements to 30-minute precipitation processing.
  - Dec 2019: SWE addition; daily albedo added; mid-day SWN/SWOUT derivation updates.
- These changes may lead to reprocessing of past data to maintain consistency.

## Author contributions
- S. Stanley: primary author and point of contact.
- Data management and site metadata compilation by multiple contributors.
- Data processing, instrumentation setup, calibration, and maintenance contributions by a large team.
- Derived data processing, analysis, and interpretation conducted by several collaborators.

## Access and use notes for analysts
- Data are provided with detailed metadata, QC, and data flags to support traceability and reproducibility.
- -9999 is the placeholder for missing values; QC and data flags indicate infilling or estimation statuses.
- Derived products (e.g., VWC from CRNS, SWE, PE, GCC) should be used with awareness of their derivation methods and associated uncertainties.
- GCC data are not quality-controlled; treat GCC cautiously in analyses.
- Data volumes are large and multi-file; ensure metadata cross-referencing to align site IDs and timeframes.