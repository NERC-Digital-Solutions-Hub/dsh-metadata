# Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]

## Overview
- Dataset from the COSMOS-UK network covering 2013–2016, stored in the Environmental Information Data Centre (EIDC).
- Data are organized into four files:
  - Hydrometeorological and soil
  - Potential evapotranspiration
  - Volumetric water content (VWC) daily
  - Volumetric water content (VWC) hourly
- Based on 42 sites installed by end of 2016; data are 30-minute resolution for hydrometeorological/soil variables and daily/hourly resolutions for derived products.
- Information here refers to sites installed before 2017; full network details and processing are in the COSMOS-UK User Guide.

## Data files and formats
- Hydrometeorological and soil: COSMOS-UK_Hydrometeorological&Soil.csv (30-minute data)
- Potential evapotranspiration: COSMOS-UK_PotentialEvapotranspiration.csv (daily, derived)
- Volumetric water content daily: COSMOS-UK_VolumetricWaterContent_Daily.csv (daily, derived)
- Volumetric water content hourly: COSMOS-UK_VolumetricWaterContent_Hourly.csv (hourly, derived)

## Hydrometeorological and soil data (30-minute resolution)
- Variables include:
  - Incoming/outgoing longwave and shortwave radiation; net radiation
  - Precipitation (mm, total)
  - Atmospheric pressure (hPa)
  - Air temperature (°C)
  - Wind speed (m/s) and wind direction (degrees)
  - Humidity metrics (relative humidity, absolute humidity)
  - Snow depth (mm)
  - Wind components (X, Y, Z) at certain sites
  - Soil-related metrics such as soil temperature and heat flux
  - Volumetric water content at various soil sensors (TDT1/TDT2, etc.)
- Temporal aggregation:
  - Time stamps: yyyy-mm-dd hh:mm GMT
  - 30-minute measurements aggregated as means over preceding time period for some variables; others recorded as end-of-period values
- Measurement and data flow:
  - Instruments on site feed data to loggers; data telemetered hourly to CEH Wallingford
- Quality control:
  - All data pass quality control tests (details in COSMOS-UK User Guide)
- Site specifics:
  - All variables measured at most sites; exceptions noted (e.g., snow depth at a subset of sites; X/Y/Z wind components not measured at several sites)

## Potential evapotranspiration (daily)
- Derivation:
  - Calculated from the 30-minute hydrometeorological and soil data
  - Uses Penman–Monteith method (FAO 56)
- File: COSMOS-UK_PotentialEvapotranspiration.csv
- Variable: Potential Evapotranspiration (mm, total over the daily period)
- Coverage: computed for all COSMOS-UK sites

## Volumetric water content (daily)
- Derivation:
  - Derived from hydrometeorological data and Cosmic-ray sensing (COSMOS) data plus background neutron counts (Jungfraujoch data)
  - Daily values are averages of corrected neutron counts with the VWC equation from Evans et al., 2016
  - D86 at 75 m depth derived via Köhli et al., 2015 method
- File: COSMOS-UK_VolumetricWaterContent_Daily.csv
- Variables:
  - Volumetric water content (%; daily average)
  - D86 at 75 m depth (cm; daily)
- Data flow:
  - Hourly hydro-meteorological data and cosmic-ray neutron counts are integrated; daily VWC values are produced accordingly

## Volumetric water content (hourly)
- Derivation:
  - Derived hourly from hydrometeorological data and COSMOS cosmic-ray sensing data plus background neutron counts
- File: COSMOS-UK_VolumetricWaterContent_Hourly.csv
- Variables:
  - Corrected COSMOS neutron counts (count; total over preceding hour)
  - Volumetric water content (%; hourly average)
  - D86 at 75 m depth (cm; hourly average)
- Data flow:
  - Scripts run hourly to produce VWC values from inputs similar to the daily dataset

## COSMOS-UK sites
- Contains 42 sites with site IDs, coordinates, start dates, calibration status, and elevations
- Examples of site entries (illustrative):
  - Alice Holt (ALIC1), start 06-MAR-15, calibrated, coordinates provided
  - Chimney Meadows (CHIMN), start 02-OCT-2013, calibrated
  - Easter Bush (EASTB), start 13-AUG-2014, calibrated
  - Plynlimon (PLYNL), start 05-NOV-2014, calibrated
  - Waddesdon (WADDN), start 04-NOV-2013, calibrated
- Notes:
  - Cwm Garw is not calibrated
  - Full list, coordinates (Easting/Northing), and altitudes are provided in the section
  - Site details and calibration status are part of the published COSMOS-UK site metadata

## Data access and governance
- Data are stored in the Environmental Information Data Centre (EIDC)
- For data processing details and data availability, refer to the COSMOS-UK User Guide

## References
- Evans et al., 2016. Soil water content in southern England derived from a cosmic-ray soil moisture observing system – COSMOS-UK
- FAO 56 (Crop evapotranspiration guidelines)
- Köhli et al., 2015 (structure for interpreting COSMOS-derived depths)
- COSMOS-UK User Guide (instrumentation, processing, and metadata)