# R implementation of the Load Apportionment Model (RLAM) determining relative quantities of phosphorus entering rivers

## Overview
- Implements the Load Apportionment Model (LAM) in R, following the original Bowes et al. work, to determine relative phosphorus loads entering rivers from constant sources (CS) and rain-related sources (RRS).
- Replaces the Excel-based version with an R-based suite and a user-friendly Shiny front-end for non-specialists.
- Enables batch processing and reuse by specialists, facilitating data-driven insights for river phosphorus management.

## Models and outputs
- Core model foundation:
  - Phosphorus concentration [P] is modeled as a function of river flow Q, distinguishing CS and RRS contributions.
  - Original form: [P] = A·Q^(B−1) + C·Q^(D−1); Bowes et al. (2014) constrain B to zero: [P] = A·Q^(-1) + C·Q^(D−1).
  - RLAM uses Equation 2 with inputs Q and [P] (TP or SRP) to estimate coefficients A, C, D.
- Outputs:
  - Phosphorus concentrations and loads from CS and RRS derived from fitted coefficients.
  - Model fits and diagnostic plots (modelled vs observed, CS vs RRS contributions) and data subset analyses.

## Data inputs and quality checks
- Input data format:
  - One CSV per site in an INPUT folder.
  - Required columns: Date (dd/mm/yyyy) and Q (discharge, m3/s); TP and/or SRP may be present.
- Data quality rules:
  - Rows with missing or negative Q are removed.
  - Rows with negative TP or SRP are removed.
  - Automatic screening removes files missing required columns or containing empty columns.
- File naming and site identification:
  - Site names are derived from input file names (minus the .csv extension).

## Data management and workflow
- Automated data ingestion:
  - RLAM scans the INPUT folder to identify usable CSV files and populates a site selection control.
- Interactive analysis:
  - Shiny front-end provides:
    - Site selection
    - Predicted variable selection (TP, SRP, or both, depending on inputs)
    - Data subset slider to define a time window for analysis
    - Real-time visualization of discharge time series and data subset
  - Four models are fitted for the full dataset; coefficient handling includes autofit and custom-fit options.
  - Data Subset mode automatically updates autofit and custom-fit results for the selected range.

## User interface and interaction
- RLAM front-end features:
  - Whole Dataset autofit results and plots
  - Whole Dataset autofit coefficients (A, C, D), Q crossover point, and dominance metrics
  - Whole Dataset plots for modelled vs observed and CS vs RRS contributions
  - Custom Coeffs mode to fix one coefficient at a time while re-fitting the others
  - Data Subset mode with equivalent outputs for the selected data window
  - Export option to save plots and coefficient data
- Custom coefficient workflow:
  - User enters a single coefficient (A, C, or D) and clicks a Refit button to fix that coefficient; other coefficients are re-estimated.
  - Plots update in real time to reflect rough changes before re-fit.

## Outputs and reporting
- Exports:
  - PDFs and CSVs saved to an OUTPUT folder (created if needed) with structured naming:
    - Whole dataset autofit: RLAM_REPORT_AUTOFIT_FULLDATA_[site]_[variable].pdf; RLAM_SPREADSHEET_AUTOFIT_FULLDATA_[site]_[variable].csv
    - Whole dataset custom fit: RLAM_REPORT_CUSTOMFIT_FULLDATA_[site]_[variable].pdf; RLAM_SPREADSHEET_CUSTOMFIT_FULLDATA_[site]_[variable].csv
    - Data subset autofit: RLAM_REPORT_AUTOFIT_SUBSET_[start]-TO-[end]_[site]_[variable].pdf; RLAM_SPREADSHEET_AUTOFIT_SUBSET_[start]-TO-[end]_[site]_[variable].csv
    - Data subset custom fit: RLAM_REPORT_CUSTOMFIT_SUBSET_[start]-TO-[end]_[site]_[variable].pdf; RLAM_SPREADSHEET_CUSTOMFIT_SUBSET_[start]-TO-[end]_[site]_[variable].csv
- Report contents:
  - Summary page with site name, predicted variable, fit type, observations, start/end data-points, A, C, D, QCP, and dominance metrics
  - Hydrograph with selected subset markers
  - Model plots for autofit and custom-fit scenarios
- Spreadsheet contents:
  - Date, Q, MODELLED_CONCENTRATION_CS, MODELLED_CONCENTRATION_RRS
  - MODELLED_LOADS_CS, MODELLED_LOADS_RRS
  - MODELLED_LOADS_PER_DAY_CS, MODELLED_LOADS_PER_DAY_RRS

## System requirements and installation
- Software:
  - R (tested with version 4.4.0/4.4.1) and R Studio recommended for user friendliness
  - R packages: shiny and ggplot2
- Environment:
  - Windows is the tested platform; RLAM can be run in R or R Studio
  - Instructions include installing R, optionally R Studio, and required packages

## File structure and running the app
- Main RLAM folder contains:
  - RLAM_MAIN.R (launch script)
  - RLAM_Functions.R (core RLAM functions)
  - server.R (Shiny server)
  - ui.R (Shiny UI)
- Sub-folder www with UKCEH logo image
- INPUT sub-folder with sample CSVs (e.g., Cut_Paley_Street.csv, Evenlode_Cassington_Mill.csv, Kennet_Woolhampton.csv, Thames_Sonning.csv)
- OUTPUT sub-folder created automatically upon exporting
- Running steps:
  - Copy input CSVs to INPUT
  - Run RLAM_MAIN.R in R/R Studio
  - RLAM scans INPUT to build site list and loads data
  - Default behavior selects the first file; data cleaning occurs on startup
  - Changing site or variable triggers re-fitting and updated visualizations
  - Use slider to define data subset and observe corresponding autofit/custom-fit updates

## Reproducibility and reuse
- All processing is implemented as reusable R scripts, enabling batch processing for multiple sites
- Outputs provide both visual and data-tabular results for auditing and further analysis

## References
- Bowes M.J. et al. (2008, 2014) foundational works on phosphorus inputs and river concentration-flow relationships
- Links to related publications provided for context and methodological grounding