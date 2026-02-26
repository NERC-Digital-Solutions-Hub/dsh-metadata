# This dataset contains the project folder of a water resource systems model ('SusHiWat_FinalVersion.WEAP') built with the Water Evaluation And Planning system (WEAP, https://www.weap21.org/) including all the files required to run the model for a historical period, and additional data to run multiple future climate change scenarios (csv files). The WEAP model was built within the 'Sustaining Himalayan Water Resources in a Changing Climate' (SusHi-Wat) project (NE/N015541/1), funded by the UK Natural Environment Research Council and the Indian Ministry of Earth Sciences through the Newton-Bhabha Fund.

## What is included

- A WEAP project file: SusHiWat_FinalVersion.WEAP, which can be opened as a zipped file.
- A sub-folder named Data containing:
  - Meteorological inputs for the model (11 csv files).
  - Extensive supporting WEAP files: 79 database files; 2 DBF files; 1 FAM file; 1 GIF file; 1 JGW file; 1 JPG file; 20 MB files; 2 CSV files; 9 text files; 74 PX files; 4 shapefiles; 1 TVF file; 19 X02 files; 15 X03 files; 9 X04 files; 7 X05 files; 4 X06 files; 4 X07 files; 2 X08 files; 2 X09 files; 2 X0C files; 1 X11 file; 13 XG0 files; 6 XG1 files; 1 XG2 file; 1 XG3 file; 1 XG4 file; 19 Y02 files; 15 Y03 files; 9 Y04 files; 7 Y05 files; 4 Y06 files; 4 Y07 files; 2 Y08 files; 2 Y09 files; 2 Y0C files; 1 Y11 file; 13 YG0 files; 6 YG1 files; 1 YG2 file; 1 YG3 file; 1 YG4 file.
- Historical run instructions and date range:
  - Historical period results: June 1989 – May 2008.
- Future climate change scenario inputs:
  - Scenarios defined by combinations of RCPs, GCMs (CMIP5), and time slices (MidCentury 2031-2050; EndCentury 2081-2100).
  - Data sources for scenarios: KNMI Climate Explorer (https://climexp.knmi.nl/selectfield_cmip5.cgi?id=someone@somewhere).

## How to run the historical period

- Open WEAP and in the main menu go to Area > Manage Areas.
- Click Restore and select SusHiWat_FinalVersion.WEAP to create a new folder SusHiWat_FinalVersion in WEAP Areas (default location: WEAP Areas folder under Documents).
- Switch to Results view to obtain results for the historical period (June 1989 – May 2008).

## How to run future climate change scenarios

- Define scenario inputs by replacing precipitation and temperature inputs with scenario-specific data:
  - Path and file mappings depend on the scenario name and are sourced from the Climate change scenarios folder.
  - Key input files:
    - Pcorrected_WEAPEBands.csv, pr_RCP_TimeSlice_GCM_basins.csv
    - pr_RCP_TimeSlice_GCM_command.csv
    - tas_RCP_TimeSlice_GCM_basins.csv
    - tasmax_RCP_TimeSlice_GCM_command.csv
    - tasmin_RCP_TimeSlice_GCM_command.csv
  - File paths to WEAP model inputs: …\WEAP Areas\SusHiWat_FinalVersion\Data\ and …\Climate change scenarios\CC_TimeSlice_Data\.
- Adjust glacier area and initial depth for multiple glacier elements:
  - In WEAP, switch to Data view, then Demand Sites and Catchments > Land use > Area.
  - Modify glacier areas for elements C04, C07, C08, C09, C10, C11, C12, C13, C14, C15, C16, C17, C18, C19, C20 using TimeSlice_GlacierProjection_CXX.csv files for the chosen scenario.
  - Switch to Glacier and adjust Initial ice depth for the same elements using the corresponding TimeSlice_GlacierProjection_CXX.csv files.
- Run the model in Results view to obtain scenario-specific results:
  - Note: The calendar dates do not shift from baseline, but outputs correspond to 2031-2050 (MidCentury) or 2081-2100 (EndCentury).

## Data sources and reproducibility

- Climate scenarios are drawn from CMIP5 data accessed via KNMI Climate Explorer.
- The dataset provides a reproducible workflow to generate historical and future scenario results by substituting meteorological inputs and glacier parameters, enabling comparative analyses across multiple climate futures.

## How this supports data use and reuse

- Provides a complete, self-contained data package to run WEAP-based hydrological scenarios, including raw inputs, configuration guidance, and step-by-step modification procedures.
- Enables end users to self-serve scenario analyses by swapping inputs and updating glacier projections, supporting policy and planning discussions with transparent data provenance.