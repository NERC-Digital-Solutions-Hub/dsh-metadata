# This dataset contains the project folder of a water resource systems model ('SusHiWat_FinalVersion.WEAP') built with the Water Evaluation And Planning system (WEAP, https://www.weap21.org/) including all the files required to run the model for a historical period, and additional data to run multiple future climate change scenarios (csv files)

## Overview
- WEAP-based water resource model named SusHiWat_FinalVersion.WEAP
- Includes everything needed to run the model for a historical period (June 1989 – May 2008)
- Provides additional data to run multiple future climate change scenarios (CSV files)

## Contents and structure
- WEAP project file: SusHiWat_FinalVersion.WEAP
- Data sub-folder contains:
  - Meteorological inputs for the model (11 CSV files)
  - WEAP-required files: numerous data files (examples include 79 database files, 2 DBF, 1 FAM, 1 GIF, 1 JGW, 1 JPG, 20 MB files, 2 CSV, 9 text files with NULL/INI/TXT extensions, 74 PX files)
  - Shapefiles and other supporting data (e.g., 4 shapefiles; various X02–YG4 file series)
- Running environment: WEAP software

## Running the model for the historical period
- Open WEAP and navigate to Area > Manage Areas
- Use Restore to load SusHiWat_FinalVersion.WEAP, creating a new folder SusHiWat_FinalVersion in WEAP Areas (default WEAP installation path: Documents folder)
- View results by selecting Results to obtain outputs for the period June 1989 – May 2008

## Running future climate change scenarios
- Scenarios are built by combining:
  - Representative Concentration Pathways (RCP)
  - Global Climate Models (GCM)
  - Time slices (MidCentury: 2031–2050; EndCentury: 2081–2100)
- Source for scenarios: KNMI climate explorer (CMIP5 data)
- To run a specific scenario, adjust model inputs related to precipitation, temperature, glacier area, and initial ice depth using scenario-specific files:
  - Precipitation and temperature inputs:
    - pr_RCP_TimeSlice_GCM_basins.csv
    - pr_RCP_TimeSlice_GCM_command.csv
    - tas_RCP_TimeSlice_GCM_basins.csv
    - tasmax_RCP_TimeSlice_GCM_command.csv
    - tasmin_RCP_TimeSlice_GCM_command.csv
    - Pcorrected_WEAPEBands.csv
    - Pcorrected_WEAPEBands_day.csv
    - Tcorrected_WEAPEBands.csv
    - Tmaxcorrected_WEAPEBands_day.csv
    - Tmincorrected_WEAPEBands_day.csv
  - Glacier area and depth updates:
    - TimeSlice_GlacierProjection_CXX.csv (for each C04, C07, C08, C09, C10, C11, C12, C13, C14, C15, C16, C17, C18, C19, C20)
- After updating inputs, run the model in the Results view to obtain outputs for the selected climate scenario
- Note: Baseline dates remain the same, but outputs correspond to the chosen time slice (2031–2050 or 2081–2100)

## Data location and references
- Model path: …\WEAP Areas\SusHiWat_FinalVersion
- Data inputs: …\WEAP Areas\SusHiWat_FinalVersion\Data
- Climate change scenario data: …\Climate change scenarios\CC_TimeSlice_Data
- Scenario inputs map to corresponding pr/tas files and TimeSlice_GlacierProjection_CXX.csv files for glacier adjustments

## Key points for analysts
- The dataset enables reproducible historical simulation (1989–2008) and exploration of multiple future climate scenarios via RCP/GCM/time-slice combinations
- Involves manual editing of WEAP inputs to reflect scenario-specific climate and glacier changes
- Includes a comprehensive set of WEAP-compatible data files to support running and reproducing results within WEAP
- Access and reproducibility depend on the WEAP software and correct navigation of the provided folder structure and file naming conventions