# SusHiWat_FinalVersion.WEAP

## Overview
- A water resource systems model dataset built with WEAP for the SusHi-Wat project.
- Includes the model file SusHiWat_FinalVersion.WEAP and a Data sub-folder with meteorological inputs (11 CSVs) plus extensive WEAP-supporting files required to run the model for historical and future climate scenarios.
- Project funded by UK NERC and Indian Ministry of Earth Sciences (Newton-Bhabha Fund).
- Historical run period: June 1989 – May 2008.

## What is included
- SusHiWat_FinalVersion.WEAP: the main WEAP model file.
- Data folder contains:
  - 11 meteorological input CSV files for model inputs.
  - A large collection of WEAP-related files (examples include 79 database files, multiple DBF/FAM/GIF/JGW/JPG files, 74 PX files, 4 shapefiles, 19 X02 files, 15 X03 files, 9 X04 files, 7 X05 files, 4 X06 files, 4 X07 files, 2 X08 files, 2 X09 files, 2 X0C files, 1 X11 file, 13 XG0 files, 6 XG1 files, 1 XG2 file, 1 XG3 file, 1 XG4 file, 19 Y02 files, 15 Y03 files, 9 Y04 files, 7 Y05 files, 4 Y06 files, 4 Y07 files, 2 Y08 files, 2 Y09 files, 2 Y0C files, 1 Y11 file, 13 YG0 files, 6 YG1 files, 1 YG2 file, 1 YG3 file, 1 YG4 file, among others).
- The dataset provides a complete package to open and run the model, including necessary data and ancillary files.

## How to run the historical period (1989–2008)
- Open WEAP and go to Area > Manage Areas.
- Click Restore and select SusHi-Wat_FinalVersion.WEAP to create a new folder SusHiWat_FinalVersion in WEAP Areas.
- Switch to Results view to obtain model outputs for the historical period (June 1989 – May 2008).

## How to run future climate change scenarios
- Scenarios are constructed by combining all RCPs with all GCMs from CMIP5, using two time slices: MidCentury (2031–2050) and EndCentury (2081–2100).
- To run a specific future scenario, update inputs related to precipitation, temperature, glacier area, and initial depth as follows:

  1) Replace precipitation and temperature inputs
  - Location: SusHiWat_FinalVersion\Data\
  - Use files from Climate change scenarios CC_TimeSlice_Data:
    - pr_RCP_TimeSlice_GCM_basins.csv
    - pr_RCP_TimeSlice_GCM_command.csv
    - tas_RCP_TimeSlice_GCM_basins.csv
    - tasmax_RCP_TimeSlice_GCM_command.csv
    - tasmin_RCP_TimeSlice_GCM_command.csv
  - File naming reflects the chosen scenario (RCP, GCM, and TimeSlice).

  2) Adjust glacier area and depth
  - In WEAP, switch to Data view.
  - Navigate to Demand Sites and Catchments > Land use > Area.
  - Update glacier area for elements C04, C07, C08, C09, C10, C11, C12, C13, C14, C15, C16, C17, C18, C19, C20 using TimeSlice_GlacierProjection_CXX.csv corresponding to the selected future scenario.
  - Then select Glacier and update Initial ice depth for the same elements using the same TimeSlice_GlacierProjection_CXX.csv files.

  3) Run the model for the chosen scenario
  - In WEAP, switch to Results view to obtain outputs for the selected climate scenario.
  - Note: The dates remain anchored to the baseline, with results corresponding to 2031–2050 or 2081–2100 depending on the scenario.

## Additional notes for data governance and reuse
- File paths referenced (examples):
  - WEAP model path: …\WEAP Areas\SusHiWat_FinalVersion\Data\
  - Climate scenario data path: …\Climate change scenarios\CC_TimeSlice_Data\
- The dataset supports scenario analysis by editing input datasets and glacier projections, enabling assessment of climate change impacts on water resources within the SusHi-Wat framework.
- Ensures reproducibility by documenting exact input files and the steps to apply them for both historical and future scenarios.