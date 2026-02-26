# R implementation of the Ecological Risk due to Flow Alteration (ERFA) method

- Purpose and scope
  - Provides an R-based implementation of the ERFA methodology to assess ecological risk from river flow alterations.
  - Designed for baseline and scenario flow time series; applicable beyond the Mekong region and can be used wherever suitable data exist.
  - Developed under the TEFRIC project ( Cambodia-focused but region-agnostic in use).

- Background and method overview
  - ERFA framework originated from Laizé et al. (2014) for Europe and adapted for climate-change assessments in Cambodia/Mekong by Thompson et al. (2014, 2018).
  - Core idea: quantify ecological risk as a function of changes in flow regime, focusing on key flow variability components (magnitude, timing, frequency, duration, rate of change).

- Data inputs and setup
  - Requires at least two monthly mean river flow time series at a location: a baseline (historic or natural) and a scenario (e.g., management, climate projection).
  - Allows definition of the hydrological year based on the river regime and user-defined high/low flow percentiles (default high = Q5, low = Q95).
  - TEFRIC ERFA is provided with example Mekong datasets to illustrate usage.

- Monthly Flow Regime Indicators (MFRIs)
  - Converts annual series (per simulation year) into ten MRFIs that summarize regime characteristics.
  - Based on six hydrological variables; for each of high-flow and low-flow periods:
    - Four medians
    - Four interquartile ranges (IQRs)
    - Two modes (timing-related indicators)
  - Specific MFRIs include:
    - Magnitude and frequency for high flows (HF5, HF4, HF3, HF1)
    - Timing (month of maximum flow, HF3)
    - Magnitude and frequency for low flows (LF5, LF4, LF3, LF1)
    - Timing for minimum flow (LF3)
  - The indicators are computed per year, then summarized across the period.

- Change detection and risk classification
  - Calculates absolute differences between scenario and baseline MRFIs.
  - Applies user-definable thresholds to determine significance:
    - For median and IQR-based MRFIs: percent-change thresholds (default 30%)
    - For mode-based MRFIs: integer change in month (default 1 month)
  - Aggregates results to classify ecological risk by flow regime (separately for high and low flows):
    - No risk: 0 MRFIs differ significantly
    - Low risk: 1 MRFI differs
    - Medium risk: 2–3 MRFIs differ
    - High risk: 4–5 MRFIs differ
  - Uses a traffic-light color coding scheme to denote overall risk class.

- Outputs and user interactions
  - Produces MRFI difference metrics and an overall risk classification.
  - Includes visual outputs such as ERFA matrices and hydrological plots.
  - Allows exporting plots and results and optionally including baseline data in plots.
  - Provides a user-friendly interface to adjust: water year definition, high/low flow percentiles, and significance thresholds.

- System requirements and installation
  - Requires R (tested with versions up to 3.6.1) and the Shiny package; can run in R or R Studio.
  - TEFRIC ERFA is delivered as TEFRIC_ERFA.zip, which includes:
    - TEFRIC_MAIN.R (launch script), server.R, ui.R (web interface)
    - TEFRIC ERFA Manual.PDF
    - FUNCTIONS (supporting R scripts)
    - www (UI assets)
    - Example project folders: Mekong_7GCMs_2deg and Mekong_HadCM3_1-6deg (INPUT subfolders for baseline and scenario time series and default settings)
- Example datasets and applications
  - Mekong_7GCMs_2deg: 30-year periods for 12 gauging stations; scenario data from seven GCMs with a 2°C global mean temperature increase.
  - Mekong_HadCM3_1-6deg: 12 gauging stations with HadCM3-based scenarios for 1–6°C warming increments.
  - Both datasets derived from MIKE SHE / MIKE 11 hydrological modelling (Thompson et al., 2013).
- User interface and workflow
  - On launch, the UI guides you through project setup and analysis:
    - Project directory selection
    - Site selection
    - Scenario selection
    - Current settings and ability to save custom settings
    - Options to export plots and results
    - Inclusion of baseline in plots
    - Definition of water year, thresholds, and low/high flow percentiles
    - ERFA matrix plot and interpretation
- Acknowledgements, licensing, and references
  - Acknowledges TEFRIC project support from NERC and collaboration among UCL, CEH, ITC, and Tonle Sap Authority.
  - References several foundational ERFA works (Laizé et al. 2014; Thompson et al. 2013, 2014, 2017, 2018).
  - Licensing details and full usage conditions are provided in the TEFRIC ERFA user manual. 
  - Disclaimer: software provided without warranty; user contact information requested for usage reporting.