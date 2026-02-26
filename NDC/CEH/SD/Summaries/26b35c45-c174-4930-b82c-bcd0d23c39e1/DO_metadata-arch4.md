# Dissolved Oxygen concentrations from Durleigh Reservoir, 2018

## Dataset scope
- Provides dissolved oxygen (DO) concentrations at Durleigh Reservoir during 2018.
- Two data files correspond to locations L2 and L3, with miniDOT oxygen loggers positioned at the bottom of the water column.
- Deployment period: 30 May 2018 to 5 October 2018.
- Measurements were taken every 10 minutes.
- Data are raw and require cleaning prior to analysis.

## Data collection details
- Location 2 (L2)
  - Lat 51.1210, Lon -3.0403, depth 6 m
  - MiniDOT Logger: Concatenated Data File
  - Sensor: 7392-875323
  - Concatenation Date: 2018-10-05 17:43:25 BST
- Location 3 (L3)
  - Lat 51.1215, Lon -3.0445, depth 4 m
  - MiniDOT Logger: Concatenated Data File
  - Sensor: 7450-701302
  - Concatenation Date: 2018-10-05 18:04:04 BST
- Parameters included in the files: Unix_Timestamp (s), UTC_Date_&_Time, Greenwich_Mean_Time, Battery (V), Temperature (°C), Dissolved_Oxygen (mg/L), Dissolved_Oxygen_Saturation (%), Q
- DO saturation calculated at 1013.0 mbar; DO concentration is reported as compensated for salinity (0.0 ppt)

## Data quality and issues
- Some periods of sensor fouling despite miniWIPER operation
- Periods when sensors were out of the water for battery replacement and cleaning (notably 13 June and 21 August 2018)
- During fouling, temperatures may be low and DO may appear as 0% saturation
- Consequently, the .txt files require cleaning prior to any analysis

## Data structure and format
- Two location-specific .txt data files (L2 and L3), labeled accordingly
- Columns/fields as listed above
- Location coordinates and depths provided for context and spatial interpretation

## Provenance and citation
- Collected by Emily Slavin and Danielle Wain
- Please cite: Slavin and Wain (2018) Slavin, E.I., Wain, D.J. 2018. Dissolved Oxygen concentrations from Durleigh Reservoir, 2018.