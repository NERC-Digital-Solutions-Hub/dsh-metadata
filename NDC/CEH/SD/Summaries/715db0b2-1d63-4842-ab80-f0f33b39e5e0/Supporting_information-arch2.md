# SusHiWat_FinalVersion.WEAP

## Overview
- A dataset containing the project folder of a water resource systems model built with WEAP (Water Evaluation And Planning system), named SusHiWat_FinalVersion.WEAP.
- Designed to run the model for a historical period and to support multiple future climate change scenarios (CSV inputs).
- Part of the SusHi-Wat project (NE/N015541/1), funded by UK NERC and the Indian Ministry of Earth Sciences via the Newton-Bhabha Fund.

## What is included
- WEAP project folder SusHiWat_FinalVersion.WEAP, which can be opened as a zipped file and contains:
  - A sub-folder named Data with meteorological inputs (11 CSV files) and many files required by WEAP (including various databases, shapefiles, images, text/config files, and several other file types in large quantities).
- Historical run data:
  - Running instructions yield results for the period June 1989 – May 2008.
- Future climate change scenarios:
  - Scenarios are created by combining all RCPs with all GCMs available in CMIP5 (via KNMI Climate Explorer).
  - Time slices available: MidCentury (2031-2050) and EndCentury (2081-2100).

## How to run the historical period
- Open WEAP and go to Area > Manage Areas.
- Click Restore and select SusHi-Wat_FinalVersion.WEAP; this creates a folder SusHiWat_FinalVersion in WEAP Areas.
- In Results view, access outputs for the historical period (1989-2008).

## How to run future climate change scenarios
- Scenarios require updating inputs to reflect a chosen RCP, GCM, and Time Slice:
  - Precipitation and temperature inputs:
    - Files to replace depend on scenario; path pattern is …\WEAP Areas\SusHiWat_FinalVersion\Data\ and related climate-change data folders.
    - Use content from climate-change data files, e.g. pr_RCP_TimeSlice_GCM_basins.csv, pr_RCP_TimeSlice_GCM_command.csv, tas_RCP_TimeSlice_GCM_basins.csv, tasmax_RCP_TimeSlice_GCM_command.csv, tasmin_RCP_TimeSlice_GCM_command.csv, etc.
  - Glacier area and depth adjustments:
    - In WEAP, go to Data view > Demand Sites and Catchments > Land use > Area.
    - Update glacier area and related elevation bands for elements C04, C07, C08, C09, C10, C11, C12, C13, C14, C15, C16, C17, C18, C19, C20 as provided in TimeSlice_GlacierProjection_CXX.csv for the chosen scenario.
    - Then select Glacier and Initial ice depth and adjust depths for the same elements using the corresponding TimeSlice_GlacierProjection_CXX.csv.
- Running the scenario:
  - After updating inputs, run via Results view to obtain outputs for the selected climate scenario.
  - Note: The baseline dates stay the same, but results correspond to 2031-2050 (MidCentury) or 2081-2100 (EndCentury).

## Data organization and access
- Path references indicate the main model files live under the WEAP Areas folder, with Data containing meteorological inputs and other required WEAP files.
- The dataset includes a broad set of supporting files (XML/INI-like, shapefiles, image files, CSVs, and WEAP-specific data files) necessary to operate the model and produce outputs.

## Key notes for analysts
- The dataset supports reproducible historical and future climate impact analysis for Himalayan water resources.
- Future scenario setup requires careful replacement of input files and glacier parametric adjustments to reflect the chosen RCP, GCM, and time slice.
- Outputs will reflect the selected climate scenario's period (either 2031-2050 or 2081-2100) while preserving the baseline date structure.