# R implementation of the Load Apportionment Model (RLAM) determining relative quantities of phosphorus entering rivers

- Purpose and scope
  - Presents an R-based implementation of the Load Apportionment Model (LAM) to rapidly determine relative contributions of phosphorus entering rivers from sewage treatment works (continuous sources, CS) and diffuse, rain-related sources (RRS).
  - Improves on a prior Excel version by enabling batch processing, better usability for non-specialists, and protection against inappropriate model edits.

- Model and methodology
  - Based on LAM (Bowes et al., 2008); distinguishes CS and RRS contributions to river phosphorus concentrations.
  - Phosphorus enters via CS (concentration decreases with flow due to dilution) and via RRS (concentration increases with flow).
  - Uses a simple concentration–flow relationship modeled as a power-law function.
  - Core equations:
    - Equation 1: [P] = A·Q^(B−1) + C·Q^(D−1)
    - Bowes et al. (2014) constrain B to zero, yielding Equation 2: [P] = A·Q^(−1) + C·Q^(D−1)
  - Outputs: phosphorus concentrations and loads from CS and RRS, expressed through coefficients A, C, and D.
  - Data inputs required: Q (discharge) and [P] (TP or SRP).

- Implementation and file structure
  - Implemented as an R suite linked to a Shiny web front-end for accessibility.
  - Core files (RLAM folder): RLAM_MAIN.R, RLAM_Functions.R, server.R, ui.R.
  - User interface assets: www/ (logo), and an INPUT folder with example site CSVs.
  - Input data organization: one CSV per site; columns Date, Q, TP and/or SRP; date format dd/mm/yyyy; mandatory Q; optional TP and/or SRP.

- Data handling and quality checks
  - Automated checks during startup:
    - Only CSV files with required columns are considered.
    - Files with empty critical columns are discarded.
  - Data cleaning:
    - Remove rows with missing or negative Q.
    - Remove rows with negative TP or SRP.
  - Data quality supports robust model fitting and transparent reporting.

- System requirements and installation
  - Requires R (tested with 4.4.x) and R Shiny; optionally R Studio for a friendlier environment.
  - Necessary packages: shiny and ggplot2.
  - Designed for Windows but can run on other OS with R/Shiny installed.

- User interface and workflow
  - Main components:
    - Site selection (dropdown)
    - Predicted variable selection (TP, SRP, or both if present)
    - Data-subset slider to select a portion of the time series
    - Export button to generate outputs
    - Time-series plot of discharge with subset indicators
    - Whole-dataset outputs (autofit coefficients, plots)
    - Whole-dataset custom-coefficients (one coefficient fixed at a time)
    - Data-subset outputs (autofit and custom-coefficients for the selected subset)
  - Model fitting behavior:
    - On startup and when site/variable changes, models are fitted to the full dataset.
    - Subset selections automatically re-fit autofit and custom-coefficient models for the subset.
  - Custom coefficient fitting:
    - Coefficients are linked; only one coefficient can be fixed at a time.
    - Users enter a custom value for A, C, or D and click to re-fit; plots update instantly for rapid feedback.

- Running the application
  - Steps:
    - Copy input CSVs to the INPUT folder.
    - Run RLAM_MAIN.R in R or RStudio.
    - The app scans INPUT and populates site and variable options; defaults to the first file (alphabetical) with appropriate columns.
  - Data preparation:
    - Only non-empty TP/SRP columns are used; entries with negative Q are removed; negative TP/SRP removed.

- Outputs and reporting
  - Exported outputs:
    - PDFs and CSVs saved to an OUTPUT sub-folder (created if absent) with standardized naming:
      - Whole dataset autofit: RLAM_REPORT_AUTOFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_FULLDATA_[site]_[variable].csv
      - Whole dataset with custom coefficients: RLAM_REPORT_CUSTOMFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_FULLDATA_[site]_[variable].csv
      - Data subset autofit: RLAM_REPORT_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
      - Data subset with custom coefficients: RLAM_REPORT_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
  - PDF contents:
    - Summary page with site, variable, model fitting type, observations, data range, coefficients A, C, D, QCrossover-Point (QCP), and percentage of observations CS-dominant.
    - Hydrograph with data-subset markers.
    - Plots for model fit and separation of CS vs RRS contributions.
  - CSV contents:
    - Date, Q, MODELLED_CONCENTRATION_CS, MODELLED_CONCENTRATION_RRS, MODELLED_LOADS_CS, MODELLED_LOADS_RRS, MODELLED_LOADS_PER_DAY_CS, MODELLED_LOADS_PER_DAY_RRS.

- Data governance, transparency, and reuse
  - Outputs provide traceable model coefficients and projectable splits between CS and RRS, supporting monitoring and policy evaluation.
  - Encourages openness by clearly reporting inputs, model fitting procedures, and results; data can be exported for sharing and review.

- Limitations and disclaimers
  - Distributed without warranty; intended as a tool to aid analysis and reporting.

- References
  - Bowes M.J. et al. (2008, 2014) on phosphorus inputs and river concentration–flow relationships, underpinning the LAM approach.