# Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Provides daily and sub-daily hydrometeorological and soil data from the COSMOS-UK network during 2013–2016.
- Data are stored in the Environmental Information Data Centre (EIDC) and split into four files.
- Based on 42 COSMOS-UK sites with 30-minute temporal resolution for hydrometeorological and soil variables (Oct 2013–Dec 2016).
- Data are logged on site, telemetered hourly to CEH Wallingford, and quality controlled.
- Includes derived products: daily potential evapotranspiration and volumetric water content from COSMOS measurements.

## Data files and contents
- Four files:
  - Hydrometeorological and soil (COSMOS-UK_Hydrometeorological&Soil.csv)
  - Potential evapotranspiration (COSMOS-UK_PotentialEvapotranspiration.csv)
  - Soil volumetric water content (Daily) (COSMOS-UK_VolumetricWaterContent_Daily.csv)
  - Soil volumetric water content (Hourly) (COSMOS-UK_VolumetricWaterContent_Hourly.csv)

- Hydrometeorological and soil data (30-minute resolution)
  - Variables include: incoming/outgoing longwave and shortwave radiation, net radiation, precipitation, atmospheric pressure, air temperature, wind speed and direction, humidity (absolute and relative), snow depth, soil temperature at multiple depths, volumetric water content (VWC) from TDT sensors, soil heat flux, and wind components (X, Y, Z).
  - Time stamps: yyyy-mm-dd hh:mm GMT.
  - Measured at up to 42 sites; snow depth and wind components availability vary by site.

- Potential evapotranspiration (daily resolution)
  - Derived from 30-minute hydrometeorological and soil data.
  - Variable: Potential Evapotranspiration (mm per time period); calculated after daily data collection.

- Volumetric water content (Daily)
  - Derived from hydrometeorological data and COSMOS cosmic-ray sensing data.
  - Variables: volumetric water content (percent) and D86 at 75 m distance from COSMOS sensor (depth-related value in cm).
  - Daily resolution (also notes on depth-specific derivations).

- Volumetric water content (Hourly)
  - Derived similarly to daily VWC but at hourly resolution.
  - Variables: corrected COSMOS neutron counts (counts) and volumetric water content (percent), plus D86 at 75 m depth.
  - Hourly resolution (with daily data also available).

## Site metadata and coverage
- 42 COSMOS-UK sites listed with:
  - Site name and ID, start date, calibration status, geographic coordinates (Easting, Northing), and altitude.
  - Map figure reference for site locations.
- Some sites are not calibrated (e.g., Cwm Garw); others are calibrated (Y).
- The document provides comprehensive site-level metadata to support data linking and spatial analysis.

## Data quality, processing, and derivation
- Data are subject to quality control tests; specifics are in the COSMOS-UK User Guide.
- Instrumentation and variable measurements are described in the user guide; data are telemetered hourly to the CEH data system.
- Derived products:
  - Potential evapotranspiration computed using Penman-Monteith method (FAO 56).
  - Volumetric water content derived from COSMOS cosmic-ray neutron data and corrections (Evans et al., 2016) for daily data; D86 values derived per Köhli et al. (2015) for depth considerations.
- New correction factors and methodology are detailed in the COSMOS-UK User Guide and associated references.

## Data access and usage
- Data are available in the Environmental Information Data Centre (EIDC) for sites installed before end of 2016.
- For network-wide data processing, processing details, and data availability across the full COSMOS-UK network, refer to the COSMOS-UK User Guide (and related documentation).
- Quality control procedures and instrumentation details are documented for reuse in environmental monitoring analyses.

## References and methodology
- Evans, J. G. et al. (2016). Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK.
- Köhli, M. et al. (2015). Footprint characteristics revised for field-scale soil moisture monitoring with cosmic-ray neutrons.
- FAO (1998). Crop evapotranspiration: Guidelines for computing crop water requirements (FAO-56).