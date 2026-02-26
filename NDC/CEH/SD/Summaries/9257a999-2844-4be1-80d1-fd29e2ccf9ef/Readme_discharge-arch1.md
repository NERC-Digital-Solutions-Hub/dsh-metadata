# Code documentation for discharge calculation

- Overview
  - Purpose: generate discharge for one-minute intervals using water level recorder (WLR) data and/or rating-curve equations (area-stage, flume, or weir) to support site-specific hydrological analysis.
  - Architecture: modular, allowing each logger/station to have its own code for flexibility; stations may combine results from multiple loggers when loggers have been moved or replaced.
  - Key components: dis.control.R (orchestrator), dis.functs.R (calculation functions), station-specific scripts (e.g., stn_101.R), and plotting via dis.plot. Time series aggregation uses timeSeries; plotting uses ggplot2.
  - Data quality features: warnings for duplicated timestamps, capability to remove duplicates with mk.nullfile, and facilities to track and reuse data sources.

- Workflow
  - User inputs (dis.control.R): site (Nilgiris or Aghnashini), relative script/data paths, start/end dates, and which WLRs to process.
  - Processing flow: dis.control.R reads inputs, aggregates time series to minute intervals, detects duplicates, and delegates plotting to dis.plot.
  - Calculations: dis.functs.R contains methods to compute discharge depending on data and method chosen; outputs are written as CSVs and figures.
  - Outputs: discharge time series, plots (PNG), and metadata; datasets can be made discoverable with proper metadata.

- Calculation methods
  - calc.disch.areastage
    - Purpose: compute discharge from a stage-discharge rating curve using a non-linear least squares (NLS) fit.
    - Approach: read stage-discharge points and processed WLR data; fit nls(Discharge ~ p1*(Stage)^p3); obtain p1 and p3; compute Discharge = p1*(Stage)^p3.
    - Inputs/outputs: input files for stage-discharge and WLR data; outputs discharge values for each timestamp.
  - calc.disch.flume
    - Purpose: compute discharge for a Montana 3" flume using a fixed flume equation.
    - Constants: p1 = 0.1771 (0.1765 in some references), p3 = 1.55.
    - Calculation: Discharge = p1 * (Stage)^p3.
  - calc.disch.weir
    - Purpose: compute discharge for v-notch weirs.
    - Constants: p1 = 1.380278, p2 = 2.5.
    - Calculation: Discharge = p1 * (Stage)^p2.
  - mk.nullfile
    - Purpose: handle duplicate timestamps when a station has multiple loggers.
    - Behavior: suggests creating a null file in WLR/NULL to avoid duplicate-timestamp issues; requires manual copying.
  - dis.plot
    - Purpose: generate and save discharge plots using ggplot2.
    - Input: formatted WLR data produced by dis.control.R.

- Station-specific example
  - stn_101.R
    - Context: compound weir located below Kollari Betta; catchment area ~293,562.50 m^2 with land cover including Acacia mearnsii and Eucalyptus globulus.
    - Steps: define constants (catchment area, data file names, timezone India), read one-minute CSV, interpret timestamps, set low/high stage parameters for the weir, compute discharge with respective formulas, merge and sort by timestamp, round to five digits, convert discharge to depth (divide by catchment area to get metres, convert to millimetres by multiplying by 1000).

- End-to-end considerations
  - Data handling: supports combining data from multiple loggers and stations; accounts for time zones and timestamp formats; includes duplicate detection and remediation guidance.
  - Outputs and traceability: maintains a reproducible workflow with explicit inputs and data lineage; outputs include CSVs and plots for reporting and further analysis.
  - Applicability: designed for field conditions where loggers may be moved or replaced, enabling flexible recalibration via station-specific scripts and rating-curve updates.

- Practical notes for analysts
  - The system emphasizes statistically driven discharge estimation (areastage) alongside physically defined equations (flume, weir), enabling validation and cross-checks.
  - Quality checks (duplicate timestamps, data gaps) are integral to ensure reliable time-series discharge estimates.
  - The framework supports exporting ready-to-use plots and data for dissemination and downstream modeling.