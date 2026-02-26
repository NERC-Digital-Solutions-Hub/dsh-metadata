# Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

## 1 Introduction
- Describes data stored in the Environmental Information Data Centre (EIDC) for the COSMOS-UK network (2013-2016).
- Data are split into four files:
  - Hydrometeorological and Soil
  - Potential Evapotranspiration
  - Volumetric Water Content (Daily)
  - Volumetric Water Content (Hourly)
- Coverage applies to sites installed before end 2016; refer to COSMOS-UK_UserGuide.rtf for full network processing and availability.

## 2 Hydrometeorological and soil data (30 minute resolution)
- 42 COSMOS-UK sites with 30-minute resolution from Oct 2013 to Dec 2016.
- Filename: COSMOS-UK_Hydrometeorological&Soil.csv
- Variables include:
  - Radiation (incoming/outgoing longwave and shortwave; net radiation)
  - Precipitation
  - Atmospheric pressure, air temperature
  - Wind speed and wind direction (and components at some sites)
  - Humidity (absolute and relative), snow depth
  - Soil temperature at multiple depths, volumetric water content (VWC) at sensors
  - Additional soil heat flux measurements
- Resolution: 30-minute
- Measurement and QC:
  - Data gathered by on-site instruments, telemetered hourly to CEH Wallingford
  - On-site QC tests applied (details in COSMOS-UK User Guide)
- Site variability:
  - Snow depth measured at a subset of sites
  - Wind components (X, Y, Z) not measured at several sites

## 3 Potential evapotranspiration data (daily resolution)
- Description: ET derived from 30-minute hydrometeorological and soil data (across 42 sites) at daily resolution.
- Filename: COSMOS-UK_PotentialEvapotranspiration.csv
- Variable: Potential Evapotranspiration (mm) — total over the day
- Derivation: computed after daily data collection using Penman-Monteith (FAO-56)
- Data flow: based on the hourly telemetered data; documentation references instrumentation and processing details

## 4 Volumetric water content data (daily resolution)
- Description: Daily volumetric water content derived from hydrometeorological data and Cosmic-ray sensing (daily)
- Filename: COSMOS-UK_VolumetricWaterContent_Daily.csv
- Variables:
  - Volumetric water content (%)
  - D86 depth data (75 m from COSMOS sensor) in cm
- Resolution: daily (D86 data calculated from daily values)
- Derivation: 
  - Daily moisture via Evans et al. 2016 method
  - D86 values via Köhli et al. 2015 method
  - Corrections and factors documented in the COSMOS-UK User Guide

## 5 Volumetric water content data (hourly resolution)
- Description: Hourly volumetric water content derived from the same inputs as the daily dataset
- Filename: COSMOS-UK_VolumetricWaterContent_Hourly.csv
- Variables:
  - Corrected COSMOS neutron counts
  - Volumetric water content (%)
  - D86 depth at 75 m (cm)
- Resolution: hourly (with daily data also available)
- Derivation: hourly scripts using hydrometeorological data, Cosmic-ray data, and neutron monitor counts (Jungfrau station data)

## 6 COSMOS-UK sites
- Metadata for 42 sites, including:
  - SITE_ID, START_DATE, CALIBRATED status
  - Coordinates (Easting, Northing) and Altitude
- Example sites include Alice Holt, Chimney Meadows, Easter Bush, Gisburn Forest, Plynlimon, Rothamsted, Wytham Woods, etc.
- Site data details available in the COSMOS-UK sites section and map (Figure 1)

## 7 References
- Evans et al. 2016. Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK.
- FAO 1998. Crop evapotranspiration: Guidelines for computing crop water requirements. FAO Irrigation and Drainage Paper 56.
- Köhli et al. 2015. Footprint characteristics for field-scale soil moisture monitoring with cosmic-ray neutrons.
- Additional methodological references: Evans et al. 2016; Evans et al. and related documentation in the COSMOS-UK User Guide.