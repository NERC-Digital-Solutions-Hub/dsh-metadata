# Collection/generation methods

- Purpose and scope
  - Deployment of RBRsolo3 pressure sensors (2020–2023) in upper regions of four UK estuaries: Conwy, Kent, Dyfi, Milford Haven.
  - Loggers were not operational continuously during the period observed.
  - Recorded variables: time/date, air pressure (dbar), sea pressure (dbar), and depth (m). Depth is the water depth beneath the sensor and referenced to a per-estuary vertical reference level (ODN); negative depth indicates water level above the reference level.

- Deployment details
  - Estuaries and reference frames
    - Conwy, Kent, Dyfi, Milford Haven
    - Each estuary has its own sensor vertical reference level (ODN) as listed in the data table.
  - Sensor locations provided as exact UK grid coordinates (Eastings/Northings) for each estuary.

- Data structure and file naming
  - Data format: CSV files.
  - File naming convention: Name_startdate_dataset.csv
    - Name: Estuary (Conwy/Dyfi/Kent/MilfordHaven)
    - startdate: YYYYMMDD
    - dataset: 1–N, ordered chronologically since the start date
  - Example: Conwy_20201002_data1.csv

- Data quality and limitations
  - Sensors were factory calibrated; no additional quality control reported.
  - Data gaps are possible due to non-continuous operation during the deployment period.
  - Different estuaries use distinct vertical reference levels, complicating cross-estuary comparisons.

- Key data interpretation notes
  - Negative sea pressure values indicate the sensor is out of the water.
  - Depth values are relative to the estuary-specific vertical reference, so absolute depth comparisons require alignment to a common reference.

- Governance and discoverability implications for data leaders
  - Precise geospatial context (Eastings/Northings) and estuary-specific vertical references should be captured in metadata.
  - Documentation of calibration status and data gaps is essential for data quality assessment.
  - Standardized metadata and naming conventions enhance discoverability and interoperability across estuaries and datasets.