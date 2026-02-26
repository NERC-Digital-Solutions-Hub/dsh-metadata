# Penllwyn Rain gauge read me document

## Overview
- A maintenance and data quality log for the Penllwyn rain gauge, detailing installation, timestamp issues, weather-related data problems, and subsequent data adjustments relevant for GIS data products.

## Timeline of events and data quality impacts
- 25/01/06: Rain gauge installed.
- 03/10/06: Timestamp drift observed (Pen RG last reading 1349 vs laptop 1441 GMT); ~52 minutes out. Reset performed.
- Feb/07: Data considered dodgy due to significant snow; wind-blown snow off the gauge likely caused under-recording.
- 30/04/07: Battery, seal, and desiccant on Tinytag replaced.
- 31/10/07: Wind blew tipping bucket at 11:20.
- 30/11/07: Wind blew tipping bucket at 10:36 (some water present in bucket).
- 22/12/07: ~8 hours of intermittently impossibly high tipping bucket readings (max readings); cold temperatures suspected as a contributing factor; bowl weirboxes also had a problem at this time.
- 03/11/07: Time stamp issue and overlap with previous download; adjusted to follow on from last record; adjustment noted in Excel file.

## Maintenance and data handling
- Equipment maintenance: battery, seal, and desiccant replacements; general sensor upkeep.
- Data handling: time stamps adjusted where necessary; adjustments documented in the accompanying Excel file.

## Data quality considerations for GIS
- Timestamp accuracy: occasional drift and overlaps requiring corrections.
- Weather-related data reliability: snowfall, wind, and extreme cold causing under-recording or spurious high readings.
- Sensor integrity: wind impacts on tipping bucket; potential issues with bowl weirboxes.
- Data gaps and anomalies: periods flagged as questionable or corrected post-download.

## Implications for GIS workflows
- Metadata must capture sensor status, maintenance events, timestamp corrections, and anomaly periods.
- QA steps should include checks for timestamp alignment with downloads, detection of buoyant or impossibly high values, and cross-validation during extreme weather.
- Clearly flag suspect data periods and document any corrections or exclusions to maintain data provenance.

## Recommendations for future use
- Maintain a detailed data quality log linked to GIS metadata (sensor health, maintenance events, timestamp corrections, anomaly notes).
- Flag and possibly exclude periods with known issues (e.g., severe weather impacts, timestamp overlaps) or archive them with clear provenance.
- Ensure time data is standardized (e.g., GMT) and that any corrections are traceable in the dataset (e.g., Excel/metadata records).
- Consider integrating maintenance notes (battery changes, desiccant replacements, component issues) into data provenance for improved future analyses.