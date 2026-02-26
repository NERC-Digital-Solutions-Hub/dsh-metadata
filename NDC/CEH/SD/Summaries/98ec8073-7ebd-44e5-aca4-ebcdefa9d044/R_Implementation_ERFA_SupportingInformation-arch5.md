# R implementation of the Ecological Risk due to Flow Alteration (ERFA) method

- Overview: TEFRIC ERFA is an R-based implementation of the ERFA methodology for assessing ecological risk from river flow alteration. Built under the TEFRIC project, it focuses on SE Asia (Mekong River Basin) but is applicable wherever baseline and scenario flow time series are available. The software is intended to support environmental flow decision-making and risk classification.

- Purpose and concepts:
  - Compares baseline (historical/natural) and scenario monthly flow time series at a location.
  - Uses a set of Monthly Flow Regime Indicators (MRFIs) to quantify changes in flow magnitude, timing, frequency, and duration.
  - Classifies ecological risk based on how many MRFIs differ significantly from baseline (no, low, medium, high risk) with a traffic-light coding system.

- Data requirements and governance considerations for Data Stewards:
  - Input data: at least two monthly mean river flow series (baseline and scenario) for the same site.
  - User-definable definitions: water year, high/low flow percentiles (default high = 5th percentile, low = 95th percentile of baseline).
  - Thresholds for significance: default 30% change for medians/IQRs; 1-month change for modes; supports governance through documentation of data provenance, processing steps, and threshold choices.
  - Metadata and provenance: output includes MRFI differences, ERFA results, plots, and the ability to document data and settings for reproducibility.

- Method details (ERFA/TEFRIC ERFA):
  - Hydrological variables are calculated yearly, then condensed into ten MRFIs (five for high flows, five for low flows) based on six hydrological variables (four medians, four IQRs, two modes).
  - MRFIs capture magnitude, variability, timing, and duration characteristics.
  - Significant changes are identified by comparing baseline and scenario MRFIs against user-defined thresholds.
  - Overall risk is determined by the number of MRFIs that differ significantly, with a separate assessment for high and low flows.

- System requirements and installation:
  - Requires R (tested with versions up to 3.6.x) and the Shiny package.
  - Can run in R or R Studio (preferred environment).
  - TEFRIC ERFA materials are provided as TEFRIC_ERFA.zip, with instructions to unzip and run TEFRIC_MAIN.R.

- Files, structure, and data organization:
  - TEFRIC_MAIN.R: launch script.
  - server.R and ui.R: core Shiny app components.
  - TEFRIC ERFA Manual.PDF: user manual and guidance.
  - FUNCTIONS: collection of R scripts used during runtime.
  - www: interface images and assets.
  - Mekong_7GCMs_2deg and Mekong_HadCM3_1-6deg: example project folders, each containing INPUT subfolders for baseline and scenario data and a default settings file.
  - Example datasets: Mekong datasets based on MIKE SHE / MIKE 11 hydrological modelling; scenarios include multiple GCM projections (7 GCMs at 2° resolution; HadCM3 at 1–6°).

- User interface and workflow:
  - Web-based interface launched by TEFRIC_MAIN.R.
  - Features: select project directory, site, scenario(s), and current settings; save custom settings; export plots and results; include baseline in plots; define water year and flow percentiles; set significance thresholds; view ERFA matrix and interpretation.

- Outputs and usability for data sharing:
  - Produces MRFI differences (scenario vs baseline), ERFA risk classification, and visual plots.
  - Exports results and plots for reporting and data sharing; supports documentation of the processing workflow for transparency and reuse.

- Acknowledgments and references:
  - Developed under NERC TEFRIC project (grant NE/R009325/1) with collaboration between UCL, CEH, ITC, and Tonle Sap Authority.
  - Acknowledges Cambodian government agencies, universities, NGOs, and workshop participants.
  - References foundational ERFA work and TEFRIC project outputs.

- Conditions of use and contact:
  - See the user manual for installation, operation, and licensing details.
  - Disclaimer: no warranty; intended for useful application with attribution.
  - Contact: geog-tefric-erfa@ucl.ac.uk for information about use.