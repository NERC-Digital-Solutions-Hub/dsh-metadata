# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview and purpose
- The ECN Data Centre provides hourly data summaries derived from 5-second samplings from Automatic Weather Stations (AWS) across ECN sites.
- The ECN programme is sponsored by a consortium of UK government departments and agencies to understand environmental change; funders support site monitoring or network coordination.
- Users are asked to acknowledge data use and to send one reprint of any publication citing ECN data.

## Protocol and data quality
- Standard operating procedures (protocols) exist to ensure comparability of data across sites; see accompanying ma.pdf for collection methods.
- Many ECN sites operate more than one AWS at the same location to enable cross-checking; AWS instances are identified by AWSNO.
- Always refer to the accompanying quality information when using data. Site managers may attach quality notes describing circumstances affecting data quality (ECN_MA_qtext.csv).

## Data structure and metadata
- Data Download fields:
  - SITECODE: Unique ECN site code
  - AWSNO: Individual AWS at a location (multiple AWS can run concurrently)
  - SDATE: Sampling date
  - SHOUR: Sampling hour
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting documentation: ECN_MA_qtext.csv contains site-specific quality notes (SITECODE, AWSNO, FIELDNAME, dates, continuing status, and descriptions).

## Site codes and locations
- Explanatory Information: Site codes T01–T12 correspond to ECN sites (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa - Snowdon, Cairngorms).
- Notes at several sites indicate that two AWS have operated at the same site, and users should record the AWSNO when using the data.

## Variables and units (FIELDNAME)
- Albedo (surface) and Albedo Sky (average) in W m^-2
- Dry bulb temperature (average) in °C (air temperature)
- Dry bulb temperature within the relative humidity sensor (average) in °C
- Net Radiation (average) in W m^-2
- Rainfall (total) in mm
- Relative Humidity (average) in percent
- Solar Radiation (average) in W m^-2
- Soil temperature at 10 cm (average) in °C
- Soil temperature at 30 cm (average) in °C
- Surface wetness (minutes in the hour that the surface is wet) in minutes
- Soil moisture - gypsum block (average) in bars
- Soil moisture - theta probe at 20 cm (average) in percent
- Soil moisture - theta probe at 10 cm (average) in percent
- SWATER_VWC (volumetric water content) at 20 cm (average) in m^3/m^3
- Wind direction (average) in degrees
- Wet bulb temperature (average) in °C
- Wind speed (average) in m s^-1

## Access and usage considerations
- Data are hourly summaries derived from high-frequency measurements; attention to AWSNO is important when multiple sensors exist at a site.
- Data users should consult the quality notes and the ECN site documentation for context and data quality considerations.
- Further information about ECN sites is available at the ECN catalogue link: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27