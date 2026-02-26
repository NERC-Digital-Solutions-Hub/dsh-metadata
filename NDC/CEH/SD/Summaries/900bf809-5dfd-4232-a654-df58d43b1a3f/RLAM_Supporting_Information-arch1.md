# R implementation of the Load Apportionment Model (RLAM) determining relative quantities of phosphorus entering rivers

## Overview
- Implements the Load Apportionment Model (LAM) to rapidly determine relative quantities of phosphorus entering rivers from sewage treatment works (CS) and diffuse sources (RRS).
- RLAM is a re-implementation in R (as a reusable script suite) with a user-friendly Shiny front-end for non-specialists.
- Extends an existing Excel version by addressing limited functionality, usability, and data protection concerns.

## Model background
- LAM distinguishes two input pathways for phosphorus: constant sources (CS) and rain-related sources (RRS).
- CS concentrations decrease with increasing river flow (dilution), while RRS concentrations increase with flow.
- Phosphorus concentration [P] is modeled as a power-law function of flow Q:
  - Base form: [P] = A·Q^(B−1) + C·Q^(D−1)
  - Bowes et al. (2014) constrain B to zero, yielding: [P] = A·Q^(-1) + C·Q^(D−1)
- RLAM uses this constrained form to derive phosphorus concentrations and loads from CS and RRS.
- Required inputs: time series of Q and [P] (TP or SRP). Coefficients A, C, D are obtained via standard model fitting.

## Input data and data quality
- Input data files: one CSV per site; file name used as site name.
- Columns: Date (dd/mm/yyyy), Q (m3/s), TP (μg/L), SRP (μg/L). Date and Q are mandatory; TP and/or SRP may be present.
- Data cleaning: rows with missing/negative Q are removed; rows with negative TP or SRP are removed.
- The app validates input files and only includes files with required columns and non-empty values.

## System requirements and installation
- Implemented in R; requires R 4.4.x (tested with 4.4.0/4.4.1) and Shiny 1.9.1; on Windows.
- Optional: R Studio for user-friendly environment.
- Required packages: shiny and ggplot2 (for plotting).

## File structure and components
- RLAM folder contains:
  - RLAM_MAIN.R: launcher script
  - RLAM_Functions.R: core RLAM functions
  - server.R: Shiny server logic
  - ui.R: Shiny UI
  - www/UKCEH-Logo_Long_Positive_RGB.JPG: UI logo
  - INPUT/: folder with example CSV files (e.g., Cut_Paley_Street.csv, Evenlode_Cassington_Mill.csv, Kennet_Woolhampton.csv, Thames_Sonning.csv)
- Input files are scanned at startup to populate site and variable options.

## Running the app
- Steps:
  - Copy input CSV files into the INPUT sub-folder.
  - Run RLAM_MAIN.R in R or R Studio.
  - RLAM scans INPUT and lists valid files for site selection.
  - By default, the first file (alphabetical) is selected; if only TP or SRP is present, only that option is shown; if both present, both are available with the first alphabetically selected.
  - Data loading excludes rows with missing/negative Q or negative TP/SRP.
  - Fitting is performed for the full dataset when the site or variable changes; Custom Coeffs default to Autofit Coeffs.

## User interface and workflow
- UI components:
  - Site selection (single)
  - Predicted variable selection (TP, SRP, or both)
  - Data subset slider to define a subset of data points
  - Export button to save plots and model results
  - Time series plot of discharge with subset markers
  - Whole dataset outputs:
    - Autofit coefficients, Q crossover point (QCP), and percentage of time dominated by CS
    - Plots: modelled vs observed and CS/RRS contributions
  - Data Subset outputs: same as Whole Dataset but for the chosen data range
  - Custom Coeffs: allow fixed coefficient values (A, C, or D) one at a time; re-fit with the fixed coefficient while others vary
- Data subset behavior:
  - Adjusting the slider re-fits and updates visualizations; autofocus coefficients update to reflect the new subset
  - Custom coefficients can be entered; plots update immediately; a separate re-fit action fixes the coefficient and re-runs the model

## Model fitting and outputs
- Four models are fitted:
  - Whole dataset Autofit
  - Whole dataset Custom Coeffs
  - Data subset Autofit
  - Data subset Custom Coeffs
- Coefficients provided:
  - A, C, D (with D representing the exponents for RRS)
  - Q Cross-over Point (QCP)
  - Percentage of observations dominated by constant sources (CS)
- Outputs for each fit:
  - Summary page in PDFs with site, variable, fit type, observations, start/end points, coefficients, QCP, CS dominance
  - Plots: hydrograph, modelled vs observed concentrations, and CS/RRS split
  - CSV spreadsheets with columns:
    - Date, Q
    - MODELLED_CONCENTRATION_CS (μg/L)
    - MODELLED_CONCENTRATION_RRS (μg/L)
    - MODELLED_LOADS_CS (mg/s)
    - MODELLED_LOADS_RRS (mg/s)
    - MODELLED_LOADS_PER_DAY_CS (t/d)
    - MODELLED_LOADS_PER_DAY_RRS (t/d)

## Data export and file management
- Exports are saved to an OUTPUT sub-folder (created if missing) alongside INPUT.
- Naming conventions:
  - Whole dataset autofit: RLAM_REPORT_AUTOFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_FULLDATA_[site]_[variable].csv
  - Whole dataset custom coefficients: RLAM_REPORT_CUSTOMFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_FULLDATA_[site]_[variable].csv
  - Data subset autofit: RLAM_REPORT_AUTOFIT_SUBSET_[start]-TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_SUBSET_[start]-TO_[end]_[site]_[variable].csv
  - Data subset custom coefficients: RLAM_REPORT_CUSTOMFIT_SUBSET_[start]-TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_SUBSET_[start]-TO_[end]_[site]_[variable].csv
- If no custom model or no data subset used, only autofit full-data outputs are saved; custom outputs overwrite existing files as needed.

## Reproducibility and data governance
- The approach explicitly tracks data sources and allows exported results to be stored with metadata in the filenames.
- The tool is provided without warranty and is intended for use by researchers and practitioners to identify phosphorus sources and assess mitigation priorities.

## References
- Bowes M.J. et al. (2014). Identifying priorities for nutrient mitigation using river concentration-flow relationships: The Thames basin, UK. Journal of Hydrology, 517, 1-12.
- Bowes M., Smith J., Jarvie H., & Neal C. (2008). Modelling of phosphorus inputs to rivers from diffuse and point sources. Science of the Total Environment, 395(2-3), 125-138.