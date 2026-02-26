# Code documentation for discharge calculation

## Overview
- Documents a modular workflow to compute discharge (m^3/s) from water level data, with support for multiple stations and loggers.
- Outputs include per-minute discharge data (CSV) and graphical figures (PNG) to enable data exploration and product creation for end users.
- Data sources are water level recorders (WLRs); workflows handle data cleaning, formatting, and conversion to discharge and depth units.

## Global structure and flow
- Each logger has separate code for flexibility; some stations combine results from multiple loggers due to equipment changes over time.
- Control flow: dis.control.R -> dis.functs.R -> station-specific routines (e.g., stn_101.R).

## Key scripts and functions

### dis.control.R
- Purpose: generate discharge for one-minute intervals over a specified time window.
- Inputs (user-entered): Site (Nilgiris or Aghnashini), relative script/data output paths, start/end dates, list of WLRs to process.
- Outputs: CSV of discharge data and figures.
- Libraries: timeSeries (time aggregation) and ggplot2 (graphing).
- Behavior: calls dis.plot to generate graphs; warns on duplicated timestamps (when multiple loggers exist); uses mk.nullfile to handle duplicates.

### dis.functs.R
- Central repository of calculation functions:
  - calc.disch.areastage: computes discharge from a stage-discharge relation using nonlinear least squares (NLS).
    - Process: read stage-discharge points, read processed WLR data, fit Discharge ~ p1*(Stage)^p3, start with p1=3, p3=5, derive p1 and p3, then compute Discharge = p1*(Stage)^p3.
  - calc.disch.flume: calculates discharge for a Montana 3" flume.
    - Formula: p1*(Stage)^p3 with p1=0.1771 and p3=1.55.
  - calc.disch.weir: computes discharge for v-notch weirs.
    - Formula: Discharge = p1*Stage^p2 with p1=1.380278 and p2=2.5.
  - mk.nullfile: tests for duplicate timestamps when a station has multiple loggers and suggests creating a null file to avoid issues; requires manual copying into WLR/NULL/ folder.
  - dis.plot: generates and saves discharge plots using ggplot2.
  
### Station-specific script: stn_101.R
- Example for a compound weir located below Kollari Betta.
- Catchment area: 293,562.50 m^2; land cover details noted.
- Steps:
  - Define constants (catchment area, type, file names).
  - Read one-minute CSV data, ensure timestamp is recognized as date-time and set to India time zone.
  - Define low-stage and high-stage parameters for the weir equations.
  - Compute discharge using:
    - Low stage: Discharge <- 1.09*(1.393799*((Low Stage-0.2065)^2.5))
    - High stage: Discharge <- 1.09*((1.394*(((High Stage-0.2065)^2.5) - ((High Stage-0.603)^2.5))) + (0.719*(High Stage-0.603)^1.5))
  - Combine, sort by timestamp, round to five digits.
  - Convert discharge to depth: depth = (Discharge / catchment area) in metres, then scale to millimetres (multiply by 1000).

## Calculation methods (technical details)
- Area-stage method (calc.disch.areastage): fits stage-discharge data with non-linear least squares to obtain p1 and p3; used to estimate discharge from water level data when a rating curve is available.
- Flume method (calc.disch.flume): relies on a fixed empirical relationship for a 3" Montana flume.
- Weir method (calc.disch.weir): uses a power-law relationship for v-notch weirs.
- All methods produce Discharge in m^3/s; depth equivalents are derived by dividing by catchment area and converting to millimetres for interpretation.

## Data inputs and outputs
- Inputs: processed WLR data, one-minute CSVs, station metadata (locations, catchment details), and constants for chosen discharge models.
- Outputs: per-minute discharge time series (CSV) and corresponding plots (PNG) for visualization and reporting.

## Data quality, robustness, and workflow considerations
- Duplicate timestamps are a known issue when multiple loggers exist; the system flags warnings and provides a pathway (mk.nullfile) to mitigate with a manual null file.
- Time handling emphasizes correct time zones (e.g., India) and date-time parsing to ensure accurate temporal alignment.
- The structure supports evolving field conditions: stations can reference multiple loggers and switch between different discharge calculation routines as needed.
- Documentation illustrates actionable steps for computing discharge and converting to depth, enabling reproducible data products for broader use.

## How this supports data exploration and usage
- Provides an end-to-end pipeline from raw WLR data to actionable discharge time series and depth measures.
- Enables end users to explore discharge dynamics through generated CSVs and plots, supporting monitoring, policy, and field decision-making.
- Encourages data quality improvements by highlighting potential duplication issues and offering remediation steps.