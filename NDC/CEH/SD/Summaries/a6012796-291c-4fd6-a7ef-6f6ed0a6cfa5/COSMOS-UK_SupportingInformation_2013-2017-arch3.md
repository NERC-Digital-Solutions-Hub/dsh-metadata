# COSMOS-UK. Daily and sub-daily hydrometeorological and soil data (2013-2017) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Dataset from 46 COSMOS-UK network sites covering October 2013 to December 2017.
- Includes sub-hourly (30-minute) hydrometeorological and soil data, QC flags, daily potential evapotranspiration (ET), hourly soil volumetric water content (VWC) from a cosmic-ray sensor, and daily VWC.
- Data are provided in multiple CSV files; missing values are encoded as -9999.
- Designed to support environmental monitoring, policy scrutiny, and decision-making, with emphasis on data quality, openness, and governance.

## Dataset contents and structure
- Sub-hourly hydrometeorological and soil data (COSMOS-UK_Hydrometeorological&Soil_2013-2017.csv): 30-minute resolution for 46 sites; includes variables such as precipitation, temperature, humidity, atmospheric pressure, wind, incoming/outgoing radiation, soil heat flux, soil temperature and VWC (via TDT sensors), and CRNS-derived VWC later processed.
- Sub-hourly QC flags (COSMOS-UK_Hydrometeorological&Soil_2013-2017_QC_Flags.csv): per-variable QC flags appended as suffix _QCFLAG; records accumulated flag values when data fail QC tests.
- Daily potential evapotranspiration (COSMOS-UK_PotentialEvapotranspiration_2013-2017.csv): daily ET (mm) computed via Penman-Monteith (FAO56) using RN, mean G (G1/G2), TA, Q, WS, PA; timestamp refers to the start of the day (00:00).
- Hourly volumetric water content (COSMOS-UK_VolumetricWaterContent_Hourly_2013-2017.csv): VWC from cosmic-ray neutron sensor, corrected for background cosmic rays, altitude, atmospheric pressure, and absolute humidity; site-specific N0 calibration used; 2018 update introduced an extra correction factor to remove spurious trends.
- Daily volumetric water content (COSMOS-UK_VolumetricWaterContent_Daily_2013-2017.csv): daily averages of hourly corrected counts to derive VWC; 00:00 start time referencing the preceding 24 hours.

## Methodology and quality control
- Data collected on-site by multiple instruments, logged locally, then telemetered hourly to CEH Wallingford.
- Two-stage QC:
  - Automatic QC tests applied to relevant variables; failing data are flagged and removed; each test has a unique flag value; flags can be summed to reflect multiple failures.
  - Daily visual inspection of plots for 1- and 10-day windows.
- QC flags dataset preserves the data structure with -QCFLAG suffix; provides traceability of which tests were failed.
- QC tests cover missing data, zero values, insufficient samples, low power, sensor faults, diagnostics, out-of-range values, and spikes.
- For VWC, corrections account for cosmic-ray flux, atmospheric pressure, humidity, and altitude; calibration uses site-specific N0 and field calibration; data reprocessed in 2018 to remove observed spurious trends.

## Completeness and limitations
- Completeness varies by site and data type; Table 7.1 (in the full doc) outlines site-level completeness for meteorological, soil, and VWC data.
- Snow depth is not universally recorded; measured only at a subset of sites (e.g., Cwm Garw, Easter Bush, Gisburn Forest, Glensaugh, Moor House, Plynlimon, Sourhope).
- Certain instruments are not installed at all sites (e.g., wind components Ux, Uy, Uz not available at all locations; Wytham Woods ended in 2016).
- Data are subject to standard limitations of field networks (metadata quality, site changes, instrument maintenance) but are supported by detailed instrumentation records and site metadata.

## Instrumentation and site details
- Instruments include:
  - Cosmic-Ray Neutron Sensor (CRNS) for VWC; counts corrected for background cosmic rays, altitude, pressure, and humidity.
  - Rain gauge (OTT Pluvio²) for precipitation.
  - Time-Domain Transmissometry (TDT) soil moisture sensors for absolute VWC and soil temperature.
  - Soil heat flux plates (Hukseflux HFP01SC).
  - Soil temperature sensors (STP01) at multiple depths.
  - Four-component radiometer (shortwave and longwave components) for net radiation.
  - Automatic weather station (Rotronic HC2A-S3) and barometric/temperature/humidity sensors (Vaisala/PTB110, HMP155).
  - 3D sonic and integrated 2D sonic anemometers for wind.
  - Snow depth (SR50A) and SnowFox snow-related measurements.
  - Campbell Scientific CR3000 data logger for on-site measurement logging.
- Site metadata include geographic coordinates, altitude, soil type, bulk density, organic matter content, and land cover; 46 sites are distributed across Great Britain with varying soil and vegetation types.

## Data access, authorship, and governance
- Data managed and curated by COSMOS-UK and CEH; primary contact for data is S. Stanley; data managers include H. M. Cooper, O. Hitt, M. Fry, O. Swain.
- Instrument calibration, field engineering, and network maintenance roles are described to support data provenance and governance.
- Data are hosted and accessible via the NERC Environmental Information Data Centre (EIDC); references and related literature are provided for methodological context (e.g., Penman-Monteith, CRNS theory, calibration approaches).
- The dataset exemplifies a monitored environmental health data stream with explicit QC, metadata, and governance processes suitable for informing policy analysis and future monitoring design.