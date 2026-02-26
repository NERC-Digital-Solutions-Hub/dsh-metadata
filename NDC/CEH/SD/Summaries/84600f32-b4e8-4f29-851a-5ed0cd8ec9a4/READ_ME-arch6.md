# Collection/generation methods

- Overview
  - RBRsolo3 pressure sensors deployed 2020–2023 in the upper regions of four UK estuaries: Conwy, Kent, Dyfi, Milford Haven.
  - The loggers were not operational continuously throughout the period.

- Sensor locations and vertical references
  - Conwy: Eastings 278636.800; Northings 371878.877; Vertical reference level (m, ODN) = -0.686
  - Kent: Eastings 348111.700; Northings 483305.838; Vertical reference level (m, ODN) = 4.206
  - Dyfi: Eastings 267157.541; Northings 297651.400; Vertical reference level (m, ODN) = -0.295
  - Milford Haven: Eastings 198933.337; Northings 205215.959; Vertical reference level (m, ODN) = -0.476

- Measured variables and units
  - Time (date time)
  - Air pressure (dbar)
  - Sea pressure (dbar)
  - Depth (m) beneath the sensor; negative depth values indicate water level above the vertical reference level

- Quality control and data quality notes
  - Sensors were factory calibrated; no further quality control performed
  - Negative sea pressure values indicate the sensor is out of the water

- Data structure and organization
  - Data are provided in CSV file format
  - File naming convention: 'Name_startdate_dataset.csv' (e.g., Conwy_20201002_data1.csv)
    - Name = Estuary [Conwy / Dyfi / Kent / MilfordHaven]
    - startdate = YYYYMMDD
    - dataset = dataset number 1–N, ordered chronologically since the start date

- Data considerations for users
  - Different estuaries have different vertical reference levels; align depth and pressures accordingly
  - Expect non-continuous operation and potential gaps; account for this in analyses and reporting
  - Use factory-calibrated metadata with caution, as no additional QC beyond factory calibration is described