# RBRsolo3 pressure sensors deployed in four UK estuaries (Conwy, Kent, Dyfi, Milford Haven) 2020-2023

## Summary
- Four estuaries (Conwy, Kent, Dyfi, Milford Haven) in the UK were instrumented with RBRsolo3 pressure sensors from 2020 to 2023.
- Loggers were not operational continuously; data contain gaps due to intermittent deployment.
- Each estuary has site-specific coordinates and a vertical reference level (ODN) used to compute depth.
- Recorded data include time, air pressure, sea pressure, and depth beneath the sensor.
- Depth values are relative to the sensor and the estuary’s vertical reference; negative depth indicates water level above the reference level.
- Sea pressure values can be negative if the sensor is out of the water.
- Data are stored as CSV files with a consistent naming convention; no additional quality control beyond factory calibration.

## Deployment and locations
- Time period: 2020–2023 (not continuous operation throughout).
- Estuaries and sensor details:
  - Conwy: Eastings 278,636.800; Northings 371,878.877; vertical reference (ODN) = -0.686 m
  - Kent: Eastings 348,111.700; Northings 483,305.838; vertical reference (ODN) = 4.206 m
  - Dyfi: Eastings 267,157.541; Northings 297,651.400; vertical reference (ODN) = -0.295 m
  - Milford Haven: Eastings 198,933.337; Northings 205,215.959; vertical reference (ODN) = -0.476 m
- Sensor placement is provided as location coordinates and a site-specific vertical reference level.

## Recorded data and units
- Recorded parameters: time (date-time), air pressure (dbar), sea pressure (dbar), depth (m).
- Depth definition: depth beneath the sensor; depth values are relative to the sensor position and the estuary’s vertical reference level.
- Interpretation notes:
  - Negative depth means the water level is above the vertical reference level.
  - Negative sea pressure indicates the sensor is out of the water.

## Data quality and availability
- Sensors came factory calibrated; no post-deployment quality control reported.
- Data outages expected due to non-continuous operation during the deployment window.

## Data structure and naming
- File format: CSV.
- File naming convention: Name_startdate_dataset.csv
  - Name: Estuary name (Conwy, Dyfi, Kent, MilfordHaven)
  - startdate: YYYYMMDD
  - dataset: integer 1–N (chronological sequence since the start date)
- Example: Conwy_20201002_data1.csv

## How this data supports analysis
- Enables time-series analysis of pressure and depth variations in multiple estuaries.
- Useful for estimating water column dynamics, identifying periods of out-of-water status, and cross-estuary comparisons once gaps are accounted for.
- Metadata (coordinates and vertical references) supports spatial alignment and depth calculations relative to a common datum.