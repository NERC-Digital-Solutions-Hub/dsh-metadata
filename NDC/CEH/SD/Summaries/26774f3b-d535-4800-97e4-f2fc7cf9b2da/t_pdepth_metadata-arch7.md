# High-resolution temperature and precipitation measurements for fire-affected locations in Australia (2019-2020) and Tenerife (2020-2021)

## Overview
- Purpose: Monitoring environmental parameters related to runoff occurrence in fire-affected areas.
- Scope: Two study sites with precise spatial references and time-series data.

## Datasets and files
- Data files:
  - T_Pdepth_ma.csv (Madre del Agua, Tenerife)
  - T_Pdepth_ts.csv (Thompson reservoir, Victoria, Australia)
- Measurements: Temperature and precipitation depth in 10-minute intervals.

## Spatial details
- Madre del Agua (Tenerife, Spain): UTM 28N 28 R, coordinates 343340, 3119657
- Thompson reservoir (Victoria, Australia): UTM 55 H, coordinates 441956, 5822296

## Temporal coverage
- Madre del Agua: 17/11/20 to 19/11/2021
- Thompson reservoir: 28/03/19 to 13/01/2020

## Measurements and methods
- Parameters: Temperature (°C) and precipitation depth (mm)
- Resolution: 10-minute intervals
- Instrumentation: RainWise Rainew raingauge coupled to Onset HOBO pendant datalogger (UA-003-64)

## Data fields
- Date and time (dd/mm/yyyy hh:mm)
- Temperature (Temp: °C)
- Precipitation depth (P: mm)

## Completeness and observations
- Completeness: Full record
- Observations: Madre del Agua = 9723; Thompson = 10050

## Provenance and contributors
- Purpose: Monitoring environmental parameters related to runoff occurrence
- Contributors: Dr Jonay Neris Tome, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr, Dr Gary Sheridan

## GIS considerations
- Suitable as point features with timestamps for time-series analyses.
- Can be joined with other spatial datasets (hydrology, fire-affected zones) to assess runoff potential and climate interactions at high temporal resolution.