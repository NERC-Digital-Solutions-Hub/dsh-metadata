# Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]

## Overview
- A COSMOS-UK dataset (2013–2016) stored in the Environmental Information Data Centre (EIDC) from 42 network sites.
- Data are organized into four CSV files and come with processing, quality control, and usage notes in the COSMOS-UK User Guide.
- Wytham Woods data end on 01-Oct-2016 due to decommissioning; other network data coverage is for Oct 2013–Dec 2016.
- Intended for researchers and policy teams needing high-resolution hydrometeorological and soil data, with derived products for evapotranspiration and soil moisture.

## Data files and formats
- Hydrometeorological and soil data (30-minute resolution)
  - Filename: COSMOS-UK_Hydrometeorological&Soil_2013-2016.csv
  - Variables include longwave/shortwave radiation, net radiation, precipitation (mm), atmospheric pressure (hPa), air temperature, wind speed/direction, humidity, snow depth, soil temperatures, volumetric water content (VWC) at multiple sensors, and wind components.
- Potential evapotranspiration (daily resolution)
  - Filename: COSMOS-UK_PotentialEvapotranspiration_2013-2016.csv
  - Derived using 30-minute inputs via Penman–Monteith (FAO 56); units in mm/day.
- Volumetric Water Content (Daily)
  - Filename: COSMOS-UK_VolumetricWaterContent_Daily_2013-2016.csv
  - Derived from hydrometeorological data and cosmic-ray sensor data; VWC in %; includes D86 depth data (75 m from sensor) in cm.
- Volumetric Water Content (Hourly)
  - Filename: COSMOS-UK_VolumetricWaterContent_Hourly_2013-2016.csv
  - Corrected cosmic-ray neutron counts and VWC (%) with hourly resolution; includes D86 depth data (75 m).

## Coverage and data resolution
- Spatial: 42 COSMOS-UK sites across the UK (site metadata available in the site list section).
- Temporal: Oct 2013–Dec 2016 for hydrometeorological and soil data; hourly (VWC) and daily (ET and VWC) derived products cover same period.
- Hydrometeorological and soil data resolution: 30-minute measurements.
- Derived products:
  - Potential evapotranspiration: daily totals derived from 30-minute inputs.
  - VWC (daily and hourly): derived from hydrometeorological data, cosmic-ray sensor counts, and background neutron data.

## Variables and measurement/derivation details
- Hydrometeorological & soil file (30-minute)
  - Variables include: incoming/outgoing longwave and shortwave radiation, net radiation, precipitation, atmospheric pressure, air temperature, wind speed and direction, humidity, snow depth, wind components (X/Y/Z), soil temperatures at multiple depths, and volumetric water content at sensors.
  - Some site-specific exceptions:
    - Snow depth measured at a subset of sites.
    - X, Y, Z wind components not measured at several sites (e.g., Alice Holt, Chimney Meadows, etc.).
  - Measurement approach: instruments on-site with data loggers; data telemetered hourly to CEH Wallingford.
  - Quality control: standard QC tests applied (details in COSMOS-UK User Guide).
- Potential Evapotranspiration (daily)
  - Derived from 30-minute hydrometeorological and soil data using Penman–Monteith (FAO 56).
- Volumetric Water Content (Daily)
  - Derived from hydrometeorological data and cosmic-ray sensor data plus background neutron data from Jungfrau (Switzerland).
  - VWC reported as daily averages; D86 (75 m depth) provided as daily depth-derived value.
  - Method references: Evans et al. 2016; correction factors as per Köhli et al. 2015.
- Volumetric Water Content (Hourly)
  - Derived hourly similar to daily VWC; includes corrected cosmic-ray neutron counts and hourly VWC values; D86 depth data provided.

## Site network (COSMOS-UK)
- 42 sites with metadata (site ID, start date, calibrated status, geographic coordinates, altitude).
- Example: sites include Chimney Meadows, Easter Bush, Gisburn Forest, Plynlimon, Rothamsted, Wytham Woods, etc.
- Start dates range around 2013–2016; most sites flagged as calibrated (Y).

## Data provenance, access, and governance
- Data are managed and stored at the Environmental Information Data Centre (EIDC) for sites installed before end of 2016.
- Data processing pipelines and instrumentation details are documented in the COSMOS-UK User Guide.
- Para-quality control tests are applied; details available in the User Guide.
- Use guidance and methodological notes referenced: Evans et al. 2016; Köhli et al. 2015; FAO 56.

## References
- Evans et al. 2016. Soil water content in southern England derived from a cosmic-ray soil moisture observing system – COSMOS-UK.
- Köhli et al. 2015. Footprint characteristics revised for field-scale soil moisture monitoring with cosmic-ray neutrons.
- FAO 1998. Crop evapotranspiration: Guidelines for computing crop water requirements (FAO-56).