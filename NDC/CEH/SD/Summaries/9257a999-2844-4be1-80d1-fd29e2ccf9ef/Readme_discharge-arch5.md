# Code documentation for discharge calculation

## Overview
- Describes a modular R-based workflow for calculating river discharge from water level recorder (WLR) data.
- Designed for flexibility: each logger/station has its own script to accommodate different equipment and setups, including legacy loggers and stations with multiple loggers.
- Outputs include minute-interval discharge data and accompanying plots; warnings are provided for data issues (e.g., duplicate timestamps).

## System architecture and data flow
- Control flow: dis.control.R -> dis.function -> station-wise routines.
- Key components:
  - dis.control.R: generates discharge for one-minute intervals; handles user inputs and initiates processing; outputs CSVs and figures; uses timeSeries and ggplot2; detects and handles duplicate timestamps.
  - dis.functs.R: contains core calculation functions for discharge from WLR data.
  - Station scripts (e.g., stn_101.R): contain station-specific constants, data handling, and discharge calculation logic.
  - dis.plot: plotting utility to create discharge graphs (PNG).
  - mk.nullfile: utility to address duplicate timestamps by creating a placeholder file (manual integration required).
- Data sources and formats:
  - Input parameters include Site (Nilgiris or Aghnashini), script/data paths, start/end dates, and WLR names.
  - Outputs: CSV discharge records and PNG plots; time zone set to India for timestamp handling.

## Core calculation methods
- calc.disch.areastage
  - Purpose: compute discharge from a set of points describing a stage-discharge curve via nonlinear least squares.
  - Process:
    - Read stage-discharge points and processed WLR data.
    - Fit model: Discharge ~ p1 * (Stage)^p3 using nls with starting values p1=3, p3=5.
    - Obtain coefficients p1 and p3, then compute Discharge = p1 * (Stage)^p3.
  - Inputs: input file names (rooted paths).

- calc.disch.flume
  - Purpose: discharge calculation for a Montana flume using a specified flume equation.
  - Constants: p1 = 0.1771 (or 0.1765 from external resources), p3 = 1.55.
  - Calculation: Discharge = p1 * (Stage)^p3.
  - Inputs: processed WLR data file.

- calc.disch.weir
  - Purpose: discharge calculation for v-notch weirs (not for compound weirs).
  - Constants: p1 = 1.380278, p2 = 2.5.
  - Calculation: Discharge = p1 * (Stage)^p2.
  - Inputs: processed WLR data file.

## Station-specific example
- stn_101.R
  - Type: compound weir located below Kollari Betta.
  - Catchment area and land cover described; one-minute CSV input and time-zone handling.
  - Stage-based discharge calculation with two regimes:
    - Low stage (within V): Discharge = 1.09 * (1.393799 * (LowStage - 0.2065)^2.5)
    - High stage (above V): Discharge = 1.09 * [1.394 * ((HighStage - 0.2065)^2.5 - (HighStage - 0.603)^2.5) + 0.719 * (HighStage - 0.603)^1.5]
  - Post-processing: bind, sort by timestamp, round to five digits, convert discharge to depth by dividing by catchment area and converting to millimetres.
  - Emphasizes integration with station-specific constants and flow regimes.

## Data inputs, outputs, and metadata
- Inputs:
  - Site selection (Nilgiris or Aghnashini), time range, and specific WLRs to process.
  - Station-specific configuration files and root paths for data and outputs.
- Outputs:
  - CSV files with minute-interval discharge data.
  - Plots (PNG) of discharge (via dis.plot) for visualization.
- Metadata and provenance considerations:
  - Documentation of per-station constants, data sources, and processing steps is embedded in station scripts.
  - Some stations reuse or combine results from previously replaced loggers, requiring careful provenance tracking.

## Data quality and governance considerations for Data Stewards
- Data consistency and standards:
  - Multiple loggers and station routines can produce non-uniform outputs; centralized conventions for timestamps, units (Discharge in m^3/s, depth in mm), and time zones are essential.
  - Duplicated timestamps trigger warnings; dedicated mk.nullfile workflow is provided to mitigate duplicates (manual file copying required).
- Metadata and documentation:
  - Each station script contains constants, data formats, and processing steps; ensure up-to-date metadata for each WLR and station.
  - Clear records of which logger contributes to a given discharge calculation for traceability.
- Data availability and interoperability:
  - The modular approach helps accommodate different station types (weirs, flumes, compound systems) but requires consistent data schemas for seamless sharing and reuse.
  - Time-series data processed at minute-level intervals improves granularity but demands robust versioning and archiving.
- Update and maintenance:
  - Because loggers are moved/replaced over time, workflows must document which scripts correspond to which hardware configurations and how to merge outputs from legacy systems.
  - Dependency management (R packages timeSeries and ggplot2) should be maintained to ensure reproducibility.

## Practical deployment notes
- User inputs:
  - Site and data paths, start/end dates, and WLRs to process must be provided by the user for dis.control.R.
- Quality checks:
  - dis.control.R issues warnings for duplicate timestamps; mk.nullfile provides a remediation path for persistent duplicates.
- Visualization and reporting:
  - dis.plot generates discharge plots to accompany numeric outputs, aiding review by data stewards and stakeholders.

## Challenges and maintenance considerations
- Handling incomplete or inconsistent user needs across diverse datasets and stations.
- Timely acquisition of data from various data creators and loggers.
- Ensuring metadata completeness and standardized formats across multiple systems and historic data.
- Managing large or complex datasets (e.g., multiple loggers, non-interoperable legacy formats) and ensuring scalable processing.
- Keeping abreast of updated constants or calibration changes for different station types (weirs, flumes, compound systems).

## Summary
Code documentation for discharge calculation provides a modular, station-aware framework for deriving river discharge from water level data, with explicit methods for area-stage, flume, and weir-based calculations, plus station-specific implementations and data quality controls. From a data stewardship perspective, the document highlights the importance of standardized inputs, robust metadata, duplicate-timestamp handling, provenance tracking, and maintainable processes to ensure that discharge data are accurate, traceable, and readily shareable across large datasets and diverse stations.