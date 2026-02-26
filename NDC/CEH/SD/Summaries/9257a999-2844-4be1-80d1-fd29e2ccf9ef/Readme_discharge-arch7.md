# Code documentation for discharge calculation

## Overview
- Documents a modular workflow to compute river discharge from water level recorder (WLR) data.
- Discharge is calculated at one-minute intervals and outputs CSVs and figures.
- Supports multiple stations/loggers, with station results sometimes combined (e.g., stn_107.R with stn_110.R).
- Uses timeSeries for time aggregation and ggplot2 for plotting; warnings for duplicate timestamps are handled.

## Basic structure
- Each logger has separate code to allow component-level tweaking for field conditions.
- Station-specific routines can be combined when needed (e.g., a station location may involve multiple loggers).

## Discharge calculation control: dis.control.R
- Purpose: generate discharge for one-minute intervals.
- Inputs to user:
  - Site (Nilgiris or Aghnashini)
  - Relative paths for scripts and data/outputs
  - Start and end dates/times (displayed in months)
  - Names of water level recorders to process
- Outputs:
  - CSV of discharge data and accompanying figures
- Key behaviors:
  - Aggregates time-series data with timeSeries
  - Plots via dis.plot
  - Issues warnings for duplicated timestamps when multiple loggers exist
  - Uses mk.nullfile to remove duplicates (manual copy into WLR/NULL as needed)

## Discharge calculation functions: dis.functs.R
- calc.disch.areastage
  - Purpose: compute discharge from a stage-discharge curve using nonlinear least squares (NLS).
  - Model: Discharge = p1 * (Stage)^p3
  - Steps: read stage-discharge file, read processed WLR data, run nls with start parameters p1=3, p3=5, extract p1 and p3, compute Discharge.
- calc.disch.flume
  - Purpose: discharge for a Montana 3" flume using a specified flume equation.
  - Model: Discharge = p1 * (Stage)^p3 with p1=0.1771, p3=1.55
  - Steps: read WLR data, apply formula, produce discharge.
- calc.disch.weir
  - Purpose: discharge for v-notch weirs (non-compound).
  - Model: Discharge = p1 * Stage^p2 with p1=1.380278, p2=2.5
  - Steps: read WLR data, apply formula, produce discharge.
- mk.nullfile
  - Purpose: identify duplicate timestamps and suggest a null-file workaround.
  - Output: guidance to create a WLR/NULL file (manual copy needed).
- dis.plot
  - Purpose: generate and save discharge plots using ggplot2.
  - Output: PNG plots; input is formatted WLR data from dis.control.R

## Code for different stations
- stn_101.R
  - Example of a station: compound weir located below Kollari Betta
  - Catchment area: 293,562.50 m^2; land cover details noted
  - Process:
    - Define constants and file names
    - Read one-minute CSV, parse timestamps, set time zone to India
    - Define low-stage and high-stage parameters for the weir
    - Compute discharge:
      - Low stage: Discharge = 1.09 * (1.393799 * (LowStage - 0.2065)^2.5)
      - High stage: Discharge = 1.09 * ((1.394 * ((HighStage - 0.2065)^2.5 - (HighStage - 0.603)^2.5)) + (0.719 * (HighStage - 0.603)^1.5))
    - Assemble results, sort by timestamp
    - Round discharge to five digits
    - Convert to depth of discharge in metres: Discharge_depth = Discharge / catchment_area
    - Convert to millimetres: Depth_mm = Discharge_depth * 1000

## Data inputs and outputs
- Inputs:
  - Processed WLR data
  - Stage-discharge data for areastage calculations
  - Station-specific data files and constants
- Outputs:
  - Discharge time series (m^3/s)
  - Depth of discharge time series (mm)
  - CSVs and plots for visualization and GIS-compatible mapping
- Dependencies:
  - R scripts dis.control.R, dis.functs.R, and station scripts (e.g., stn_101.R)
  - R packages: timeSeries, ggplot2

## GIS-relevant considerations
- Enables generation of map-ready discharge data linked to catchment areas and station locations.
- Supports combining data from multiple loggers/stations to enhance spatial coverage.
- Emphasizes consistent timing (one-minute intervals) and time zone handling (India) for accurate spatial-temporal analysis.
- Handles data quality issues (duplicate timestamps) to ensure reliable GIS-derived visuals and analyses.
- Converts raw discharge to depth (mm) for intuitive map symbolism and integration with catchment attributes.