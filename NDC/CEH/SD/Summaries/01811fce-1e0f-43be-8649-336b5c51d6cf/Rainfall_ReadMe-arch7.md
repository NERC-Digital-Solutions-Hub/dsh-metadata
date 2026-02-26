# ReadMe file for Rainfall.csv

- Purpose and scope: Rainfall data used in studies investigating soil greenhouse gas emissions from sheep urine deposited on an unimproved montane grassland.
- Data source and instrumentation: Rainfall recorded with a HOBO® RG3 Data Logging rain gauge equipped with a Pendant Event data logger (Tempcon Instrumentation Ltd., Sussex, UK).
- Logging behavior: If a given hour had 0 mm of rainfall, that hour was not logged; records include only periods where rainfall was detected.
- Data fields and formats:
  - Date_time: Date and time of the recorded event. Format: dd/mm/yyyy hh:mm.
  - Hourly_rain: Total rainfall recorded over the hour in millimetres (mm).
- Data readiness and GIS considerations:
  - Gaps: Because zero-rain hours are not logged, the time series contains gaps that may require imputation or careful handling for continuous analyses.
  - Temporal resolution: Hourly observations; ensure correct interpretation of the Date_time format and any time-zone assumptions.
  - Data integration: Useful for map-based or time-series visualizations when combined with other spatial or environmental datasets, with attention to data provenance and potential site-specific limitations.
- Data quality and constraints:
  - Data limited to the rainfall events detected by the specified instrument; may not represent non-detections.
  - Possible limitations related to study-specific context (soil greenhouse gas emissions research) and instrument placement.
- Usage and attribution:
  - Authors must be acknowledged if data are reused or reproduced.
  - Describes how rainfall data were collected and formatted to support GIS-based analyses and visualizations.