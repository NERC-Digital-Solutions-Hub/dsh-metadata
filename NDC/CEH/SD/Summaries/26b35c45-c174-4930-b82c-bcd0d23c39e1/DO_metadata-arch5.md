# Dissolved Oxygen concentrations from Durleigh Reservoir, 2018

## Overview
- Metadata file for the dataset of dissolved oxygen (DO) concentrations from Durleigh Reservoir in 2018.
- Two data files correspond to different locations (L2 and L3) labeled accordingly.
- Measurements collected with miniDOT oxygen loggers (PME) equipped with miniWIPERs at the bottom of the water column at two locations from 30/05/2018 to 05/10/2018.
- Readings every 10 minutes.
- Data provided as raw .txt files; not yet cleaned for analysis.

## Location and sensor details
- Location 2:
  - Latitude 51.1210, Longitude -3.0403
  - Depth: 6 m
  - MiniDOT Sensor: 7392-875323
  - Concatenation Date: 2018-10-05 17:43:25 BST
- Location 3:
  - Latitude 51.1215, Longitude -3.0445
  - Depth: 4 m
  - MiniDOT Sensor: 7450-701302
  - Concatenation Date: 2018-10-05 18:04:04 BST
- Common data fields (per file): Unix_Timestamp (s), UTC_Date_&_Time, Greenwich_Mean_Time, Battery (V), Temperature (°C), Dissolved_Oxygen (mg/L), Dissolved_Oxygen_Saturation (%), Q
- DO concentration notes: DO concentration compensated for salinity 0.0 ppt; saturation computed at pressure 1013.0 mbar

## Data contents and format
- Raw data provided in two .txt files (one per location).
- Includes sensor readings with timestamps, environmental variables, and a quality flag (Q).

## Data quality, limitations, and caveats
- Some periods where sensors were fouled despite miniWIPER operation.
- Periods when sensors were out of the water for battery replacement and cleaning (notably 13 June and 21 August 2018).
- Temperature readings may be low during certain periods; DO can drop to 0% saturation when fouled.
- Prior to analysis, the .txt files require cleaning to address these issues.

## Provenance and citation
- Collected by Emily Slavin and Danielle Wain.
- Dataset should be cited as: Slavin and Wain (2018) Dissolved Oxygen concentrations from Durleigh Reservoir, 2018.

## Metadata and governance notes for data stewards
- Consider providing a cleaned/processed DO dataset alongside raw files.
- Ensure metadata documents: dataset title, authors, collection period, locations, coordinates, depths, sensor IDs, units, and data quality caveats.
- Document cleaning procedures for fouled/out-of-water periods and any data flagging.
- Clarify access, licensing, storage location, and versioning to support discoverability and reuse.