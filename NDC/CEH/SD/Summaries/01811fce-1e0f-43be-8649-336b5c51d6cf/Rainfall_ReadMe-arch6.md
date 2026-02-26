# ReadMe file for Rainfall.csv

## Overview
- Contains hourly rainfall data across studies investigating soil greenhouse gas emissions from sheep urine deposited on an unimproved montane grassland.

## Data collection and structure
- Instrument: HOBO® RG3 Data Logging rain gauge with a Pendant Event data logger (Tempcon Instrumentation Ltd., Sussex, UK).
- Logging rule: If an hour recorded 0 mm of rainfall, the event was not logged; records show only periods where rainfall was detected.
- Schema:
  - Date_time: Date and time of the recorded event, format dd/mm/yyyy hh:mm.
  - Hourly_rain: Total rainfall for the hour in millimetres (mm).

## Data quality and caveats
- Gaps in the data represent periods with no recorded rainfall, not explicit zero-rain hours; interpret missing rows as zero rainfall if aligning to a complete hourly timeline.
- Authors must be acknowledged if data are reused or reproduced.

## Provenance and usage considerations
- Data originate from field measurements in a montane grassland context related to sheep urine deposition studies.
- When combining with other datasets, ensure consistent time zones, date formats, and handling of missing (non-logged) hours.

## Data preparation tips for analysis
- Create a complete hourly time series by inserting zero-rain hours where gaps exist, if analysis requires full hourly coverage.
- Consider deriving additional features (e.g., cumulative rainfall, rainfall frequency) for correlation with soil greenhouse gas emissions.
- Verify and document authorship acknowledgment when using or citing the data.