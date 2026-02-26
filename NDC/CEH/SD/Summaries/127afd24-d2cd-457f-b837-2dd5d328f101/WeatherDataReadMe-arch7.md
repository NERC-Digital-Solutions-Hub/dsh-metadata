# WeatherData.csv

## Overview
- Data describing temperate conditions and rainfall during measurement campaigns on Welsh Mountain ewes equipped with Daily Diary sensors (Wildbyte Technologies Ltd., UK).
- Rainfall and air temperature recorded at half-hourly intervals at the Semi-Improved site; for the Unimproved site, data sourced from a nearby COSMOS facility.
- Campaigns are described in UrineEventsReadMe.csv.

## Data collection and sources
- Daily Diary sensors used to collect environmental data.
- Semi-Improved site: local measurements.
- Unimproved site: rainfall and temperature from COSMOS-UK facility (53°23′N, 4°0ʹW).

## Data fields / headers
- Site: Semi-Improved or Unimproved pasture.
- Season: Spring or autumn per site.
- DateTime: Date and time of measurement (dd/mm/yyyy hh:mm:ss).
- Rainfall: Rainfall in millimeters (mm).
- Temp: Air temperature in degrees Celsius (°C).

## Spatial and temporal considerations
- Data are temporally high-resolution (every 30 minutes).
- Spatial granularity is tied to site designation (Semi-Improved vs Unimproved); exact coordinates not provided in the file.
- Data from two sources (on-site measurements vs COSMOS facility) may require harmonization.

## Data quality and standards
- Potential challenges include combining data from multiple sources with different resolutions or reference locations.
- Suitable for GIS mapping and time-series analysis once data are cleaned and aligned across sites and sources.

## Reuse and citation
- If data are reused, ensure full citation.
- Key reference for COSMOS data: Evans et al., 2016 (COSMOS-UK).

## References
- Evans, J.G., Ward, H.C., Blake, J.R., et al. 2016. Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK. Hydrological Processes 30, 4987-4999.