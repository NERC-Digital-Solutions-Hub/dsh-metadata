# ECN Weather and Environmental Data from Automatic Weather Stations (Hourly summaries from 5-second samplings)

## Overview
- Data product from ECN Data Centre, Centre for Ecology and Hydrology.
- ECN dataset is run by a consortium of UK government departments and agencies; intended to understand environmental change.
- For GIS use: designed to support map-based visualisations of environmental variables across sites.

## Data provenance and owners
- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk).
- Dataset Owners: UK Environmental Change Network (ECN) programme and partner organisations (e.g., AFBI, BBSRC, Natural Resources Wales, DEFRA, Environment Agency, Natural England, NERC, etc.).
- Usage acknowledgement: Please acknowledge dataset use in publications and send one reprint of any publication citing ECN data.

## Data content and structure
- Temporal resolution: hourly summaries derived from 5-second samplings by Automatic Weather Stations (AWS).
- Data structure (download format):
  - SITECODE: unique ECN site code (e.g., T01, T02, …).
  - AWSNO: individual AWS at a site (sites often have two AWS; AWSs can be concurrent).
  - SDATE: sampling date.
  - SHOUR: sampling hour.
  - FIELDNAME: variable measured.
  - VALUE: measured value.
- Quality notes: quality information accompanies data; site managers may attach explanatory text in ECN_MA_qtext.csv to document data quality issues.

## Variable information for mapping
- ALBGRD: Albedo (surface/ground; Wm-2).
- ALBSKY: Albedo of sky (Wm-2).
- DRYTMP: Dry bulb temperature (°C).
- DRTYMP_RH: Dry bulb temp within RH sensor (°C).
- NETRAD: Net Radiation (Wm-2).
- RAIN: Rainfall (mm; total).
- RH: Relative humidity (%).
- SOLAR: Solar radiation (Wm-2).
- STMP10: Soil temperature at 10 cm (°C).
- STMP30: Soil temperature at 30 cm (°C).
- SURWET: Surface wetness (minutes per hour).
- SWATER: Soil moisture (gypsum block; a dimensionless unit in bars).
- SWATER_T: Theta probe soil moisture at 20 cm (%).
- SWATER_T10: Theta probe soil moisture at 10 cm (%).
- SWATER_VWC: Volumetric water content at 20 cm (m3/m3).
- WDIR: Wind direction (degrees).
- WETTMP: Wet-bulb temperature (°C).
- WSPEED: Wind speed (m/s).

Note: Field names have accompanying descriptive text and units; field descriptions indicate whether values are averages or totals.

## Site codes and locations
- Sites labeled T01–T12, with names and coordinates:
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - T12 Cairngorms
- Many sites have two AWS units operating concurrently; AWSNO must be noted when using data.
- Location coordinates are provided for each site in the explanatory information.

## Data quality, protocol, and supporting documentation
- Protocols: ECN standard operating procedures to ensure data comparability across sites; see accompanying ma.pdf for data collection details.
- Quality documentation: ECN_MA_qtext.csv contains site manager notes on data quality issues, with fields for SITECODE, AWSNO, FIELDNAME, dates, and descriptions.
- Data quality emphasis: use accompanying quality information; consider AWS replacements and AWSNO when constructing time-series.

## Access, usage, and attribution
- Data download fields are as described (SITECODE, AWSNO, SDATE, SHOUR, FIELDNAME, VALUE).
- Supporting documentation is available; additional site details and quality notes are accessible via ECN resources and the catalogue link provided.
- Attribution: acknowledge ECN data use and provide a copy of any publication citing the data.

## GIS considerations and best practices
- For map-based visualisations, join data by SITECODE and AWSNO, and align by SDATE and SHOUR to create hourly environmental maps.
- Use site coordinates from the Explanatory Information for accurate geospatial plotting.
- When multiple AWS per site exist, incorporate AWSNO to distinguish data sources; consult ECN_MA_qtext.csv for site-specific quality text and any known issues.
- Temporal resolution is hourly, but underlying data are based on 5-second AWS samples; track this in metadata for precise time-based analyses.
- Be mindful of potential data quality flags and site-specific notes when filtering data for GIS analyses.