# Data from automatic water monitoring buoy from Blelham Tarn 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

- Overview
  - Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
  - Measurements include air temperature, solar radiation, wind speed, and lake temperature profiles.
  - Timeframe: 2012–2015; data recorded in GMT.
  - Data are raw (not yet calibrated/quality controlled) but have undergone visual checks with obvious hardware errors removed.
  - Used in multiple current scientific studies, including PhD work.

- Sampling regime and collection methods
  - Instruments and measurements
    - Air temperature (°C)
    - Solar radiation flux (W/m²) via pyranometer
    - Wind speed (m/s)
    - Lake water temperatures at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12 m
  - Sampling frequency
    - Data collected every 4 minutes.
    - Hourly averages computed: average over the previous hour (data from the hour ending at the measurement time excluded).
  - Time reference
    - All data are in Greenwich Mean Time (GMT).
  - Data storage history
    - Until 19 July 2012: hourly averages calculated by a Campbell Scientific datalogger.
    - From 19 July 2012 onwards: hourly averages stored in an Oracle database.

- Data structure and format
  - Storage format: Comma-separated values (CSV).
  - Columns
    - Date_GMT: Date and time of measurement (GMT)
    - 0.5m: Water temperature at 0.5 m depth (°C)
    - 1m: Water temperature at 1 m depth (°C)
    - 2m: Water temperature at 2 m depth (°C)
    - 3m: Water temperature at 3 m depth (°C)
    - 4m: Water temperature at 4 m depth (°C)
    - 5m: Water temperature at 5 m depth (°C)
    - 6m: Water temperature at 6 m depth (°C)
    - 7m: Water temperature at 7 m depth (°C)
    - 8m: Water temperature at 8 m depth (°C)
    - 9m: Water temperature at 9 m depth (°C)
    - 10m: Water temperature at 10 m depth (°C)
    - 12m: Water temperature at 12 m depth (°C)
    - Air_Temperature: Air temperature (°C)
    - Pyranometer: Solar radiation flux (W/m²)
    - Wind Speed: Wind speed (m/s)

- Quality control, calibration, and data quality
  - Status: Raw data not yet calibrated or quality controlled.
  - Quality checks performed: Visual inspection; obvious hardware malfunctions removed.
  - Data gaps: Occur due to buoy maintenance or sensor/logger problems.

- Data provenance, versioning, and usage
  - Dataset is referenced in scientific work, including studies by PhD students.
  - Document notes the data’s current use and potential ongoing analyses; implies need for ongoing versioning and metadata updates as calibration and quality control are applied.
  - Implication for stewardship: maintain provenance records, update quality flags, and track any reprocessing (calibration, gap filling, or transformations).

- Data accessibility, sharing, and governance considerations
  - Data are provided in a portable CSV format with explicit variable definitions and units, aiding discoverability and reuse.
  - Governance notes for data stewards:
    - Maintain comprehensive metadata (instruments, depths, units, time zone, averaging method, data processing steps, known gaps, access conditions, and contact).
    - Document calibration status and planned quality control procedures.
    - Capture and communicate data lineage (source sensors, datalogger/DB shift, processing steps).
    - Establish a clear update pipeline to incorporate new measurements, reprocessed data, and any corrections.
    - Consider cataloging this dataset in a data portal with metadata fields aligned to user needs and governance standards.

- Practical stewardship recommendations
  - Create a formal metadata record including:
    - Dataset name, scope, location, and time coverage (2012–2015).
    - Measurement methods, instruments, depths, units, and data processing (4-minute sampling, hourly averages, GMT).
    - Data quality state (raw; calibration status pending; known gaps and maintenance events).
    - Access, licensing, and citation guidelines; contact person for data.
  - Implement data quality workflow:
    - Calibrate and quality-check raw data.
    - Document any corrections or transformations.
    - Flag and annotate gaps with cause and expected resolution.
  - Plan for data updates:
    - Versioning scheme for recalibrated data.
    - Procedures for ingesting new data, updating the CSV/数据库, and refreshing metadata.
  - Ensure interoperability:
    - Standardize column naming and units; maintain mapping for legacy vs. new storage systems (Campbell Scientific datalogger vs. Oracle DB).
  - Data discovery and reuse:
    - Provide documentation on data provenance, measurement uncertainties, and recommended use cases (e.g., climate or limnology studies).

- End notes
  - Data from this buoy are actively used in ongoing research; stewardship should prioritize robust metadata, transparent quality control, and reliable access mechanisms to support broad reuse.