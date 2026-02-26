# Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Dataset covers the COSMOS-UK network from Oct 2013 to Dec 2016, consisting of data from 42 sites.
- Data are split into four CSV files:
  - Hydrometeorological and soil
  - Potential evapotranspiration
  - Volumetric water content (VWC) daily
  - Volumetric water content (VWC) hourly
- Data available in the Environmental Information Data Centre (EIDC); Wytham Woods ends on 01-Oct-2016 (site decommissioned).
- More details on data processing and availability across the network are in the COSMOS-UK User Guide.

## Data files and resolutions
- Hydrometeorological and soil (COSMOS-UK_Hydrometeorological&Soil_2013-2016.csv)
  - 42 sites, 30-minute resolution, Oct 2013–Dec 2016
  - Variables include: radiation (longwave/shortwave, incoming/outgoing; net), precipitation (mm), atmospheric pressure (hPa), air temperature (°C), wind speed and direction, humidity (absolute and relative), snow depth, wind components (X/Y/Z), soil heat flux, soil temperature at multiple depths, VWC at TDT sensors, etc.
  - Measured by on-site instruments and logged locally; telemetered to CEH Wallingford hourly.
  - Quality control applied (see User Guide).
- Potential Evapotranspiration (COSMOS-UK_PotentialEvapotranspiration_2013-2016.csv)
  - Daily resolution derived from 30-minute hydrometeorological and soil data
  - Values in mm per day; calculated at all sites
  - Derived via Penman-Monteith (FAO56) after daily data collection
- Volumetric Water Content Daily (COSMOS-UK_VolumetricWaterContent_Daily_2013-2016.csv)
  - Daily resolution derived from hydrometeorological data and cosmic-ray sensor data
  - Variables: Volumetric water content (%), D86 (depth-related parameter) at 75 m from sensor (cm)
  - Daily averages of corrected neutron counts used to compute VWC (Evans et al., 2016); D86 derived as per Köhli et al., 2015
- Volumetric Water Content Hourly (COSMOS-UK_VolumetricWaterContent_Hourly_2013-2016.csv)
  - Hourly resolution
  - Variables: Corrected cosmic-ray neutron counts (counts), Volumetric water content (%), D86 at 75 m (cm)

## COSMOS-UK sites
- 42 sites with metadata (site IDs, coordinates, start dates, calibration status, and elevations)
- Example: site IDs include ALIC1, BICKL, CHIMN, EASTB, EASTB etc., with Easting/Northing coordinates and altitude (m)
- Start dates range from 2013 to 2016; most sites calibrated as of their start date
- Map and site details provided in the dataset documentation

## Data collection, processing, and quality control
- On-site instruments log data; data telemetered to CEH Wallingford every hour
- Instrument-specific details and variable mappings provided in COSMOS-UK User Guide
- Quality control tests applied to all data (details in User Guide)
- VWC data derived from a combination of COSMOS-UK site data and background neutron counts from Jungfraujoch (Switzerland)
- VWC calculations follow Evans et al. (2016); D86 corrections follow Köhli et al. (2015); refer to user guide for correction factors

## Usage notes
- Wytham Woods data ends 01-Oct-2016 due to decommissioning
- Data are useful for linking hydrometeorological conditions, soil moisture (via cosmic-ray neutron method), and evapotranspiration at multiple temporal scales
- For cross-site and long-term analyses, consult the COSMOS-UK User Guide and references for methodological details and instrument specifics

## References
- Evans J. G. et al. (2016). Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK.
- FAO (1998). Crop evapotranspiration: Guidelines for computing crop water requirements. FAO Irrigation and Drainage Paper 56.
- Köhli M. et al. (2015). Footprint characteristics revised for field-scale soil moisture monitoring with cosmic-ray neutrons.
- COSMOS-UK User Guide (additional methodological and instrument details).