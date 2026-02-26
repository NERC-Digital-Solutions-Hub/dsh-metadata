# Field level headings: 1m, GMT = °C at 1 metre. 3m, GMT = °C at 3metre. 5m, GMT = °C at 5 metre. 7m, GMT = °C at 7 metre. 9m, GMT = °C at 9 metre. 11m, GMT = °C at 11 metre. 13m, GMT = °C at 13 metre. 15m, GMT = °C at 15 metre. 17m, GMT = °C at 17 metre. 19m, GMT = °C at 19 metre

- Dataset purpose and scope
  - Time-series temperature data collected at multiple depths (1 m, 3 m, 5 m, 7 m, 9 m, 11 m, 13 m, 15 m, 17 m, 19 m) using 10 Labfacility platinum resistance thermometers (PRTs) in a single location.
  - Temperature readings are labeled as GMT times; measurement range for thermometers is -5 to +40 °C.

- Temporal and spatial coverage
  - Date range: 03/11/2006 00:00 to 15/12/2008 14:00 (UTC/GMT).
  - Location details: grid reference SH 77961 46465; latitude 53.001555; longitude -3.8200267; elevation 460 m.

- Instrumentation and data collection
  - Temperature sensors: 10 Labfacility PRTs, each encapsulated in a stainless steel sheath.
  - Data logger: Campbell Scientific CR10X.
  - Data characteristics: multi-depth temperature measurements corresponding to the listed depths (1–19 m).

- Data structure and metadata considerations
  - Observations likely arranged as time-stamped records with temperature values for each depth channel at each timestamp.
  - Depth labels are discretely defined (1 m, 3 m, 5 m, 7 m, 9 m, 11 m, 13 m, 15 m, 17 m, 19 m); ensure consistent labeling and units (degrees Celsius).
  - Temperature value units: °C; time stamps in GMT/UTC.

- Data quality, standards, and processing
  - Sensor range is -5 to +40 °C; confirm calibration status and any drift corrections.
  - Potential QA steps: verify time synchronization across channels, check for missing values, flag outliers, and document any data transformations (e.g., calibration adjustments, gap filling).
  - Standardization needs: harmonize field names (e.g., depth_m, temperature_C, timestamp_UTC) and ensure consistent depth ordering across records.

- Data provenance and documentation
  - Document instrument IDs, calibration records, deployment dates, maintenance events, and any data processing steps applied.
  - Maintain a data dictionary and method notes describing how depths map to measurement channels and how GMT times relate to local time if applicable.

- Data storage, access, and updating
  - Data should be uploaded to the appropriate data portals/catalogues with clear provenance, license/usage terms, and update frequency.
  - Establish an update workflow for new observations, including versioning and change logs.

- Governance considerations and recommended actions for Data Stewards
  - Clarify user needs and use cases to inform metadata completeness (e.g., seasonality, quality flags, and retrieval formats).
  - Standardize metadata schema across depths and time points to support interoperability with other datasets.
  - Implement robust QA/QC protocols and keep calibration/maintenance records accessible.
  - Ensure clear handling of data limitations (e.g., gaps, sensor range limits, potential time drift) in dataset documentation.
  - Plan for long-term accessibility and consistency given the age of the data (2006–2008) and potential format migrations.

- Key considerations for future reuse
  - Provide a dataset-level summary including purpose, location, instrumentation, data coverage, and known limitations.
  - Include a reproducible processing workflow or scripts if transformations were applied, plus a data dictionary with field definitions.