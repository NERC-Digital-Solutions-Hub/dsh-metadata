# Automatic Weather Station recordings from Moor House and Helbeck, Cumbria, 1974 - 1987

## Overview
- A historic dataset of Automatic Weather Station (AWS) recordings from Helbeck AWS (near Brough) and Moor House AWS in Cumbria, UK.
- Collected by Ken Taylor; stored in a database described by Cuthbertson (1993).
- Related ECN (Environmental Change Network) monitoring continues at Moor House (1991–2015; Rennie et al., 2017).

## Location and spatial references
- Helbeck AWS located in a wood near Brough, Cumbria.
- Moor House AWS located at grid reference 375100 533400.
- Helbeck grid reference: 378900 516000.
- Spatial orientation suitable for GIS mapping and historical climate visualization.

## Recording locations and temporal coverage
- Data grouped by DATID with site and time characteristics:
  - 40: Helbeck, hourly readings; 01-Jan-78 to 18-Oct-83.
  - 6: Helbeck, May 1974–Jun 1978; hourly readings.
  - 7: Helbeck, May 1974–Jun 1978; daily readings.
  - 5: Moor House, July 1974–Aug 1979; daily readings.
  - 41: Moor House, hourly readings; 01-Jan-79 to 08-Feb-87.
  - 4: Moor House, July 1974–Aug 1979; hourly readings.
- Temporal coverage spans 1974–1987 with varying frequencies (hourly and daily) per site and period.
- The dataset structure indicates multiple sub-datasets with differing start/end dates and sampling intervals.

## Variables and data schema
- Key fields:
  - DATID: Data set identification record number.
  - NO_REC: Number of recordings used to establish the value.
  - REC_TIME: Recording date (DD-MM-YYYY).
  - REC_HOUR: Hour of recording (0–23).
  - SOL_RAD: Solar radiation (Watts per square metre).
  - AIR_TEMP: Air temperature (degrees Celsius).
  - DEP_TEMP: Temperature depression (dry-wet bulb difference; a humidity proxy).
  - WIND_VEL: Wind velocity (km; interpreted as km/hr or km/day depending on dataset).
  - WIND_DIR: Wind direction.
  - RAINFALL: Rainfall (mm).
- Units vary by variable; some fields have two possible unit interpretations depending on the record.

## Data quality and caveats
- Missing values are present within the dataset.
- Reasons for missing data are unknown due to the historic nature of the records.
- Quality assurance procedures for these historic data are not documented in the dataset description.

## Related data and sources
- Original collection and storage referenced to Cuthbertson (1993): A database for environmental research programmes.
- UK Environmental Change Network (ECN) continues monitoring Moor House (1991–2015); Rennie et al. (2017) provide ECN meteorology data (NERC EIDC DOI available).
- Economic and historical context suggests potential integration with GIS-based climate visualization and historical weather maps.

## GIS-use considerations and recommendations
- Suitable for map-based time-series visualization of weather variables (air temperature, solar radiation, wind, rainfall) across two sites.
- Use grid references to place points; consider linking records by DATID to reconstruct temporal sequences.
- Handle missing values with appropriate imputation or masking in spatial analyses.
- Be aware of differing sampling frequencies by DATID; standardize temporal granularity for comparative analyses (e.g., hourly vs daily).
- Validate coordinates and temporal ranges against ECN data if integrating with newer datasets (Moor House continuation 1991–2015).