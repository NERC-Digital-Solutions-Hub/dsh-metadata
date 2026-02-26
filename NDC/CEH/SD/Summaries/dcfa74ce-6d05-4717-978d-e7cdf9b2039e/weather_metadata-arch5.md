# 2018 weather station data from Durleigh Reservoir metadata file

- Dataset describes weather measurements from the Delta T WS-GP1 weather station at Durleigh Reservoir.
- Location details: latitude 51.1195, longitude -3.0389; mounted on the side of a building, 4 m above reservoir surface.
- Timeframe: data collected from 05/04/2018 to 05/10/2018; date and time formatted as dd/mm/yyyy HH:MM.
- Authors and citation: Slavin and Wain (2018); Please cite as Slavin, E.I., Wain, D.J. 2018. Weather data from Durleigh Reservoir, 2018. Weather measurements deployed by Emily Slavin and Danielle Wain.
- Purpose: determine on-site weather conditions to support measurements of in-reservoir processes.

- Parameters and sensors (with specs):
  - Air temperature (°C) — sensor: RHT3nl-CA; Range: 20–70°C; Accuracy: ±0.3°C; Sampling: 10-minute averages.
  - Humidity (%) — sensor: RHT3nl-CA; Range: -5% to 95% RH at 23°C; Accuracy: ±2%; Sampling: 10-minute averages.
  - Radiation (W/m^2) — sensor: D-PYRPA-CA; Range: 0 to 1.1 kW/m^2; Accuracy: ±5%; Sampling: 10-minute averages.
  - Rainfall (mm) — sensor: RG2+WS-CA; Range: 160 mm funnel diameter; Accuracy: 0.2 mm per tip; Sampling: 10-minute intervals.
  - Wind Direction (degrees) — sensor: D-034B-CA; Range: 0–360°; Accuracy: ±4°; Sampling: 10-minute averages.
  - Wind Speed (m/s) — sensor: D-034B-CA; Range: 0.4–75 m/s; Accuracy: ±0.1 m/s; Sampling: 10-minute averages.

- Metadata scope and intent:
  - Captures deployment context, sensor types, units, measurement intervals, and accuracy to enable reproducibility and data discovery.
  - Supports integration into data catalogues and potential sharing while detailing measurement standards.

- Governance and stewardship considerations:
  - Clear authorship and citation enable traceability and accountability.
  - Explicit temporal and spatial coverage aids discoverability and interoperability.
  - Standardized 10-minute aggregation facilitates harmonization with other datasets.
  - Documentation of sensor models and performance supports quality assurance and potential calibration checks.

- Practical actions for Data Stewards:
  - Verify metadata completeness (sensor IDs, units, ranges, accuracies, sampling intervals).
  - Ensure consistent date-time format and clarify time zones if needed.
  - Attach or link this metadata to the full dataset in the data portal and catalogue.
  - Record any data quality notes, calibration records, or known data gaps for transparency.