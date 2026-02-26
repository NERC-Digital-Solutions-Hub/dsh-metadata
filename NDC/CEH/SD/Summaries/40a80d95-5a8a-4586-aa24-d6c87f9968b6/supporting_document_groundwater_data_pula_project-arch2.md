# PULA Groundwater data folder

## Overview
- 25 CSV data files documenting in situ groundwater measurements in the Gaborone catchment, Botswana.
- Period: May 2017 to June 2018; collected by the Botswana Department of Water Affairs, Botswana International University of Science and Technology, and the University of Aberdeen.
- Purpose: understand long-term groundwater response to the 2016–2017 floods, including water level and basic physico-chemical parameters, and assess spatial variability.
- Part of the NERC-funded PULA project, evaluating wider impacts of extreme rainfall and flooding on water quality across surface and groundwater with varied geology and land use.
- Sampling locations chosen to cover spatial variability and practical accessibility.

## Data content and structure
- Two data strategies:
  - Strategy 1: near-monthly, manual in situ measurements from 22 boreholes (Strategy 1 files total: 22).
  - Strategy 2: high-temporal-resolution (5-minute) timeseries from 3 boreholes (Strategy 2 files total: 3).
- Measured parameters:
  - Groundwater level depth (water table depth), groundwater temperature, pH, electrical conductivity (EC), total dissolved solids (TDS).
- Data files:
  - Strategy 1: PULA_GW_level_physicochem_***.csv (7 columns: date, time, GWD, pH, T, EC, TDS).
  - Strategy 2: PULA_GW_timeseries_***.csv (5 columns: date, time, GWD, T, EC if available).
- Raw data include notes on units and calibration as described below.

## Experimental design and sampling regime
- Strategy 1 (spatial mapping):
  - 22 boreholes across the catchment.
  - Measured monthly or less frequently; 41 sampling days across campaigns.
  - Totals: 149 measurement occasions; 456 measurements across parameters (GWD, pH, T, EC, TDS).
- Strategy 2 (high-frequency timeseries):
  - 3 boreholes with 5-minute logging (May 2017 – June 2018).
  - Totals: 861,816 measurements (324,353 GWD, 324,376 T, 213,087 EC).
- Spatial and temporal coverage designed to reflect flood-drought-flood cycles and regional variability.

## Methods and instrumentation
- Strategy 1 (manual, in situ):
  - Groundwater level: Hydrotechnik dipmeter; depth referenced to borehole casing.
  - Physico-chemical: pumped grab samples; pH, temperature, EC, TDS measured with Hanna HI-98129 portable tester.
  - Sampling after 5 minutes flushing from taps.
- Strategy 2 (automatic, high-temporal):
  - Groundwater level, temperature, EC recorded with Solinst Leveloggers (two LTC, one LT).
  - Raw levels expressed as freshwater head; barometric compensation applied using a Barologger; depth corrected using Strategy 1 data via linear interpolation.
  - 8 download dates aligned with Strategy 1 rounds.
- All measurements calibrated per instrument specifications (factory calibration; some cross-checks with manual dipmeter).

## Data quality and preprocessing
- Datasets screened for obvious errors (human entry mistakes, anomalous logger records); erroneous data removed.
- EC and TDS observations indicate freshwater; no salinity-based head corrections required beyond barometric adjustment.

## Calibration, units, and data quality control
- GWD (Strategy 1): meters; 0.01 m resolution; calibrated with manual dipmeter (factory calibration).
- GWD (Strategy 2): meters; 0.001 m resolution; calibrated via manual dipmeter.
- pH: unitless; resolution 0.01; calibration using standard pH solution.
- Temperature: Celsius; Strategy 1 0.1°C resolution; Strategy 2 0.001°C; factory calibration.
- EC: microSiemens per cm; Strategy 1 resolution 1 µS/cm; Strategy 2 resolution 0.1 µS/cm; factory calibration.
- TDS: ppm; Strategy 1 resolution 1 ppm; factory calibration.

## Temporal and spatial coverage
- Spatial: 22 boreholes across the Gaborone catchment to capture spatial variability in groundwater response.
- Temporal: May 2017 – June 2018, with near-monthly data (Strategy 1) and continuous 5-minute timeseries (Strategy 2).

## Relevance to environmental monitoring and archiving
- Provides standardized, quality-checked groundwater data suitable for trend analysis and policy evaluation.
- Data processing steps (barometric correction, interpolation) enable consistent depth estimates across strategies.
- File naming conventions and CSV format facilitate data reuse and integration with other datasets.
- Data quality controls and removal of erroneous measurements support reliable environmental monitoring outputs.
- Highlights limitations and gaps due to logistical constraints and occasional equipment failures, which analysts can account for in risk-aware assessments.