# R implementation of the Ecological Risk due to Flow Alteration (ERFA) method

- Overview
  - An R-based implementation of the ERFA method, part of the TEFRIC project (Translating Environmental Flow Research in Cambodia).
  - Although focused on SE Asia (Mekong data provided as examples), the code can be applied wherever baseline and scenario river flow time series exist.
  - Includes a user-friendly interface (Shiny) to compute ecological risk from flow alterations.

- Method at a glance
  - Data requirements: two monthly mean river flow time series at a location — one baseline (historical/natural) and one scenario (e.g., management changes or climate projections).
  - Hydrological year: allows definition of the year used for calculating indicators based on river regime.
  - Thresholds for high/low flows: defined by percentiles of the baseline series (default high = 95th percentile, low = 5th percentile; user-definable).
  - Monthly Flow Regime Indicators (MRFIs): ten indicators derived from six hydrological variables per year, split into:
    - High-flow indicators: medians, IQRs, and timing (mode-based month of maximum flow).
    - Low-flow indicators: medians, IQRs, and timing (mode-based month of minimum flow).
  - Output per scenario: absolute differences between scenario and baseline MRFIs.
  - Significance thresholds: user-defined (default 30% change for medians/IQR-based MRFIs; default 1-month change for mode-based MRFIs).
  - Risk classification: counts how many MRFIs differ significantly; classifies overall ecological risk for high and low flows separately into no/low/medium/high, using a traffic-light scheme.
  - Data products: MRFI values, ERFA risk classification, and plots/results suitable for reporting and decision-making.

- Data and inputs
  - Requires baseline and scenario monthly river discharge time series.
  - Produces a decomposition into MRFIs that summarize magnitude, variability, timing, and duration aspects of flow regimes.

- Output and products
  - MRFI time-series and comparisons (scenario vs baseline).
  - ERFA risk classification (per flow regime: high and low).
  - ERFA matrix plot and other visual outputs.
  - Exportable plots and environmental flow results; ability to include baseline in plots.

- Implementation and usage
  - System requirements: R (tested with versions up to 3.6.1) and Shiny.
  - Distribution: TEFRIC_ERFA.zip containing:
    - TEFRIC_MAIN.R (launch), server.R, ui.R (Shiny app), TEFRIC ERFA Manual.PDF.
    - FUNCTIONS (supporting R scripts), www (UI assets).
    - Example project folders: Mekong_7GCMs_2deg and Mekong_HadCM3_1-6deg with INPUT subfolders for baseline and scenarios.
  - How to run: open TEFRIC_MAIN.R to launch a web interface; use it to select project, site, scenario(s), and settings; adjust water year definition, low/high flow percentiles, and significance thresholds; save settings and export results.
  - User interface features: project/site selection, scenario selection, current settings, saving custom settings, exporting outputs, including baseline in plots, defining water year, setting percentiles, thresholds, and viewing the ERFA matrix plot.

- Data sets and regional context
  - Example Mekong River Basin datasets derived from MIKE SHE / MIKE 11 hydrological modeling.
  - Two dataset groups:
    - Mekong_7GCMs_2deg: 30-year periods for 12 gauging stations with seven GCM-driven scenarios (2° resolution, ~5% significance).
    - Mekong_HadCM3_1-6deg: 12 stations with HadCM3 projections across 1–6°C warming increments (1° increments).
  - These examples illustrate multi-model and multi-scenario application, but the tool is region-agnostic.

- Acknowledgments and license
  - Developed under TEFRIC with collaboration from UCL, CEH, ITC, and Tonle Sap Authority.
  - Acknowledges workshop participants and partner institutions.
  - Conditions of use and licensing are described in the user manual; disclaimer of warranty included.

- References
  - Foundational ERFA work and subsequent TEFRIC adaptations (Laizé et al. 2014; Thompson et al. 2018; and related Mekong-focused studies).