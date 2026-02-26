# R implementation of the Load Apportionment Model (RLAM) determining relative quantities of phosphorus entering rivers

## Aim
- Provide a robust R-based implementation of the Load Apportionment Model (LAM) to determine relative phosphorus inputs to rivers from sewage works (CS) and diffuse sources (RRS).
- Improve on the original Excel version by enabling batch processing, reducing user error, and offering a user-friendly web front-end (R Shiny) for non-specialists.
- Support consistent environmental monitoring outputs suitable for scrutiny of health and policy performance over time.

## What RLAM does
- Implements LAM (Bowes et al., 2008) to quantify phosphorus entering rivers as total phosphorus (TP) or soluble reactive phosphorus (SRP) from constant sources (CS) and rain-related sources (RRS).
- Uses a concentration–flow relationship:
  - CS loads typically decrease with increasing flow due to dilution.
  - RRS loads typically increase with increasing flow.
- Applies a simplified model in Eq. 2: [P] = A.Q^-1 + C.Q^D-1, where B is constrained to zero (Bowes et al., 2014), enabling derivation of CS and RRS concentrations and loads from input Q and [P].
- Outputs model coefficients (A, C, D), Q crossover point (QCP), and the percentage of observations dominated by constant sources (%ObsCSDom).

## Model background and equations
- Base equation (Eq. 1) distinguishes CS and RRS contributions to [P] via a power-law in discharge Q.
- Bowes et al. (2014) constrain B to zero, yielding Eq. 2 used in RLAM.
- Required inputs: time series of Q and [P] (TP or SRP).
- Coefficients A, C, D are estimated from standard fitting techniques; these enable reconstruction of P concentrations and loads from CS and RRS.

## Input data and formats
- Per-site input: one CSV file with columns Date (dd/mm/yyyy), Q (m3/s), and optionally TP (μg/L) and/or SRP (μg/L).
- At least Date and Q are mandatory; TP and/or SRP may be present or absent.
- Data quality checks:
  - Rows with missing/negative Q or negative TP/SRP are removed.
  - App performs automated checks on input files in the INPUT folder (validates presence and non-emptiness of required columns).
- File naming: use clear site names; app uses CSV file names (without .csv) as site names.

## System requirements and installation
- RLAM consists of R scripts and uses Shiny and ggplot2.
- Tested with R 4.4.x and Shiny 1.9.1 on Windows.
- Requires R (and optionally R Studio) and installation of the Shiny and ggplot2 packages.
- RLAM files include:
  - Top-level: RLAM_MAIN.R (launch), RLAM_Functions.R (core functions), server.R, ui.R
  - www/UKCEH-Logo_Long_Positive_RGB.JPG
  - INPUT/ sample CSVs (e.g., Cut_Paley_Street.csv, Evenlode_Cassington_Mill.csv, Kennet_Woolhampton.csv, Thames_Sonning.csv)

## User interface and workflow
- RLAM_MAIN.R launches a Shiny web interface with:
  - Site selection (single)
  - Predicted variable selection (TP or SRP, depending on input data)
  - Data subset slider to choose a range of data points
  - Export button to save outputs
  - Time-series plot of discharge with subset markers
  - Whole-dataset outputs (autofit coefficients, model plots)
  - Whole-dataset custom-coefficients outputs (coefficients fixed by user)
  - Data-subset outputs (autofit and custom-coefficients) for the selected range

## Running the app: step-by-step
- Copy input CSV files into the INPUT sub-folder.
- Run RLAM_MAIN.R in R or R Studio.
- The app scans INPUT and filters to valid CSVs with required columns and non-empty data.
- On start:
  - First file (alphabetical) is loaded; if only TP or only SRP is present, only that option appears for the predicted variable.
  - Data are cleaned (removing rows with missing/negative Q or negative TP/SRP).
  - Models are fitted for the full dataset; custom coefficients default to autofit values.
- Data Subset:
  - Use the slider to select a subset; outputs for the subset automatically refresh and autofit coefficients update accordingly.
- Custom models:
  - Coefficients A, C, D can be fixed one at a time. Enter a fixed value in a field and click the corresponding Refit button.
  - Plots update in real-time while refining the fit.
- Exports:
  - Click Export Plots & Model Coefficients to create an OUTPUT folder (if needed) containing PDFs and CSVs with standardized naming.

## Outputs: reports and spreadsheets
- PDF reports (ROUTINES):
  - RLAM_REPORT_AUTOFIT_FULLDATA_[site name]_[variable name].pdf
  - RLAM_REPORT_CUSTOMFIT_FULLDATA_[site name]_[variable name].pdf
  - RLAM_REPORT_AUTOFIT_SUBSET_[start]-[end]_[site name]_[variable name].pdf
  - RLAM_REPORT_CUSTOMFIT_SUBSET_[start]-[end]_[site name]_[variable name].pdf
- CSV spreadsheets (ROUTINES):
  - RLAM_SPREADSHEET_AUTOFIT_FULLDATA_[site name]_[variable name].csv
  - RLAM_SPREADSHEET_CUSTOMFIT_FULLDATA_[site name]_[variable name].csv
  - RLAM_SPREADSHEET_AUTOFIT_SUBSET_[start]-[end]_[site name]_[variable name].csv
  - RLAM_SPREADSHEET_CUSTOMFIT_SUBSET_[start]-[end]_[site name]_[variable name].csv
- Contents:
  - Summary page: site, predicted variable, model type (autofit or custom), observations, start/end points, coefficients (A, C, D), QCP, %CSdom, hydrograph, model plots, and concentration/loads split by CS and RRS.
  - CSVs include per-date fields: Date, Q, MODELLED_CONCENTRATION_CS, MODELLED_CONCENTRATION_RRS, MODELLED_LOADS_CS, MODELLED_LOADS_RRS, MODELLED_LOADS_PER_DAY_CS, MODELLED_LOADS_PER_DAY_RRS.

## Data structure and project organization
- Top-level RLAM folder contents:
  - RLAM_MAIN.R, RLAM_Functions.R, server.R, ui.R
  - www/ (UKCEH logo)
  - INPUT/ (sample site CSVs)
- Outputs are saved to an OUTPUT sub-folder created alongside INPUT when exporting.

## Data quality and limitations
- Automated checks help ensure only well-formed CSVs with required columns are used.
- Rows with missing/negative Q or negative TP/SRP are removed to maintain data integrity.
- Provides a transparent, auditable workflow suitable for monitoring environmental phosphorus inputs over time and across sites.

## References
- Bowes M.J. et al. (2008). Modelling of phosphorus inputs to rivers from diffuse and point sources. Science of the Total Environment.
- Bowes M.J. et al. (2014). Identifying priorities for nutrient mitigation using river concentration-flow relationships: The Thames basin, UK. Journal of Hydrology.