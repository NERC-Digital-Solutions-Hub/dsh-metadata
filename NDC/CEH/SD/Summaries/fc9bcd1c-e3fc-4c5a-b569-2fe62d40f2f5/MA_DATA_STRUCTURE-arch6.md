# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk) and ECN programme are the originators of the dataset.
- Dataset Owners: UK Environmental Change Network (ECN) programme sponsored by a consortium of UK government departments and agencies.

## Purpose and Scope

- Data are hourly summaries derived from 5-second samplings by Automatic Weather Stations (AWS).
- Collected to support understanding of environmental change and cross-site comparability.

## Ownership and Usage Guidance

- Acknowledge the use of ECN data in publications to demonstrate data value.
- Send one reprint of any publication that cites the data.
- ECN has standard operating procedures to ensure data comparability across sites; refer to accompanying ma.pdf for data collection explanations.

## Data Collection Protocol

- Standard operating procedures (protocols) in place to ensure comparability across ECN sites.
- Additional explanatory document: ma.pdf describes data collection methods.

## Data Structure and Access

- Data download fields:
  - SITECODE: Unique code for each ECN site.
  - AWSNO: Individual AWS at a location (can be multiple concurrent at the same site).
  - SDATE: Sampling date.
  - SHOUR: Sampling hour.
  - FIELDNAME: Variable measured.
  - VALUE: Measured value.
- Supporting documentation: ECN_MA_qtext.csv contains quality notes attached by site managers; fields include SITECODE, AWSNO, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.

## Site and Instrumentation Details

- Site codes T01–T12 with corresponding site names and locations (e.g., Drayton, Glensaugh, Hillsborough, Moor House Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Porton Down, Y Wyddfa Snowdon, Cairngorms).
- Many sites have operated two AWS units concurrently; always note the AWSNO when using data to ensure proper interpretation and cross-checking.

## Variables and Measurement Information

- Fieldnames (examples) and meanings:
  - ALBGRD: Albedo (W m^-2) and Albedo Sky (W m^-2), ground and sky.
  - DRYTMP: Dry bulb temperature (°C) and within humidity sensor (°C).
  - NETRAD: Net Radiation (W m^-2).
  - RAIN: Rainfall (mm, total).
  - RH: Relative Humidity (%).
  - SOLAR: Solar Radiation (W m^-2).
  - STMP10 / STMP30: Soil temperature at 10 cm and 30 cm (°C).
  - SURWET: Surface wetness (minutes in the hour).
  - SWATER / SWATER_T / SWATER_T10 / SWATER_VWC: Soil moisture measures (gypsum block, theta probe at 20 cm and 10 cm; volumetric water content).
  - WDIR: Wind direction (degrees).
  - WETTMP: Wet bulb temperature (°C).
  - WSPEED: Wind speed (m s^-1).
- Note: Units are provided for each field as indicated in the documentation.

## Additional Information

- Further site details and information available at: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27
- The dataset description encourages users to consult the quality information and the ECN site notes to account for data quality issues and site-specific circumstances.