# R implementation of the Load Apportionment Model (RLAM) determining relative quantities of phosphorus entering rivers

## Purpose and scope
- Implements the Load Apportionment Model (LAM) to quantify relative phosphorus contributions entering rivers from constant sources (CS) and rain-related sources (RRS).
- Replaces a limited Excel version with an R-based suite and a user-friendly Shiny front-end for non-specialists.
- Enables batch processing, reuse by specialists, and systematic data governance for multiple sites.

## Model overview
- LAM concept: phosphorus entering rivers from CS and RRS affects concentration with distinct flow relationships.
  - CS: concentrations decrease with river flow (dilution).
  - RRS: concentrations increase with river flow.
- Core equation (modified): [P] = A Q^(-1) + C Q^(D-1) to separate CS and RRS contributions.
- Required inputs: dataset of discharge (Q) and phosphorus concentration ([P]) either as TP or SRP.
- Outputs: coefficients A, C, D (fitted), phosphorus concentrations/loads from CS and RRS, and diagnostic metrics.
- Provides both full-dataset autofit and subset-based analyses; supports user-defined coefficient constraints (custom fits).

## Data inputs and quality checks
- One CSV per site; file name used as site identifier.
- Required columns: Date (dd/mm/yyyy) and Q (m3/s); TP and/or SRP optional.
- Automated data screening:
  - Excludes files missing required columns or containing empty columns.
  - Removes rows with missing/negative Q or negative TP/SRP.
- Input columns and example format are defined; the app supports batch loading for multiple sites.

## File formats, structure, and installation
- File formats: R scripts, CSV, JPEG (plots).
- Main RLAM folder should contain:
  - RLAM_MAIN.R (launch script)
  - RLAM_Functions.R (core RLAM functions)
  - server.R, ui.R (Shiny app components)
  - www/UKCEH-Logo_Long_Positive_RGB.JPG
  - INPUT/ (site CSV files; examples provided)
- System requirements:
  - R (4.4.x; tested with 4.4.0/4.4.1) and Shiny 1.9.1; ggplot2
  - Windows recommended; optionally RStudio
- Installation steps:
  - Install R (and optionally RStudio)
  - Install Shiny and ggplot2 packages
  - Run RLAM_MAIN.R to launch the web interface

## User interface and workflow
- Site selection: choose which site to analyse (from available INPUT CSVs with valid data).
- Predicted variable: choose TP or SRP depending on data availability.
- Data subset slider: define a subset of the data; the UI highlights the selected range on the discharge plot.
- Model views:
  - Whole Dataset autofit: coefficients A, C, D; Q cross-over point; percentage of observations CS-dominated; plots of modeled vs observed P and CS/RRS splits.
  - Whole Dataset custom coefficients: fix one coefficient (A, C, or D) and re-fit with others free; provides immediate plots for quick assessment.
  - Data Subset autofit: same outputs as full dataset but limited to the selected data range; coefficients reset to autofit for the subset.
  - Data Subset custom coefficients: same as full dataset but restricted to subset data.
- Interaction details:
  - Custom coefficient changes update plots instantly; actual re-fit requires hitting the corresponding button.
  - Models are re-fitted automatically when the data subset changes.
- Exports:
  - Exports PDFs and CSVs to an OUTPUT folder (created if absent) with standardized naming:
    - Whole dataset autofit: RLAM_REPORT_AUTOFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_FULLDATA_[site]_[variable].csv
    - Whole dataset custom fit: RLAM_REPORT_CUSTOMFIT_FULLDATA_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_FULLDATA_[site]_[variable].csv
    - Data subset autofit: RLAM_REPORT_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_AUTOFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
    - Data subset custom fit: RLAM_REPORT_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].pdf and RLAM_SPREADSHEET_CUSTOMFIT_SUBSET_[start]_TO_[end]_[site]_[variable].csv
  - Each PDF includes a summary page (site, variable, fitting type, observations, coefficients, QCP, CS-dominance percentage) plus hydrograph and model plots.
  - CSVs contain per-date rows with Q, modeled CS and RRS concentrations, modeled loads, and loads per day for CS and RRS.

## Outputs and data products
- PDFs:
  - Summary reports for autofit and custom fits (full dataset and data subset).
  - Plots: hydrograph, modelled CS vs. RRS contributions, and fit diagnostics.
- CSVs:
  - Time series with explicit modeling outputs:
    - Date, Q
    - MODELLED_CONCENTRATION_CS, MODELLED_CONCENTRATION_RRS (μg/L)
    - MODELLED_LOADS_CS, MODELLED_LOADS_RRS (mg/s)
    - MODELLED_LOADS_PER_DAY_CS, MODELLED_LOADS_PER_DAY_RRS (t/d)
- Purpose of outputs: enable auditability, reproducibility, and integration with broader data governance processes for nutrient loading studies.

## Reproducibility and governance considerations
- Automated data validation and subset analysis support consistent, auditable analyses across multiple sites.
- Clear documentation of model parameters and fit types (autofit vs. custom) enhances traceability.
- Batch-ready structure supports governance needs for large datasets and standardized reporting.

## References
- Bowes M.J., et al. (2008). Modelling of phosphorus inputs to rivers from diffuse and point sources. Science of the Total Environment.
- Bowes M.J., et al. (2014). Identifying priorities for nutrient mitigation using river concentration-flow relationships: The Thames basin, UK. Journal of Hydrology.