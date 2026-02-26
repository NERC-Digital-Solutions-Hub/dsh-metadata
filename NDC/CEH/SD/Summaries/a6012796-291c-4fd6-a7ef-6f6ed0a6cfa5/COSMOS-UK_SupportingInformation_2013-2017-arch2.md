# Supporting documentation for COSMOS-UK (2019). Daily and sub-daily hydrometeorological and soil data (2013-2017) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview

- Describes COSMOS-UK daily and sub-daily hydrometeorological and soil data from 46 sites, spanning 2013–2017 (end of 2017).
- Data are organized into five files: 
  - Sub-hourly hydrometeorological and soil data
  - Sub-hourly QC flags
  - Daily potential evapotranspiration
  - Hourly soil volumetric water content (VWC) from cosmic-ray sensor
  - Daily soil VWC from cosmic-ray sensor
- Data are collected with multiple instruments, quality-checked, and uploaded to CEH’s central data system.

## COSMOS-UK sites

- 46 sites across the COSMOS-UK network with varying site characteristics (altitude, soil type, land cover).
- Site metadata provided (e.g., start dates, geographic coordinates, soil type, bulk density, organic matter, land cover).
- Some site-specific notes: varying instrumentation availability; data completeness varies by site.

## Data files and content

- 3.1 COSMOS-UK_Hydrometeorological&Soil_2013-2017.csv
  - 30-minute resolution data for 46 sites (Oct 2013–Dec 2017). Missing values coded as -9999.
  - Variables include: incoming/outgoing shortwave and longwave radiation, net radiation, precipitation, atmospheric pressure, air temperature, wind speed/direction, specific humidity, relative humidity, snow depth (site-limited), wind components, soil heat flux (G1, G2), soil temperature and VWC from TDT sensors, and near-surface soil temperature and VWC from multiple depths.
  - Some measurements are instantaneous; others are 30-minute aggregates (sum/mean). Timestamp refers to end of the 30-minute period.
- 3.2 Sub-hourly QC flags
  - Parallel QC flags file mirroring the data file structure, with suffix _QCFLAG on each variable.
  - Flags indicate failures of automatic QC tests; multiple flags can be combined and recorded as a single value.
- 4 COSMOS-UK_PotentialEvapotranspiration_2013-2017.csv
  - Daily Penman-Monteith-based potential evapotranspiration (PET) for all sites (Oct 2013–Dec 2017).
  - Uses RN, mean G1/G2, TA, Q, WS, PA; DATE_TIME is the start of the day (00:00 GMT) and represents the full preceding 24-hour period.
- 5 COSMOS-UK_VolumetricWaterContent_Hourly_2013-2017.csv
  - Hourly VWC derived from Cosmic-Ray Neutron Sensor (CRNS) data (46 sites).
  - Also includes corrected neutron counts and a depth indicator (D86 at 75 m).
  - Corrections account for background cosmic ray intensity, atmospheric pressure, and absolute humidity; VWC derived via one of three methods (site-specific N0, universal calibration/hmf, or neutron transport modelling). COSMOS-UK uses site-specific N0 approach.
  - Post-2018 adjustments applied to remove spurious trends via a gamma-based correction factor.
- 6 COSMOS-UK_VolumetricWaterContent_Daily_2013-2017.csv
  - Daily VWC derived similarly from hourly corrected counts (as daily averages) for all sites.
  - DATE_TIME denotes the beginning of the day (00:00 GMT); daily step used for VWC value and D86 depth calculations.
- 7 Completeness
  - Contains completeness metrics for Met (precipitation, humidity, air temperature, pressure, radiation, wind) and Soil (soil heat flux, soil temperature, TDT-based VWC), plus VWC completeness.
  - Provides site-by-site completeness summaries over Oct 2013–Dec 2017.
- 8 Instrumentation
  - Section 8.1 outlines instrument types used (CRNS, rain gauge, soil moisture sensors, heat flux plates, soil temperature sensors, radiometer, automatic weather station, barometer, anemometers, snow depth sensors, etc.).
  - Section 8.2 details site-by-site installation variations (not all instruments present at every site).
  - CRNS measures fast neutrons to infer soil moisture; counts corrected for atmospheric conditions and using a reference site. VWC derived using calibration methods and corrections described in Evans et al. (2016) and related literature.
  - Examples of instruments: Hydroinnova CRS-2000/CRS-1000, OTT Pluvio² rain gauge, Acclima TDT sensors, Hukseflux HFP01SC heat flux plates, Hukseflux STP01 soil temperature sensors, Hukseflux radiometer, Rotronic/HUMICAP humidity and temperature sensors, Gill WindMaster 3D Sonic Anemometer, Campbell SR50A snow depth sensor, Campbell CR3000 data logger.
- 8.2 Site-level instrument variation table
  - Documents which sites have which instruments installed (many sites do not have every instrument).

## Methodology and data quality

- Data are collected by on-site loggers, then telemetered hourly to CEH Wallingford for QC.
- Quality control (QC) process has two stages:
  - Automatic QC tests: data failing tests are flagged and removed; each test has a unique flag value; multiple failures combine into a single QC flag value.
  - Daily visual inspection with plots covering 1- and 10-day time frames.
- QC flagging:
  - Flags indicate issues such as missing data, zero data where not expected, too few samples, low battery, sensor fault, diagnostic flags, out of range values, dependencies between variables, spikes, and error codes.
  - The QC flag file mirrors the data file structure with _QCFLAG suffixes; for example, a particular data value with a combined 72 flag indicates failures for low power (8) and out of range (64).
- VWC processing (CRNS):
  - Corrected neutron counts are obtained after adjusting for background cosmic ray intensity, altitude, atmospheric pressure, and absolute humidity.
  - Counts are converted to VWC using chosen calibration methods; site-specific N0 calibration used by COSMOS-UK.
  - 2018 adjustment factor applied to counts to remove spurious trends, with site-specific gamma values derived empirically.
  - Daily and hourly VWC derived from corrected counts; D86 depth values computed from VWC as per Köhli et al. (2015).

## Data accessibility and use for environmental monitoring

- Outputs provide standardized, time-stamped datasets suitable for long-term environmental health and policy performance monitoring.
- Data are stored and accessible via CEH data portals; QC flags enable traceability of data quality issues.
- The integration of multiple data streams (meteorology, soil moisture from TDT and CRNS, PET) supports analysis of soil-plant-atmosphere interactions and water balance at catchment scales.
- The documentation emphasizes data completeness and instrument metadata to aid reproducibility and cross-site comparisons.

## Key references and notes

- Core methodological references for CRNS-based VWC and calibration, and FAO-56 Penman-Monteith PET methodology.
- Notes on timestamp conventions: many sub-daily data refer to the end of the preceding period, while PET timestamps refer to the start of the day.
- Instrumentation details and site-specific deployment are provided to support interpretation and quality assessment of site data.