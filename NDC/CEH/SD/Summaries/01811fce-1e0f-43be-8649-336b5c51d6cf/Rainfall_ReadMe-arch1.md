# ReadMe file for Rainfall.csv

- Purpose: Description of hourly rainfall data used in studies investigating soil greenhouse gas emissions from sheep urine deposited on unimproved montane grassland.
- Data source and instrument: Rainfall recorded with a HOBO RG3 Data Logging rain gauge with a Pendant Event data logger (Tempcon Instrumentation Ltd., Sussex, UK).
- Logging behavior: If an hour had 0 mm of rainfall, that hour was not logged; records show only the time periods during which rainfall was detected.
- Data fields:
  - Date_time: Date and time of the recorded event (format: dd/mm/yyyy hh:mm).
  - Hourly_rain: Total rainfall in millimeters for the hour.
- Data scope: The dataset spans multiple studies examining soil GHG emissions from sheep urine in unimproved montane grassland.
- Data completeness notes: Because hours with zero rainfall are omitted, the dataset contains gaps corresponding to dry periods. Users may need to infer or fill zeros if a continuous hourly series is required.
- Usage and attribution: Authors must be acknowledged if the data are reused or reproduced.
- Considerations for analysts:
  - Be aware of potential scale and completeness issues due to data being recorded only for detected rainfall events.
  - When merging with other datasets, account for missing hours and potential time-zone assumptions not specified in the ReadMe.
  - Rainfall is reported in millimeters per hour; ensure consistent units across analyses.