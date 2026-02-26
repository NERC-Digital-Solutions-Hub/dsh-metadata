# Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]

## Overview
- Dataset from the COSMOS-UK network covering 2013–2016, stored in the Environmental Information Data Centre (EIDC).
- Comprises four files:
  - Hydrometeorological and soil (30-minute resolution)
  - Potential evapotranspiration (daily)
  - Volumetric water content (daily)
  - Volumetric water content (hourly)
- Data obtained from 42 COSMOS-UK sites installed by 2016; instruments log data on-site and telemeter to CEH Wallingford hourly.
- Quality control is applied; instrumentation and processing are described in the COSMOS-UK User Guide.

## Hydrometeorological and soil data (30-minute resolution)
- Filename: COSMOS-UK_Hydrometeorological&Soil.csv
- Period: October 2013 – December 2016
- Variables (examples): incoming/outgoing longwave and shortwave radiation, net radiation, precipitation (mm, total), atmospheric pressure (hPa), air temperature (°C, mean), wind speed (m/s), wind direction (degrees), absolute and relative humidity, snow depth, soil temperature, volumetric water content (VWC) at multiple sensors, soil heat flux, wind components (X, Y, Z).
- Resolution: 30 minutes (variables often reported as mean over the preceding time period or at end of period).
- Measurements: on-site instruments with data telemetered hourly; full instrument details in the COSMOS-UK User Guide.
- Notes: some site- or variable-specific exceptions (e.g., snow depth not at all sites; wind components missing at a subset of sites).

## Potential evapotranspiration data (daily)
- Filename: COSMOS-UK_PotentialEvapotranspiration.csv
- Period: October 2013 – December 2016
- Variable: Potential evapotranspiration (mm) – daily total
- Derivation: calculated from 30-minute hydrometeorological and soil data; uses Penman-Monteith method (FAO 56) after daily data collection.
- Derived for all sites using the same workflow as the hydrometeorological data.

## Volumetric water content data (daily)
- Filename: COSMOS-UK_VolumetricWaterContent_Daily.csv
- Period: October 2013 – December 2016
- Variables: volumetric water content (VWC, %), daily averages; includes D86 depth measurements (75 m from COSMOS sensor) in cm.
- Resolution: daily (D86 values derived from daily COSMOS data).
- Derivation: from hydrometeorological data, COSMOS cosmic-ray neutron data, and background neutron counts (Jungfrau station, Switzerland); daily values use Evans et al. 2016 method; D86 derived per Köhli et al. 2015.

## Volumetric water content data (hourly)
- Filename: COSMOS-UK_VolumetricWaterContent_Hourly.csv
- Period: October 2013 – December 2016
- Variables: corrected COSMOS neutron counts (Total), VWC (%, hourly mean), D86 depth (75 m) in cm.
- Resolution: hourly (also available as daily via the daily VWC file)
- Derivation: hourly derivation from hydrometeorological data and COSMOS neutron data; uses Evans et al. 2016 and Köhli et al. 2015 methods; on-site instrumentation details in User Guide.

## COSMOS-UK sites (metadata)
- 42 sites with site IDs, coordinates (Eastings/Northings), altitude, start dates, and calibration status.
- Example sites include Alice Holt, Chimney Meadows, Easter Bush, Plynlimon, Rothamsted, Wytham Woods, Sheepdrove, etc.
- Metadata highlights:
  - SITE_ID, START_DATE, CALIBRATED (Y/N), EASTING, NORTHING, ALTITUDE
  - Most sites calibrated (Y); a few exceptions (e.g., Cwm Garw not calibrated)
- Site map reference provided in accompanying materials.

## Data quality, use, and references
- Data undergo quality control; specifics available in the COSMOS-UK User Guide.
- Suitable for GIS-based visualization of spatial and temporal patterns across sites, including:
  - 30-minute hydrometeorological fields
  - Daily PET and soil moisture variables
  - Hourly and daily VWC with depth information (D86)
- Key references:
  - Evans et al. 2016, COSMOS-UK: soil water content derived from cosmic-ray soil moisture monitoring
  - FAO 1998, Crop evapotranspiration: guidelines (FAO-56)
  - Köhli et al. 2015, footprint characteristics for field-scale soil moisture monitoring

## Usage notes for GIS specialists
- Formats: CSV files suitable for ingestion into GIS workflows; ensure time zone (GMT) alignment when mapping.
- Resolutions: 30-minute hydrometeorological data; daily PET and soil moisture; hourly VWC for high-temporal-detail mapping.
- Site metadata enables accurate georeferencing and site-based symbolization in maps (e.g., by calibration status, altitude, or location clusters).
- For complete instrumentation details and processing steps, refer to the COSMOS-UK User Guide and the referenced publications.