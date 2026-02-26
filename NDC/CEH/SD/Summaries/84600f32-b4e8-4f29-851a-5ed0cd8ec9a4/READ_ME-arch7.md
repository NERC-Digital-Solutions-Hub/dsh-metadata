# RBRsolo3 pressure sensors deployment in four UK estuaries (Conwy, Kent, Dyfi, Milford Haven) 2020-2023

## Overview
- Four estuaries monitored: Conwy, Kent, Dyfi, Milford Haven (upper regions).
- Timeframe: deployments between 2020 and 2023; sensors were not continuously operational.
- Data are provided as CSV files with per-estuary deployments and datasets ordered chronologically.

## Spatial and deployment details
- Sensor locations (per estuary) with coordinates and vertical reference (ODN):
  - Conwy: Eastings 278,636.800; Northings 371,878.877; vertical reference level -0.686 m (ODN)
  - Kent: Eastings 348,111.700; Northings 483,305.838; vertical reference level 4.206 m (ODN)
  - Dyfi: Eastings 267,157.541; Northings 297,651.400; vertical reference level -0.295 m (ODN)
  - Milford Haven: Eastings 198,933.337; Northings 205,215.959; vertical reference level -0.476 m (ODN)

## Recorded variables and units
- Time: date and time
- Air pressure: dbar
- Sea pressure: dbar
  - Negative sea pressure indicates the sensor is out of the water
- Depth: meters
  - Depth is the water depth beneath the sensor
  - Negative depth values indicate water level above the local vertical reference level (ODN)

## Data structure and file naming
- File format: CSV (.csv)
- File naming convention: Name_startdate_dataset.csv
  - Name: Estuary name [Conwy, Dyfi, Kent, MilfordHaven]
  - startdate: YYYYMMDD
  - dataset: dataset number (1-N) ordered chronologically since the start date
- Example: Conwy_20201002_data1.csv

## Quality control and data integrity
- Sensors were factory calibrated; no additional quality control performed on the data.

## GIS usage considerations
- Coordinate reference: local coordinates (Eastings/Northings) with estuary-specific vertical reference levels (ODN); ensure harmonization to a common projection and vertical datum when integrating across estuaries.
- Depth interpretation: use the estuary-specific vertical reference level to convert depth to a common baseline if required.
- Data gaps: deployments were not continuous; account for gaps when constructing time series.
- Data integration: combine datasets from multiple estuaries carefully due to differing vertical references; consolidate time stamps across files for cross-estuary analyses.

## Limitations and notes for analysts
- Lack of post-deployment quality control beyond factory calibration; validate critical analyses where possible.
- Negative depth and sea pressure indicators require careful handling during data cleaning and interpretation.