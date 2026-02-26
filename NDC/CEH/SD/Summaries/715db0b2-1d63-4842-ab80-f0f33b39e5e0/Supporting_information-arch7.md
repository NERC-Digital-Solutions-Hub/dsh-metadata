# This dataset contains the project folder of a water resource systems model ('SusHiWat_FinalVersion.WEAP') built with the Water Evaluation And Planning system (WEAP, https://www.weap21.org/) including all the files required to run the model for a historical period, and additional data to run multiple future climate change scenarios (csv files).

## Overview
- Purpose: A WEAP-based water resource model (SusHiWat) designed to simulate historical and future climate scenarios for Himalayan water resources.
- Historical period results: June 1989 – May 2008.
- Future climate scenarios: Combinations of RCPs, GCMs, and time slices (MidCentury 2031–2050; EndCentury 2081–2100).
- Audience fit: Enables GIS-based visualization and exploration of spatial water-resource impacts under climate change.

## What is included
- SusHiWat_FinalVersion.WEAP: The main WEAP project file.
- Data sub-folder: Contains 11 meteorological input CSV files and numerous supporting WEAP files (e.g., 79 database files, various DBF, FAM, GIF, JGW, JPG, TXT-related files, shapefiles, PX, X02–XYG0 series, Y02–YG4 series, etc.).
- Climate-change inputs: Files intended to drive future scenarios, organized by scenario (RCP, GCM, Time Slice) and glacier-related data files.
- TimeSlice data: TimeSlice_GlacierProjection_CXX.csv for glacier area and initial depth adjustments per scenario.
- Import/export guidance files: Pcorrected_WEAPEBands.csv, pr_RCP_TimeSlice_GCM_basins.csv, pr_RCP_TimeSlice_GCM_command.csv, tas_RCP_TimeSlice_GCM_basins.csv, tasmax_RCP_TimeSlice_GCM_command.csv, tasmin_RCP_TimeSlice_GCM_command.csv, etc.
- Historical data inputs: Meteorological inputs and model parameters for the baseline period.

## How to run for the historical period
- Open WEAP and go to Area > Manage Areas.
- Click Restore and select SusHiWat_FinalVersion.WEAP to create a new folder SusHiWat_FinalVersion in WEAP Areas (default WEAP installation path in Documents).
- Switch to Results view to obtain model outputs for the historical period (June 1989 – May 2008).

## How to run future climate change scenarios
- Scenario selection: Combine RCP + GCM + Time Slice using KNMI Climate Explorer to identify the desired scenario (e.g., MidCentury or EndCentury).
- Input updates for a chosen scenario:
  - Replace precipitation and temperature inputs with scenario-specific files:
    - Pcorrected_WEAPEBands.csv uses pr_RCP_TimeSlice_GCM_basins.csv
    - Pcorrected_WEAPEBands_day.csv uses pr_RCP_TimeSlice_GCM_command.csv
    - Tcorrected_WEAPEBands.csv uses tas_RCP_TimeSlice_GCM_basins.csv
    - Tmaxcorrected_WEAPEBands_day uses tasmax_RCP_TimeSlice_GCM_command.csv
    - Tmincorrected_WEAPEBands_day uses tasmin_RCP_TimeSlice_GCM_command.csv
  - File path: SusHiWat_FinalVersion\Data\ (replace with the corresponding Climate change scenarios\Data files).
- Glacier area and depth adjustments:
  - In WEAP, switch to Data view > Demand Sites and Catchments > Land use > Area.
  - Modify glacier areas for elements C04, C07, C08, C09, C10, C11, C12, C13, C14, C15, C16, C17, C18, C19, C20 using TimeSlice_GlacierProjection_CXX.csv.
  - Switch to Glacier > Initial ice depth and adjust depths for the same elements using the corresponding TimeSlice_GlacierProjection_CXX.csv.
- Run results:
  - Use Results view to generate outputs for the selected climate-change scenario.
  - Note: The temporal frame in WEAP remains baseline dates, but results correspond to 2031–2050 or 2081–2100 depending on the scenario.

## Data organization and file types
- WEAP project and data: SusHiWat_FinalVersion.WEAP and a Data folder with meteorological inputs (11 CSVs) and many support files for WEAP (including databases, shapefiles, and various configuration and data files).
- Climate-change scenario data: Scenario-specific CSVs and glacier projection files used to modify inputs for future runs.
- Structure is designed to support GIS-based analysis and map-driven presentation of water-resource dynamics under multiple climate scenarios.