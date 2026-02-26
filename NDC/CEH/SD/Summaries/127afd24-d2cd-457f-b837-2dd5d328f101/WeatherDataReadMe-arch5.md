# WeatherData.csv

## Overview
- WeatherData.csv contains half-hourly measurements of rainfall and air temperature collected during measurement campaigns on Welsh Mountain ewes equipped with Daily Diary sensors (Wildbyte Technologies Ltd., UK).
- Data include campaigns at two pasture sites (Semi-Improved and Unimproved) with campaign details described in UrineEventsReadMe.csv.
- For the Unimproved site, temperature and rainfall data are sourced from a COSMOS facility (COSMOS-UK).

## Data content and structure
- Headers/variables:
  - Site: Semi-Improved or Unimproved pasture
  - Season: Spring or Autumn at each site
  - DateTime: Date and time in dd/mm/yyyy hh:mm:ss format
  - Rainfall: Rainfall in millimetres (mm)
  - Temp: Air temperature in degrees Celsius (°C)
- Sampling frequency:
  - Rainfall and Temperature recorded at half-hourly intervals at the Semi-Improved site
  - Unimproved site data sourced from COSMOS (balancing with the campaign context)

## Data provenance and sources
- Daily Diary sensors used for data collection (Wildbyte Technologies Ltd., UK)
- Semi-Improved site data collected at Skye Instruments Ltd., Llandrindod Wells, UK
- Unimproved site data sourced from a COSMOS facility (53°23′N, 4°0′W)
- Related campaign details and methodology are described in UrineEventsReadMe.csv

## References
- Evans, J.G. et al. 2016. Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK. Hydrological Processes 30, 4987-4999.

## Data quality, metadata and reuse considerations
- If data are reused, ensure proper citation of WeatherData.csv and associated campaigns (and the COSMOS source where applicable).
- Metadata and documentation should capture:
  - Site designation (Semi-Improved vs Unimproved)
  - Season designation (Spring vs Autumn)
  - DateTime formatting and time zone context
  - Units for Rainfall (mm) and Temp (°C)
- The dataset references UrineEventsReadMe.csv for details on campaign context, which should be consulted to interpret the data correctly.

## Governance and stewardship considerations for Data Stewards
- Ensure complete and consistent metadata across Site, Season, DateTime, Rainfall, and Temp, including unit definitions.
- Verify alignment between semi-improved and unimproved data sources (including the COSMOS-derived variables) and document any differences.
- Track data provenance and ensure proper citation requirements are met for reuse.
- Manage data updates and maintain linkage to related files (e.g., UrineEventsReadMe.csv).
- Prepare for data sharing/portal deposition by providing standardized headers, formats, and documentation.