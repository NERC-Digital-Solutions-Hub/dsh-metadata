# R implementation of the Ecological Risk due to Flow Alteration (ERFA) method

- Data context and aim
  - Provides an R-based implementation of the ERFA methodology as part of the TEFRIC project focused on environmental flows.
  - Although developed around Mekong River Basin data in SE Asia, the approach is applicable wherever baseline and scenario river flow time series are available.
  - Designed to support assessing ecological risk from flow alterations and to produce interpretable outputs for decision-making.

- Methodology at a glance
  - Required inputs: at least two monthly mean river flow time series for a location — one baseline (historical/natural) and one scenario (e.g., a management plan or climate projection).
  - Hydrological processing: compute annual variables for each year of the simulation period; define the hydrological year, and set low/high flow thresholds using user-defined percentiles (default high flows at the 5th percentile, low flows at the 95th percentile of the baseline).
  - Monthly Flow Regime Indicators (MRFIs): derive ten indicators per period (baseline and each scenario) that summarize magnitude, variability, timing, and frequency of flows. They are built from six hydrological variables:
    - Four medians (HF1–HF4 or LF1–LF4)
    - Four interquartile ranges (IQRs) for high/low flows
    - Two modes (months of maximum and minimum flow)
  - High-flow vs. low-flow separation: five MRFIs describe high-flow regime; five describe low-flow regime.
  - Significance and risk
    - Compare scenario vs. baseline MRFIs; use user-defined thresholds to determine significance (default: 30% change for medians/IQRs; one-month difference for mode-based MRFIs).
    - Overall ecological risk is classified by how many MRFIs differ significantly from baseline, with separate assessments for high and low flows.
    - Visualized using a traffic-light scheme (no risk, low, medium, high) based on the count of significantly changed MRFIs.
  - Output focus: changes in MRFIs, a matrix plot (ERFA matrix), and plots/tables of results for interpretation and dissemination.

- Data inputs and governance
  - Requires clear data provenance and metadata for both baseline and scenario series (data source, time coverage, units, quality, and any processing steps).
  - Encourages data owners to maintain versioned inputs and document thresholds and hydrological year definitions to ensure reproducibility.
  - Outputs are designed to support communication with policy colleagues and other stakeholders through clear visuals and summaries.

- Software, installation, and system requirements
  - Built in R and relies on the Shiny package for the user interface.
  - Tested with R up to version 3.6.1 and Shiny up to version 1.3.2.
  - Requires:
    - R (or R Studio as a convenience layer)
    - Shiny package
  - Distribution: TEFRIC_ERFA.zip containing all code, manuals, and example datasets.

- Project structure and components
  - TEFRIC_MAIN.R: launcher for TEFRIC ERFA
  - server.R and ui.R: core Shiny app components
  - TEFRIC ERFA Manual.PDF: user manual
  - FUNCTIONS: scripts implementing runtime functions
  - www: user interface assets (images, etc.)
  - Mekong_7GCMs_2deg and Mekong_HadCM3_1-6deg: example project directories, each with INPUT subfolders for baseline, scenario data, and default settings
  - Example datasets include:
    - Mekong_7GCMs_2deg: 30-year periods for 12 gauging stations; scenarios from seven GCMs corresponding to +2°C
    - Mekong_HadCM3_1-6deg: same stations; HadCM3 scenarios for 1–6°C increments
  - Data origin: derived from MIKE SHE / MIKE 11 hydrological modelling work related to the Mekong River Basin

- User interface and workflow
  - On launch, the app opens a web interface with:
    - Project directory selection
    - Site selection
    - Scenario selection
    - Current settings and ability to save custom settings
    - Options to export plots and results, including baseline data in plots
    - Definitions of water year, low/high flow percentiles, and significance thresholds
    - Visualization tools: hydrological plots and MRFI-based results
    - ERFA matrix plot and interpretation guidance

- Regional focus and applicability
  - While the TEFRIC ERFA example data focus on the Mekong River Basin, the method is general and can be applied to any river where baseline and scenario flow time series are available.
  - Supports assessment of climate change impacts, water resource development, or other flow-altering scenarios.

- Acknowledgements, licensing, and references
  - Developed under the TEFRIC project (NERC grant NE/R009325/1) with collaboration between UCL, CEH, ITC, and the Tonle Sap Authority.
  - Acknowledges workshop participants and partner institutions.
  - References foundational works: Laizé et al. (2014) on ERFA; Thompson et al. (2018, 2017, 2014, 2013) on TEFRIC and Mekong applications.
  - Conditions of use: see the TEFRIC ERFA user manual and licensing details.
  - Disclaimer: no warranty; users are encouraged to report usage details to the project team.