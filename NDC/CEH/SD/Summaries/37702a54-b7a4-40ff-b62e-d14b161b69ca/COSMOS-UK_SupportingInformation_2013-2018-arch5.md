# Daily and sub-daily hydrometeorological and soil data (2013-2018) [COSMOSUK]

## Overview
- A comprehensive COSMOS-UK data package covering 50 sites from Oct 2013 to Dec 2018.
- Includes sub-hourly (30-minute) and hourly hydrometeorological and soil data, plus daily derivatives.
- Data organized into 201 files: site metadata, sub-hourly data and QC flags, hourly VWC, and daily VWC with related metrics (PE and SWE).

## Data structure and metadata
- Primary files:
  - COSMOS-UK_SiteMetadata_2013-2018.csv: site locations, IDs, start/end dates, soil type, bulk density, soil organic carbon, land cover.
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018.csv: sub-hourly data (30-minute resolution) with variables such as radiation components, precipitation, air temperature, humidity, pressure, wind, humidity, snow depth, wind components, soil temperatures and VWC at various depths.
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018_QC_Flags.csv: QC flags for sub-hourly data (aligned with data columns, suffixed with _QCFLAG).
  - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2018.csv: hourly VWC (COSMOS_VWC) and derived variables (D86, etc.).
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2018.csv: daily VWC (COSMOS_VWC), daily D86, PE, SWE, SNOW, and ALBEDO.
- Missing values consistently coded as -9999 in data files.
- Timestamp conventions:
  - Sub-hourly: DATE_TIME end of the 30-minute period (e.g., 12:30 refers to 12:00–12:30).
  - Daily: DATE_TIME represents 00:00 for the day (start of the 24-hour period).

## Data processing and quality control
- Data flow: instruments feed loggers on-site; data telemetered hourly to CEH Wallingford; two-stage QC applied before dataset release.
- QC stages:
  - Automatic QC tests run via processing scripts; failing data are flagged and removed.
  - Daily visual QC via plots for 1–10 day windows.
- QC flags:
  - Unique numeric flags indicate specific tests failed; multiple failures sum to a final QC flag value.
  - QC results stored in separate QC flag CSV files with _QCFLAG suffix, mirroring data structure.
- Tests cover: zero data, too few samples, low battery power, sensor faults, diagnostics, out-of-range values, secondary variable dependencies, spikes, and error codes.
- Traceability: final QC flag values map back to specific tests and variables, enabling reconstruction of processing decisions.

## Sub-hourly data (SH)
- Coverage: 30-minute resolution for multiple hydrometeorological and soil variables across sites; some variables measured at varying depths or not at all sites.
- Key variables include:
  - Radiation components (incoming/outgoing shortwave and longwave, net radiation)
  - Precipitation
  - Air temperature, relative humidity
  - Atmospheric pressure
  - Wind speed and direction (including X, Y, Z components at some sites)
  - Snow depth and related metrics
  - Soil temperature and volumetric water content (VWC) at several depths
  - Heat fluxes (G1, G2)
- Data completeness varies by site and variable; some sensors are not installed at all sites, and certain measurements (e.g., snow depth at some sites) are limited.
- Data sources and processing notes:
  - Measurements from various on-site instruments are aggregated to 30-minute values or used as instantaneous end-of-period values as specified.
  - 30-minute counts and sensor readings are telemetered hourly to CEH and QC’d before inclusion.

## Hourly volumetric water content (VWC)
- Derived VWC data (COSMOS_VWC) at hourly resolution for all sites.
- Derived using cosmic-ray neutron sensing (CRNS) with corrections for:
  - Background cosmic-ray intensity (linked to Jungfraujoch NMDB reference)
  - Atmospheric pressure and absolute humidity (Q)
  - Site altitude
- VWC computation methods used at COSMOS-UK:
  - Site-specific N0 calibration with field calibration
  - Other methods (universal hydrogen molar fraction and neutron transport modeling) exist but are not the primary COSMOS-UK approach.
