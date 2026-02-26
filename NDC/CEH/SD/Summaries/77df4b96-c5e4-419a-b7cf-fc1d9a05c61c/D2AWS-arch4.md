# Automatic Weather Station recordings from Moor House and Helbeck, Cumbria, 1974 - 1987

## Overview
- Historic dataset of Automatic Weather Station (AWS) records from Moor House and Helbeck, Cumbria, UK.
- Data collected by Ken Taylor.
- Stored in a database described in Cuthbertson (1993): A database for environmental research programmes.
- Related long-term monitoring at Moor House continued by UK Environmental Change Network (ECN) for 1991–2015.

## Site Locations
- Helbeck AWS: wood near Brough, Cumbria; grid reference 378900 516000.
- Moor House AWS: grid reference 375100 533400.
- ECN continuation at Moor House (1991–2015) referenced via ECN data centre.

## Recording locations and temporal resolutions
- Data recorded at multiple sites with varying temporal resolutions; identified by DATID.
- Examples:
  - DATID 40: Helbeck, hourly readings; 01-Jan-1978 to 18-Oct-1983.
  - DATID 6: Helbeck, May 1974–June 1978, hourly readings; 04-May-1974 to 13-Jun-1978.
  - DATID 7: Helbeck, May 1974–June 1978, daily readings; 04-May-1974 to 12-Jun-1978.
  - DATID 5: Moor House, July 1974–Aug 1979, daily readings; 27-Jul-1974 to 20-Aug-1979.
  - DATID 41: Moor House, hourly readings; 01-Jan-1979 to 08-Feb-1987.
  - DATID 4: Moor House, July 1974–Aug 1979, hourly readings; 27-Jul-1974 to 21-Aug-1979.
- Each record includes earliest and latest dates for the corresponding site/resolution.

## Variables and data content
- Data columns and descriptions:
  - DATID: Data set identification record number.
  - NO_REC: Number of recordings used to establish the value.
  - REC_TIME: Date of reading (DD-MM-YYYY).
  - REC_HOUR: Hour of reading (0–23).
  - SOL_RAD: Solar radiation (W/m^2).
  - AIR_TEMP: Air temperature (°C).
  - DEP_TEMP: Temperature depression (°C) – dry vs. wet bulb difference, humidity proxy.
  - WIND_VEL: Wind velocity (km/h) – reported as km/h (hourly or daily averages depending on dataset).
  - WIND_DIR: Wind direction.
  - RAINFALL: Rainfall (mm).
- Note: Missing values exist within the historic dataset; overall QA procedures are unknown.

## Data quality and limitations
- Historic nature means quality assurance procedures are not documented.
- Missing values present; reasons for missing data are not known.
- Metadata completeness and consistency across different DATIDs/temporal resolutions may vary.
- No explicit modern QA/validation described in the summary.

## Data governance and integration considerations for Data Leaders
- The dataset spans multiple sites and resolutions, requiring harmonization if used together (e.g., aligning time stamps, units, and missing-value handling).
- Provenance is documented (collector: Ken Taylor; storage reference: Cuthbertson 1993), with ECN continuation at Moor House providing a potential extension.
- Useful for historical climate analyses, dairy or ecosystem studies, or methodological work on integrating heterogeneous environmental time series.
- Metadata enhancements (clear QA status, data provenance trails, and complete documentation of each DATID) would improve discoverability and reusability.
- When planning broader data strategies, consider cross-referencing this dataset with ECN records (1991–2015) for continuity and broader context.