# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Fortnightly measurements.rft'

## Overview
- Provides data-structure details for two Fortnightly Clocaenog datasets (2015-2016).
- Aims to support data usage, linking site-level environmental measurements with soil respiration and related variables.

## Datasets included
- Fortnightly measurments_Clocaenog_2015-2016_site.csv
  - 20 columns, 32 rows
  - Site-level measurements
- Fortnightly measurments_Clocaenog_2015-2016_soil respiration.csv
  - 38 columns, 32 rows
  - Soil respiration dataset (plus temperature, moisture, PAR)

## Data structure and variables

- Dataset 1: Fortnightly measurments_Clocaenog_2015-2016_site.csv
  - Date (Day/Month/Year)
  - Rainfall (mm)
  - Throughfall for Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control (all in mm)
  - Water table depth for each plot:
    - Plot1 - Warming: cm
    - Plot2 - Warming: mm
    - Plot3 - Control: mm
    - Plot4 - Drought: mm
    - Plot5 - Drought: mm
    - Plot6 - Control: mm
    - Plot7 - Warming: mm
    - Plot8 - Drought: mm
    - Plot9 - Control: mm

- Dataset 2: Fortnightly measurments_Clocaenog_2015-2016_soil respiration.csv
  - Date (Day/Month/Year)
  - Soil respiration for Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control (mg CO2-C m-2 h-1)
  - Soil temperature for Plot1 - Warming through Plot9 - Control (°C)
  - Soil moisture for Plot1 - Warming through Plot9 - Control (Vol%)
  - Photosynthetic active radiation (PAR) for Plot1 - Warming through Plot9 - Control (µmol m-2 s-1)
  - Columns follow a pattern with per-plot treatment descriptors: e.g., Plot1 - Warming, Plot2 - Warming, Plot3 - Control, etc., plus corresponding environmental measurements.

## Temporal coverage and sampling
- Fortnightly measurements (biweekly) across 2015-2016.
- Date column present in both datasets to anchor measurements.

## Units and data quality notes
- Units vary across variables:
  - Rainfall: mm
  - Throughfall: mm
  - Water table depth: mixed (Plot1 noted in cm; others shown in mm)
  - Soil respiration: mg CO2-C m-2 hr-1
  - Soil temperature: °C
  - Soil moisture: Vol%
  - PAR: µmol m-2 s-1
- Data are structured by plot and treatment (Warming, Drought, Control), enabling treatment-effect analyses.
- As a supplement to other documentation, this file emphasizes data structure and column semantics to aid data preparation and integration.

## How analysts can use this data
- Merge site and soil respiration datasets on Date and Plot/Treatment identifiers to study relationships between environmental conditions and soil processes.
- Assess treatment effects (Warming, Drought, Control) on rainfall interception (throughfall), water table depth, soil respiration, temperature, and moisture.
- Build predictive models linking rainfall, soil moisture and temperature to soil respiration across plots and treatments.
- Use PAR data to explore photosynthetically active radiation’s role in soil processes across plots.

## Metadata and access notes
- Document acts as a supplement to the Clocaenog Fortnightly measurements supporting documentation.
- Detailed data structure descriptions support discoverability and re-use within broader data portals.