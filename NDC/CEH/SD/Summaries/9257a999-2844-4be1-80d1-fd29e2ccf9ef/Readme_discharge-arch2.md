# Code documentation for discharge calculation

## Overview
- Describes a modular, station-centric framework for calculating stream discharge from water level data.
- Emphasizes flexibility to tweak components for field conditions, with some stations combining results from multiple loggers or past equipment changes.
- Outputs include discharge time series in CSVs and visual figures; plots are produced with ggplot2.
- Includes data quality steps such as duplicate timestamp handling and clear data flow from raw WLR data to final discharge estimates.

## Core Structure
- Each logger has an independent code module to allow site-specific adaptations.
- Some stations combine results from multiple loggers (e.g., original WLR plus flank measurements like flumes), reflecting historical equipment moves.
- The processing pipeline follows: dis.control.R -> dis.functs.R -> station-specific routines (e.g., stn_101.R).

## Control flow and main scripts
- dis.control.R
  - Generates discharge values for one-minute intervals.
  - Input requirements: Site (Nilgiris or Aghnashini), relative script/data output paths, start/end dates, and names of WLRs to process.
  - Uses timeSeries (for time aggregation) and ggplot2 (for plotting).
  - Calls dis.plot to produce plots.
  - Issues warnings if duplicate timestamps exist when multiple loggers are present; uses mk.nullfile to remove duplicates.
- dis.functs.R
  - Contains the functions invoked by the control script.
  - Key functions include:
    - calc.disch.areastage: computes discharge from a rating curve using non-linear least squares (NLS).
    - calc.disch.flume: computes discharge for a Montana flume via a specified flume equation.
    - calc.disch.weir: computes discharge for v-notch weirs.
    - mk.nullfile: creates a placeholder file to flag/avoid duplicate timestamps when multiple loggers are present (manual copy required to WLR/NULL folder).
    - dis.plot: generates and saves discharge plots as PNGs.
- Code organization by station (example: stn_101.R).

## Data inputs and configuration
- Inputs required by dis.control.R:
  - Site: Nilgiris or Aghnashini.
  - Relative file names for scripts and outputs.
  - Start/end dates and time interval display (in months).
  - Names of water level recorders to process.
- Data handling:
  - Uses one-minute CSV files from processed WLR data.
  - Ensures timestamps are recognized as date-time objects and aligns time zones to India.
  - Duplicated timestamps are warned about; duplicates are mitigated via a null file approach (mk.nullfile) when multiple loggers exist.

## Key functions

- calc.disch.areastage
  - Purpose: estimate discharge from a stage-discharge rating curve using non-linear least squares.
  - Process:
    - Read rating curve point file and processed WLR data.
    - Run NLS: Discharge ~ p1 * (Stage)^p3.
    - Obtain coefficients p1 and p3; compute Discharge = p1 * (Stage)^p3.
  - Inputs: input file names (and root).

- calc.disch.flume
  - Purpose: calculate discharge for a Montana 3" flume.
  - Constants:
    - p1 ≈ 0.1771 (0.1765 cited in external sources)
    - p3 = 1.55
  - Formula: Discharge = p1 * (Stage)^p3.
  - Inputs: input file names (and root).

- calc.disch.weir
  - Purpose: compute discharge for v-notch weirs (not suitable for compound weirs).
  - Formula: Discharge = p1 * (Stage)^p2 with p1 = 1.380278, p2 = 2.5.
  - Inputs: input file names (and root).

- mk.nullfile
  - Purpose: test for and address duplicate timestamps when a station has multiple loggers.
  - Behavior: suggests creating a null file to avoid duplicates; requires manual copying to WLR/NULL folder.
  - Input: duplicated timestamps (from dis.control.R).

- dis.plot
  - Purpose: generate and save discharge plots using ggplot2.
  - Input: formatted WLR data produced by dis.control.R.

## Station example

- stn_101.R
  - Description: compound weir located just below Kollari Betta.
  - Catchment context: area 293,562.50 m^2; land cover includes Acacia mearnsii and Eucalyptus globulus; upper reaches are grassland with Sheila patches.
  - Steps:
    - Define constants (catchment data, file names, time settings).
    - Read one-minute CSV; parse timestamps; set India time zone.
    - Define low-stage and high-stage parameters for the weir equation.
    - Compute discharge:
      - Low stage: Discharge = 1.09 * (1.393799 * (Low Stage - 0.2065)^2.5)
      - High stage: Discharge = 1.09 * [ (1.394 * ((High Stage - 0.2065)^2.5 - (High Stage - 0.603)^2.5)) + (0.719 * (High Stage - 0.603)^1.5) ]
    - Combine, sort by timestamp, round discharge to five digits.
    - Convert to depth of discharge in metres by dividing by catchment area; multiply by 1000 to express in millimetres.
  - Output: time-aligned discharge and derived depth values for the station.

## Outputs and storage
- Outputs include:
  - CSV files of discharge time series.
  - PNG plots of discharge over time.
- Data quality and provenance:
  - WLR data integration from multiple loggers is supported but flagged for duplicates.
  - Duplicates can be addressed via mk.nullfile and manual placement in WLR/NULL.

## Tools, environment, and dependencies
- R-based workflow.
- Libraries: timeSeries (for time aggregation) and ggplot2 (for plotting).
- Modular, station-specific scripts to accommodate field conditions and equipment history.