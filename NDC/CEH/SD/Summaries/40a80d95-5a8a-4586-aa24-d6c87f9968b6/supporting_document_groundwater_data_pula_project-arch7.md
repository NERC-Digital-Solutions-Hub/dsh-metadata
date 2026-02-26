# PULA Groundwater data folder

## Overview
- String of 25 data files containing in situ groundwater measurements (water table depth and physico-chemical parameters) in the Gaborone catchment, Botswana.
- Time period: May 2017 – June 2018.
- Collected by teams from the Botswana Department of Water Affairs, BIUST, and the University of Aberdeen.
- Part of the NERC-funded PULA project assessing groundwater response to extreme rainfall and flooding and spatial variability in water quality across areas with different geology and land use.
- Sampling aimed to capture spatial variability, with practical access considerations driving site selection.

## Data collection and sampling design
- Strategy 1: Spatial mapping across 22 boreholes, near-monthly measurements (monthly or less) of GWD, pH, temperature, EC, and TDS.
  - 149 measurement occasions on 41 days (11 campaigns) yielding 456 measurements (75 GWD, 95 pH, 96 T, 95 EC, 95 TDS).
- Strategy 2: High-temporal-resolution (5-minute) timeseries at 3 boreholes, focused on a subset of parameters (GWD, temperature, EC; with GWD also measured at some times).
  - 18/05/2017 – 09/06/2018 period, 861,816 measurements (324,353 GWD, 324,376 T, 213,087 EC).
- Borehole locations cover spatial variability; automatic dataloggers used at some sites to enhance temporal resolution.

## Instruments and measurement methods
- Strategy 1 (manual, near-monthly):
  - GWD: Hydrotechnik dipmeter; depth referenced to borehole casing.
  - pH, temperature, EC, TDS: HI-98129 portable tester; pumped grab samples after 5 minutes flushing.
- Strategy 2 (automatic, high-frequency):
  - GWD, temperature, EC: Solinst Levelogger (LT/LTC); some sites with LTC (GWD, T, EC), one with LT (GWD, T).
  - Data recorded as freshwater head; barometric compensation applied using Barologger data.
- Data processing (depth): barometric compensation, conversion to freshwater head, and depth correction using Strategy 1 measurements with linear interpolation for non-sampling dates.
- Datalogger download events: eight sessions (Aug 2017, Sep 2017, Nov 2017, Nov 2017, Nov 2017, Jan 2018, Mar 2018, Jun 2018).

## Data processing, calibration, and quality control
- Calibration and units:
  - GWD: Strategy 1 0.01 m resolution (factory calibration); Strategy 2 0.001 m resolution (manual dipmeter calibration used for final depth).
  - pH: 0.01 resolution; Hanna HI-98129; calibration with standard pH 7 solution.
  - Temperature: Strategy 1 0.1 °C; Strategy 2 0.001 °C; factory calibration (or instrument-specific calibration noted).
  - EC: Strategy 1, 1 µS/cm; Strategy 2, 0.1 µS/cm; factory calibration.
  - TDS: Strategy 1 1 ppm; factory calibration.
- Quality control: datasets checked for obvious measurement errors and anomalous datalogger records; clearly erroneous entries removed.
- Data integrity notes: near-monthly data (Strategy 1) may have gaps due to logistical constraints and occasional instrument failure.

## Data structure and file naming
- File types:
  - Strategy 1: 22 files named PULA_GW_level_physicochem_***.csv
  - Strategy 2: 3 files named PULA_GW_timeseries_***.csv
- Content and columns:
  - Strategy 1 files: 7 columns — measurement date (dd/mm/yyyy), measurement time (hh:mm), GWD (m), pH, T (°C), EC (µS/cm), TDS (ppm).
  - Strategy 2 files: 5 columns — measurement date (dd/mm/yyyy), measurement time (hh:mm:ss), GWD (m), T (°C), EC (µS/cm) where available.
- The borehole list (Table 1) provides names, coordinates (lat/long in decimal degrees), measurement period/frequency, and parameters collected; several boreholes are equipped with automatic dataloggers.

## Geospatial context and GIS relevance
- Data include geolocated boreholes across the Gaborone catchment, enabling map-based visualization of groundwater depth and water quality indicators.
- Two scales of data enable:
  - Spatial distribution mapping (Strategy 1) of groundwater levels and water quality parameters across many boreholes.
  - High-frequency time series (Strategy 2) for trend and anomaly detection at selected sites.
- Considerations for GIS use:
  - Data gaps and varying temporal resolutions between strategies.
  - Need for barometric correction and depth normalization when integrating Strategy 2 with Strategy 1.
  - Metadata on instruments, calibration, and units supports consistent symbolization and unit conversion in maps and time-enabled visualisations.

## Summary for GIS use
- The PULA Groundwater data folder provides a georeferenced, multi-parameter groundwater dataset for the Gaborone catchment (May 2017–June 2018), suitable for creating map-based visualisations of groundwater depth and water quality across space and time.
- With 22 boreholes (monthly data) plus 3 boreholes with 5-minute time series, the dataset supports both broad spatial analyses and detailed temporal analyses.
- Care is required to handle data gaps, different measurement resolutions, and processing steps (barometric correction, depth interpolation) to ensure accurate GIS representations.