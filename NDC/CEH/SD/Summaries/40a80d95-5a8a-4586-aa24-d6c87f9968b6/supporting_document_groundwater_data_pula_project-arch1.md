# PULA Groundwater data folder

## Overview
- Contains 25 data files from the Gaborone catchment, Botswana, May 2017 – June 2018.
- Collected to understand long-term groundwater response to the 2016–2017 floods and spatial variability in response.
- Part of the NERC-funded PULA project examining water quality impacts of extreme rainfall and flooding across surface and groundwater systems.
- Sampling covers spatial variability (22 boreholes) and high-temporal-resolution monitoring (3 boreholes).

## Data content and structure
- 22 Strategy 1 files: near-monthly measurements of groundwater level depth (GWD), pH, temperature (T), electrical conductivity (EC), and total dissolved solids (TDS) from 22 boreholes.
- 3 Strategy 2 files: high-temporal-resolution (5-minute) timeseries for three boreholes measuring GWD, T, and EC (where available).
- File naming and formats:
  - Strategy 1: PULA_GW_level_physicochem_***.csv (7 columns).
  - Strategy 2: PULA_GW_timeseries_***.csv (5 columns).

## Sampling design and temporal coverage
- Strategy 1: spatial mapping across 22 boreholes with low temporal resolution (monthly or less); 41 sampling days across 149 occasions, yielding about 456 measurements across parameters (GWD, pH, T, EC, TDS).
- Strategy 2: high-temporal-resolution monitoring (5-minute intervals) for 3 boreholes from 18/05/2017 to 09/06/2018; 861,816 measurements total (324,353 GWD; 324,376 T; 213,087 EC).
- Sampling campaigns were aligned with flood-drought-flood cycles to capture variability.

## Measurement methods and instrumentation
- Strategy 1:
  - GWD measured in situ with a Hydrotechnik dipmeter; depth referred to borehole top.
  - pH, temperature, EC, and TDS measured from pumped grab samples using HI-98129 portable tester.
- Strategy 2:
  - Automatic logging with Solinst Leveloggers (two with LTC for GWD/T/EC, one with LT for GWD/T).
  - Heads converted to freshwater depth; barometric compensation applied using a Barologger at Otse-ramotswa landfill BH2.
  - Depth corrections applied via linear interpolation using Strategy 1 measurements.
- Calibration and units:
  - GWD: Strategy 1 (0.01 m resolution), Strategy 2 (0.001 m); factory vs manual dipmeter calibration.
  - pH: 0.01 resolution; calibration with pH 7.01 solution.
  - Temperature: Strategy 1 0.1 °C; Strategy 2 0.001 °C.
  - EC: Strategy 1 1 µS/cm; Strategy 2 0.1 µS/cm.
  - TDS: Strategy 1 1 ppm.
- Data were not corrected beyond stated calibrations; EC and TDS observed as freshwater values.

## Data quality and control
- Data screened for obvious errors (recording mistakes, anomalous logger data) and such issues removed manually.
- Data include gaps due to logistical constraints, equipment failures, and human error; near-monthly datasets are incomplete for certain months/parameters.

## Data structure and access
- All data provided as CSV files, two data formats:
  - Strategy 1: PULA_GW_level_physicochem_***.csv with 7 columns (date, time, GWD, pH, T, EC, TDS).
  - Strategy 2: PULA_GW_timeseries_***.csv with 5 columns (date, time, GWD, T, EC).
- Metadata includes borehole identifiers, coordinates (Table 1 details), measurement periods, and parameters per borehole.
- Data management notes that datasets (and derived datasets) may be uploaded to portals with metadata for discoverability.

## Key considerations and potential analyses
- Investigate spatial patterns in groundwater level, pH, temperature, EC, and TDS across boreholes and their variability with flood cycles.
- Compare near-monthly Strategy 1 data with high-frequency Strategy 2 data to understand short-term dynamics and lagged responses.
- Assess data gaps and uncertainties due to sampling schedule and instrument reliability when performing trend analyses or model development.
- Use borehole coordinates and sampling history to contextualize hydrogeological variability (geology, land use) within the catchment.