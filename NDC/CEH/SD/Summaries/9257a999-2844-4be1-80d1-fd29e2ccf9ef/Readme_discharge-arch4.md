# Code documentation for discharge calculation

## Overview
- Describes a modular R-based workflow to compute water discharge from water level recorder (WLR) data.
- Designed for flexibility: each logger/station has its own script to accommodate field conditions and equipment changes.
- Supports combining results from multiple loggers at a station and generates both numerical and graphical outputs.
- Includes data quality checks and handling of duplicate timestamps.

## System architecture
- Control flow: dis.control.R -> dis.function -> station-wise routines.
- dis.control.R:
  - Generates discharge for one-minute intervals.
  - Inputs: site (Nilgiris or Aghnashini), relative script/data paths, start/end dates, and WLR names.
  - Outputs: CSV of discharge data and accompanying figures.
  - Uses timeSeries for aggregation and ggplot2 for plotting; calls dis.plot for visualizations.
  - Warns on duplicated timestamps; uses mk.nullfile to remove duplicates when multiple loggers exist.
- dis.functs.R:
  - Repository for functional calculations used by the control script.
  - Includes multiple discharge calculation methods (area-stage based) and utility functions (e.g., mk.nullfile, dis.plot).
- Station-specific scripts (e.g., stn_101.R):
  - Define station constants (catchment area, catchment type, file names).
  - Read one-minute CSV WLR data, parse timestamps, set the India time zone.
  - Apply stage-discharge equations (low/high stage logic for weirs/flumes).
  - Compile results, sort by time, round values, and convert discharge to depth (mm) by dividing by catchment area.

## Data inputs and outputs
- Inputs:
  - Processed WLR data and station-specific data files.
  - Station names and identifiers; catchment information.
  - Start and end times, and the list of water level recorders to process.
- Outputs:
  - CSV file with minute-by-minute discharge values.
  - PNG plots generated via dis.plot.
  - Optional null file to handle duplicate timestamps when multiple loggers exist (mk.nullfile).

## Processing pipeline and data handling
- Time handling:
  - Timestamps read and converted to date-time with India time zone.
- Duplicate timestamps:
  - Warnings if duplicates occur; mk.nullfile aids in removing duplicates by creating a placeholder to skip problematic timestamps.
- Aggregation and plotting:
  - timeSeries used for time-based aggregation; dis.plot uses ggplot2 to create discharge plots.
- Station-wise processing:
  - Each station script defines how to compute discharge based on available data and the appropriate physical model.

## Calculation methods (dis.functs.R)
- calc.disch.areastage:
  - Uses a non-linear least squares fit to a rating curve: Discharge = p1 * (Stage)^p3.
  - Input: stage-discharge point file and processed WLR data.
  - Fitting with starting parameters p1=3, p3=5; outputs coefficients to compute discharge.
- calc.disch.flume:
  - Montana 3" flume model with p1 = 0.1771 (0.1765 per some references) and p3 = 1.55.
  - Discharge = p1 * (Stage)^p3.
- calc.disch.weir:
  - V-notch weir model (single plain weir; not suitable for compound weirs).
  - Discharge = p1 * (Stage)^p2 with p1 = 1.380278, p2 = 2.5.
- Outputs from these calculations are combined per timestamp, then transformed to depth of discharge by dividing by catchment area and converting to millimetres.

## Station example: stn_101.R
- Describes a compound weir below Kollari Betta.
- Catchment area and land cover details.
- Steps include:
  - Defining constants and file names.
  - Reading one-minute WLR CSV, parsing timestamps, and setting time zone.
  - Applying low-stage and high-stage equations for the weir to compute discharge.
  - Stacking, sorting by time, rounding to five digits, and converting to depth in millimetres.

## Data governance and practical considerations for Data Leaders
- Modularity supports field-condition adaptations and easier governance of data processing pipelines.
- Clear data lineage: separate control script, functional calculators, and station-specific logic.
- Data quality: built-in checks for duplicate timestamps and documentation of handling duplicates (null file approach).
- Discoverability and reuse: standardized input/output formats and plotting facilitate sharing results with policy colleagues and partners.
- Transparency: explicit constants, station parameters, and formulas enable reproducibility and auditability across stations and data sources.
- Collaboration potential: structure allows coordination across stations and potential integration with a wider data community for discharge assessment.