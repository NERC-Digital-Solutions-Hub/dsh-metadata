# WeatherData.csv

## Overview
- Data for the Uplands-N2O project (grant NE/M015351/1) documenting temperate climate measurements during Welsh Mountain ewe campaigns.
- Collected with Daily Diary sensors (Wildbyte Technologies Ltd., UK).
- Two pasture site types: Semi-improved and Unimproved.
- Rainfall and air temperature data accompany ewe study campaigns; detailed campaign notes available in UrineEventsReadMe.csv.

## Data content and structure
- Measurements: Rainfall (mm) and Temp (°C) recorded at half-hourly intervals.
- Sites:
  - Semi-Improved site: rainfall and temperature recorded locally (Skye Instruments Ltd., Llandrindod Wells, UK).
  - Unimproved site: data sourced from COSMOS facility nearby (COSMOS-UK reference).
- Data headers/columns:
  - Site: Semi-Improved or Unimproved
  - Season: Spring or Autumn
  - DateTime: dd/mm/yyyy hh:mm:ss
  - Rainfall: mm
  - Temp: °C

## Data collection and provenance
- Temperature and rainfall data tied to measurement campaigns using Daily Diary sensors.
- Unimproved-site data linked to COSMOS-UK cosmic-ray soil moisture observation framework (Evans et al., 2016).
- COSMOS reference: Evans, J.G. et al., 2016, Hydrological Processes 30, 4987-4999.

## Variables and data format
- Temporal resolution: half-hourly
- Temporal format: DateTime as dd/mm/yyyy hh:mm:ss
- Units: Rainfall in millimeters (mm); Temp in degrees Celsius (°C)
- Categorical fields: Site (Semi-Improved/Unimproved), Season (Spring/Autumn)

## Sites and campaign context
- Semi-Improved and Unimproved pasture conditions reflect differing management or grazing contexts.
- Campaign-specific details and methodology are linked to UrineEventsReadMe.csv for further data collection notes.

## Reuse and citation
- If data are reused, ensure full citation of data and, where applicable, of campaigns and sensor methods.
- Reference COSMOS-UK source for the unimproved-site data (Evans et al., 2016).

## Data quality and challenges
- Potential for integrating data from two different data sources (local instrumentation vs. COSMOS) due to site origin.
- Clear alignment required for cross-site temporal coverage and consistent DateTime formatting when combining datasets.