- 2018 adjustments:
  - An extra correction factor F_i to account for geomagnetic fluctuations and CRNS reference differences; site-specific gamma (ɣ) values introduced to reprocess VWC and remove spurious trends.
- Data handled as: 30-minute neutron counts telemetered, summed to hourly, corrected, then hourly VWC computed; D86 depth values derived from hourly VWC.

## Daily data
- Daily resolution derived metrics:
  - COSMOS_VWC: daily average VWC
  - D86_75m: daily depth-related metric
  - PE: Penman-Monteith-based potential evapotranspiration
  - SWE: Snow Water Equivalent (midday value, 12:00)
  - SNOW: snow day indicator (1 if snow detected, 0 otherwise)
  - ALBEDO: daily albedo, calculated from SWOUT/SWIN between 10:00–14:00
- Snow detection and SWE estimation:
  - Snow days identified via albedo thresholds (average albedo > 50% indicates snow; falls below 35% ends snow day)
  - SWE estimated by comparing daily count rates with a snow-free benchmark using a method described in Wallbank et al. (2020)
- PE calculation:
  - Derived from sub-hourly data using Penman-Monteith (RN, G, TA, RH, WS, PA)
  - Daily PE is the sum of non-negative sub-hourly PE values
- Time stamping:
  - Daily data timestamps refer to the start of the day (00:00) and cover the preceding 24-hour period, unlike the sub-daily datasets.

## Completeness and limitations
- Completeness metrics are provided per site and by data category (Met, Soil, and VWC); VWC completeness reflects the derived CRNS-based data quality.
- Variability in site instrumentation and sensor availability affects overall completeness; some variables are not available at all sites or are missing for certain periods.
- CRNS-derived VWC is sensitive to snow cover and vegetation; caveats are noted regarding snow-days and SWE estimation during snow events.
- Some data gaps and changes over time are addressed via reprocessing and calibration updates (see Changes to data).

## Instrumentation and site deployment
- COSMOS-UK uses a suite of instruments, including:
  - Cosmic-Ray Neutron Sensor (CRNS) for VWC
  - Pluvio rain gauge
  - TDT soil moisture sensors for VWC and soil temperature
  - Soil heat flux plates (Hukseflux)
  - Soil temperature sensors (STP01)
  - Four-component radiometer for net radiation
  - Automatic weather station (air temperature, humidity, etc.)
  - Barometric pressure sensors
  - Wind sensors (3D and integrated 2D sonic anemometers)
  - Snow depth sensor (SR50A)
  - SnowFox SWE sensor
  - Campbell Scientific data logger (CR3000)
- Instrumentation varies by site; Section 7.2 documents site-specific installation details and which instruments are missing at particular sites.

## Changes to data and versioning
- Ongoing reprocessing when improvements are made; notable changes include:
  - Jul 2020: VWC calibration values updated; CRNS counts infilled from secondary tube; NMDB data infilled; 30-minute precipitation updated (from real-time to non-real-time); PE updated (method revision and aggregation changes)
  - Dec 2019: SWE added; daily albedo added
- These updates reflect efforts to improve calibration, data completeness, and consistency across the time series.

## Access, provenance, and governance
- Documentation and data are provided as supporting documentation for COSMOS-UK and are available via the COSMOS-UK website and the NERC Environmental Information Data Centre (EIDC).
- Clear data provenance, calibration methodology, QC processes, and instrument details support data governance, reproducibility, and informed reuse by data stewards and data users.
- Author contributions and project management details are documented to support accountability and data stewardship responsibilities.

## Key references
- Primary methodological and calibration sources for CRNS-based VWC, PE computation, SWE estimation, and related COSMOS-UK processing and QC workflow (e.g., Evans et al. 2016; Baatz et al. 2014; Franz et al. 2012, 2013; Köhli et al. 2015; Wallbank et al. 2020).