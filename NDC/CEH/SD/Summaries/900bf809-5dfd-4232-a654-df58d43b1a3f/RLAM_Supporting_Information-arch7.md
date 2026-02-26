# R implementation of the Load Apportionment Model (RLAM) determining relative quantities of phosphorus entering rivers

## Overview
- Implements the Load Apportionment Model (LAM) to determine relative phosphorus (P) entering rivers from constant sources (CS) and rain-related sources (RRS).
- Based on Bowes et al. (2008) with refinement from Bowes et al. (2014); uses a simple, rapid model linking P concentration to river flow (Q).
- Uses Equation 2 (as per Bowes 2014): [P] = A.Q^-1 + C.Q^(D-1), enabling separation of CS and RRS contributions and deriving concentrations and loads from inputs.

## Models and Outputs
- Provides four model configurations:
  - Whole dataset autofit coefficients
  - Whole dataset with custom coefficients
  - Data subset autofit coefficients
  - Data subset with custom coefficients
- Outputs per model include:
  - Summary page with site, variable (TP or SRP), fit type, observations, start/end points, coefficients A, C, D, Q crossover point (QCP), and % observations dominated by CS.
  - Hydrograph with data subset indicators.
  - Plots of modelled vs observed P and P split into CS and RRS contributions.
  - CSV spreadsheets detailing modeled concentrations and loads:
    - MODELLED_CONCENTRATION_CS
    - MODELLED_CONCENTRATION_RRS
    - MODELLED_LOADS_CS
    - MODELLED_LOADS_RRS
    - MODELLED_LOADS_PER_DAY_CS
    - MODELLED_LOADS_PER_DAY_RRS
- Outputs are generated for:
  - Whole dataset (autofit and custom)
  - Data subset (autofit and custom)

## File Format and Folder Structure
- RLAM main folder contains:
  - RLAM_MAIN.R (launch script)
  - RLAM_Functions.R (core functions)
  - server.R (Shiny server)
  - ui.R (Shiny UI)
  - www/UKCEH-Logo_Long_Positive_RGB.JPG (UI asset)
  - INPUT/ (example site CSV files)
    - Examples: Cut_Paley_Street.csv, Evenlode_Cassington_Mill.csv, Kennet_Woolhampton.csv, Thames_Sonning.csv
- Input data: one CSV per site with columns Date (dd/mm/yyyy), Q (m3/s), and optionally TP (μg/L) and/or SRP (μg/L).
- Naming: site names derived from CSV filenames (minus .csv).

## Inputs and Data Quality
- Required: Date and Q; TP and/or SRP optional.
- Data quality checks:
  - Files with missing Date, Q, TP, or SRP are discarded.
  - Rows with missing/negative Q or negative TP/SRP are removed.
- Pre-processing ensures inputs are suitable for model fitting and plotting.

## System Requirements and Installation
- Requires R (tested with 4.4.x) and R Studio (optional) on Windows.
- R packages: shiny and ggplot2.
- Documentation and links for Shiny and ggplot2 provided.

## User Interface and Running the App
- Launch RLAM_MAIN.R to open a web interface with:
  - Site selection dropdown (single)
  - Predicted variable dropdown (TP, SRP, or both, depending on data)
  - Data subset slider to select a range (with visual indicators on the hydrograph)
  - Export button to generate outputs
  - Time-series plot of discharge with subset indicators
  - Whole dataset section showing autofit results and corresponding plots
  - Data Subset section mirroring the whole dataset outputs
  - Custom Coefficients section allowing one coefficient (A, C, or D) to be fixed and re-fitted
- App behavior:
  - On start, inputs are scanned from INPUT; first file alphabetically is selected by default.
  - If only TP or SRP is present, only that option is shown for prediction; if both are present, both are available with default alphabetical selection.
  - Data are loaded and cleaned (removing invalid rows) before fitting models.
  - Changing site or variable refits four models on the full dataset.
  - Adjusting the data subset via slider automatically resets autofit coefficients for the new subset.
  - Custom coefficients require a re-fit action; plots update in real-time to reflect interim changes.

## Exporting and Outputs
- Exports PDFs and CSVs to an OUTPUT sub-folder (created if absent) alongside INPUT.
- File naming conventions:
  - Whole dataset autofit: RLAM_REPORT_AUTOFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_FULLDATA_[site]_[variable].csv
  - Whole dataset custom: RLAM_REPORT_CUSTOMFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_FULLDATA_[site]_[variable].csv
  - Data subset autofit: RLAM_REPORT_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
  - Data subset custom: RLAM_REPORT_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
- Each PDF includes site info, variable, fit type, data range, coefficients, QCP, and plots.
- CSVs include time series and modeled concentrations and loads for CS and RRS.

## Practical GIS Context
- Facilitates batch processing of multiple river sites, enabling integration with GIS workflows.
- Generates time-series and load/discharge data suitable for spatial linking with river networks and watershed analyses.
- Outputs can be used to populate GIS-based dashboards or to accompany spatial analyses of phosphorus inputs and mitigation priorities.

## References
- Bowes M.J., et al. (2014). Identifying priorities for nutrient mitigation using river concentration-flow relationships: The Thames basin, UK. Journal of Hydrology.
- Bowes M., Smith J., Jarvie H., & Neal C. (2008). Modelling of phosphorus inputs to rivers from diffuse and point sources. Science of the Total Environment.