# WeatherData.csv

## Overview
- Dataset capturing temperate climate conditions and rainfall during measurement campaigns on Welsh Mountain ewes equipped with Daily Diary sensors (Wildbyte Technologies Ltd., UK).
- Rainfall and air temperature recorded at half-hourly intervals at the Semi-Improved site; unimproved site data sourced from a nearby COSMOS facility.
- Data are linked to campaigns described in UrineEventsReadMe.csv; authors and project identifiers listed.

## Data Content and Structure
- Data headers:
  - Site: Semi-Improved or Unimproved pasture
  - Season: Spring or Autumn at each site
  - DateTime: Date and time of measurement (dd/mm/yyyy hh:mm:ss)
  - Rainfall: Rainfall in millimetres (mm)
  - Temp: Air temperature in degrees Celsius (°C)
- Sites and seasons cover measurements across two pasture types (Semi-Improved, Unimproved) and two seasons (Spring, Autumn).
- Measurements come from:
  - Semi-Improved: on-site rainfall and temperature
  - Unimproved: values sourced from COSMOS facility (Evans et al., 2016)

## Data Provenance and References
- Project: NE/M015351/1
- Authors: Karina A Marsden; Lucy Lush; Jon A Holmberg; Harris; Mick J Whelan; Sophie Webb; Andrew J King; Rory P Wilson; Davey L Jones; Alice F Charteris; Laura M Cardenas; Dave R Chadwick
- Primary reference: COSMOS-UK data framework (Evans et al., 2016)
- Additional campaign details: UrineEventsReadMe.csv

## Data Quality, Metadata and Access
- Data usage requires full citation to the original source.
- Metadata should clarify data sources per site (on-site measurements for Semi-Improved; COSMOS-derived values for Unimproved) and time zone considerations for DateTime.
- Temporal resolution is consistent (half-hourly); potential need for harmonization across sites.

## Implications for Data Leaders
- Demonstrates multi-site data integration with differing data sources (on-site vs COSMOS-derived) and consistent variable definitions.
- Highlights importance of cross-referencing auxiliary documentation (UrineEventsReadMe.csv) for campaign context.
- Emphasizes citation discipline and tracking of data lineage (author list, project ID, and COSMOS reference).
- Suggests attention to metadata completeness (instrument details, measurement periods, units) to improve discoverability and reusability.

## Related Materials
- UrineEventsReadMe.csv (campaign details)
- Evans et al., 2016 (COSMOS-UK reference)