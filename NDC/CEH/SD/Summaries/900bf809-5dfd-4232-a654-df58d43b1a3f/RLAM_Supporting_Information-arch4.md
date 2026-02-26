# R implementation of the Load Apportionment Model (RLAM) determining relative quantities of phosphorus entering rivers

- Purpose and value
  - Provides an R-based implementation of the Load Apportionment Model (LAM) to rapidly quantify relative phosphorus inputs to rivers from sewage treatment works (CS) and diffuse sources (RRS).
  - Improves on the Excel version by enabling batch processing, reproducibility, and a user-friendly web front-end (R Shiny) for non-specialists.
  - Supports reuse by specialists and integration into broader data workflows.

- Model overview
  - LAM distinguishes two phosphorus entry pathways: constant sources (CS) and rain-related sources (RRS).
  - CS loads decrease with river flow due to dilution; RRS loads increase with flow.
  - Core math is a concentration–flow relationship, expressed as a power-law function of flow.
  - Original form: [P] = A·Q^(B-1) + C·Q^(D-1); Bowes et al. (2014) constrain B to zero: [P] = A·Q^(-1) + C·Q^(D-1).
  - RLAM uses the constrained form; inputs are Q and P (TP or SRP); coefficients A, C, D are estimated from data.
  - Outputs include phosphorus concentrations and loads from CS and RRS.

- Data inputs and validation
  - Inputs: one CSV per site containing Date, Q, and either TP, SRP, or both.
  - Data quality checks: discard files with missing/empty essential columns; remove rows with negative Q or TP/SRP; only CSV files loaded.
  - Folder structure: RLAM_MAIN.R, RLAM_Functions.R, server.R, ui.R; www with logo; INPUT folder with example site files.
  - File naming: site names derived from input file names; input data must include required columns.

- Running and using RLAM
  - Step-by-step:
    - Copy input CSVs to the INPUT folder.
    - Run RLAM_MAIN.R in R or RStudio.
    - The app scans INPUT to build a site list; by default selects the first file; options depend on available columns (TP, SRP, or both).
    - Load data: remove rows with missing/negative Q or TP/SRP values.
    - On site or variable change, fit four models on the full dataset; set Custom Coeffs to Autofit values.
    - Data Subset: use a slider to select a subset; model fits update automatically for the subset.
    - Custom Coefficients: fix one coefficient (A, C, or D) at a time and refit; plots update as you type prior to refit.
  - Outputs and visualization: plots include the hydrograph and model fits; supports viewing autofit and custom-fit results for full data and subsets.

- Outputs and dissemination
  - Export functionality creates an OUTPUT folder and saves:
    - Full data, autofit: RLAM_REPORT_AUTOFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_FULLDATA_[site]_[variable].csv
    - Full data, custom coefficients: RLAM_REPORT_CUSTOMFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_FULLDATA_[site]_[variable].csv
    - Subset, autofit: RLAM_REPORT_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
    - Subset, custom coefficients: RLAM_REPORT_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
  - Each PDF includes a summary page with site name, chosen variable, fitting type, data point count, start/end points, A, C, D, Q cross-over point, and time-series plots plus concentration/load decompositions.
  - Spreadsheet outputs contain:
    - Date, Q
    - MODELLED_CONCENTRATION_CS, MODELLED_CONCENTRATION_RRS (μg/L)
    - MODELLED_LOADS_CS, MODELLED_LOADS_RRS (mg/s)
    - MODELLED_LOADS_PER_DAY_CS, MODELLED_LOADS_PER_DAY_RRS (t/d)

- System requirements
  - R (tested with 4.4.x; works with 4.4.0/4.4.1) and Shiny (1.9.1); ggplot2 for plotting.
  - Windows OS; can run via R or R Studio.
  - Install required packages: shiny and ggplot2 (RStudio is optional for a more user-friendly environment).

- Reproducibility and governance
  - Provides a transparent, reproducible workflow for estimating phosphorus source contributions across multiple sites.
  - Facilitates batch processing and standardized reporting, enabling consistent data-to-decision workflows for nutrient mitigation planning.

- References
  - Bowes et al. (2008, 2014) foundational work on modelling phosphorus inputs and the constrained coefficient approach.
  - Links to related publications for methodological context.