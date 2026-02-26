# SusHiWat_FinalVersion.WEAP

- Overview
  - A water resource systems model built in WEAP (Water Evaluation And Planning system) for the Himalayan region, as part of the Sustaining Himalayan Water Resources in a Changing Climate (SusHi-Wat) project (NE/N015541/1).
  - Funded by UK NERC and the Indian Ministry of Earth Sciences through the Newton-Bhabha Fund.
  - Includes all files required to run the model for a historical period and to explore multiple future climate change scenarios.
  - Historical period outputs cover June 1989 to May 2008.
  - Future scenarios are based on CMIP5 RCPs and GCMs, with time slices MidCentury (2031-2050) and EndCentury (2081-2100).

- Contents and structure
  - The dataset is a WEAP project folder SusHiWat_FinalVersion.WEAP, which can be opened as a zipped file.
  - Contains a sub-folder named Data with:
    - 11 meteorological input CSV files (for model inputs).
    - A large set of WEAP support data files: 79 database files, 2 DBF files, 1 FAM file, 1 GIF file, 1 JGW file, 1 JPG file, many large files (e.g., 20 MB), multiple CSV, TXT, INI, and NULL files.
    - 74 PX files, 4 shapefiles, 1 TVF file, 19 X02 files, 15 X03 files, 9 X04 files, 7 X05 files, 4 X06 files, 4 X07 files, 2 X08 files, 2 X09 files, 2 X0C files, 1 X11 file, 13 XG0 files, 6 XG1 files, 1 XG2 file, 1 XG3 file, 1 XG4 file, 19 Y02 files, 15 Y03 files, 9 Y04 files, 7 Y05 files, 4 Y06 files, 4 Y07 files, 2 Y08 files, 2 Y09 files, 2 Y0C files, 1 Y11 file, 13 YG0 files, 6 YG1 files, 1 YG2 file, 1 YG3 file, 1 YG4 file.
  - The dataset includes explicit instructions to run the model for historical and future scenarios.

- How to run for the historical period (June 1989 – May 2008)
  - Open WEAP and go to Area > Manage Areas.
  - Use Restore to browse for SusHi-Wat_FinalVersion.WEAP; this creates a new folder SusHiWat_FinalVersion in WEAP Areas > WEAP Areas folder (default location is WEAP installation’s Documents folder).
  - In Results view, review model outputs for the historical period (1989-2008).

- How to run future climate change scenarios
  - Scenarios combine all RCPs with all CMIP5 GCMs available on the KNMI Climate Explorer.
  - Time slices: MidCentury (2031-2050) and EndCentury (2081-2100).
  - To run a specific scenario, modify the WEAP inputs related to precipitation, temperature, glacier area, and initial depth:
    - Replace precipitation and temperature inputs:
      - Use files from Climate Change Scenarios/Data:
        - Pcorrected_WEAPEBands.csv
        - Pcorrected_WEAPEBands_day.csv
        - Tcorrected_WEAPEBands.csv
        - Tmaxcorrected_WEAPEBands_day.csv
        - Tmincorrected_WEAPEBands_day.csv
      - Corresponding target files follow the naming pattern: pr_RCP_TimeSlice_GCM_basins.csv, pr_RCP_TimeSlice_GCM_command.csv, tas_RCP_TimeSlice_GCM_basins.csv, tasmax_RCP_TimeSlice_GCM_command.csv, tasmin_RCP_TimeSlice_GCM_command.csv.
    - Adjust glacier area and depth:
      - In WEAP, Data view > Demand Sites and Catchments > Land use > Area.
      - Change glacier area for elements C04, C07, C08, C09, C10, C11, C12, C13, C14, C15, C16, C17, C18, C19, C20 using TimeSlice_GlacierProjection_CXX.csv for the specific scenario.
      - In Glacier > Initial ice depth, adjust depths for the same elements using TimeSlice_GlacierProjection_CXX.csv.
  - Run the model in Results view to obtain outputs for the chosen climate scenario.
  - Note: The model dates remain the same as the baseline, but outputs correspond to 2031-2050 or 2081-2100 depending on the scenario.

- Access and usage notes
  - Path reference for the WEAP model: …\WEAP Areas\SusHiWat_FinalVersion\Data\ (and accompanying Climate Change Scenarios folders).
  - The dataset provides a reproducible workflow to assess how climate change may affect Himalayan water resources, including data inputs, scenario customization, and resulting outputs.