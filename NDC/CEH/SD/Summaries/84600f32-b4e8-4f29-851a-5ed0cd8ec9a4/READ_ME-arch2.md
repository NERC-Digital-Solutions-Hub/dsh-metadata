# RBRsolo3 pressure sensors deployment in four UK estuaries (Conwy, Kent, Dyfi, Milford Haven) 2020-2023

## Overview
- Description of collection/generation methods for environmental monitoring data using RBRsolo3 pressure sensors.
- Sensors deployed in upper regions of four UK estuaries between 2020 and 2023; operation was not continuous across the period.
- Locations and sensor reference levels provided (Table 1).

## Deployment details
- Estuaries: Conwy, Kent, Dyfi, Milford Haven.
- Deployment window: 2020–2023.
- Logger locations are specified per estuary (see coordinates and vertical reference levels).

## Measured variables and units
- Time: date and time stamps.
- Air pressure: in decibars (dbar).
- Sea pressure: in decibars (dbar).
- Depth: meters, defined as water depth beneath the sensor; depth is relative to the estuary’s vertical reference level (ODN). Negative depth values indicate water level above the reference level.

## Reference levels and depth interpretation
- Each estuary has a specific vertical reference level (in meters, ODN):
  - Conwy: -0.686 m
  - Kent: 4.206 m
  - Dyfi: -0.295 m
  - Milford Haven: -0.476 m
- Negative sea pressure values indicate the sensor is out of the water.

## Quality control
- Sensors were factory calibrated.
- No additional quality control has been performed on the data after collection.

## Data structure and file naming
- Data format: CSV (.csv) files.
- File naming convention: Name_startdate_dataset.csv
  - Example: Conwy_20201002_data1.csv
- Name corresponds to estuary (Conwy, Dyfi, Kent, Milford Haven).
- startdate is in YYYYMMDD.
- dataset is an index (1–N) indicating chronological datasets since the start date.

## Estuary coordinates and reference details (Table 1 overview)
- Conwy
  - Eastings: 278,636.800
  - Northings: 371,878.877
  - Vertical reference (ODN): -0.686 m
- Kent
  - Eastings: 348,111.700
  - Northings: 483,305.838
  - Vertical reference (ODN): 4.206 m
- Dyfi
  - Eastings: 267,157.541
  - Northings: 297,651.400
  - Vertical reference (ODN): -0.295 m
- Milford Haven
  - Eastings: 198,933.337
  - Northings: 205,215.959
  - Vertical reference (ODN): -0.476 m

## Relevance for environmental monitoring and analysis
- Data are prepared for standardized analysis of environmental health and policy performance over time.
- Following the organisation’s monitoring approach, data should be verified, quality assured, cleaned, and transformed as needed.
- Datasets are intended to be stored and uploaded to appropriate portals to enable broader access and re-use, supporting data integration with other environmental datasets.