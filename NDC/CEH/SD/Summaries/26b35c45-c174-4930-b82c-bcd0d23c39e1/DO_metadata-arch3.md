# Dissolved Oxygen concentrations from Durleigh Reservoir, 2018

- Dataset context
  - Dissolved Oxygen (DO) concentrations measured at Durleigh Reservoir in 2018 using miniDOT oxygen loggers with miniWIPER positioned at the bottom of the water column.
  - Two locations (L2 and L3) are provided, with separate data files for each location.
  - Deployment period: 30 May 2018 to 05 Oct 2018.
  - Measurements taken every 10 minutes.

- Location and sensors
  - Location 2 (L2): Lat 51.1210, Lon -3.0403, depth 6 m; Sensor: 7392-875323.
  - Location 3 (L3): Lat 51.1215, Lon -3.0445, depth 4 m; Sensor: 7450-701302.
  - Concatenated data files labeled per location with concatenation dates: 2018Oct05 17:43:25 BST (L2) and 2018Oct05 18:04:04 BST (L3).

- Data fields and format
  - Parameters included in the raw text files: Unix_Timestamp (s), UTC_Date_&_Time, Greenwich_Mean_Time, Battery (V), Temperature (°C), Dissolved_Oxygen (mg/L), Dissolved_Oxygen_Saturation (% saturation), Q (quality flag).

- Data quality and conditioning
  - The data are raw and require cleaning prior to analysis.
  - Noted sensor fouling periods and times when sensors were out of the water for battery replacement and cleaning (13 June and 21 August 2018), which may result in periods of low or zero DO saturation.
  - DO concentration is reported with salinity compensation at 0.0 ppt; saturation values are computed at standard pressure (1013.0 mbar).
  - Data gaps and potential inaccuracies may arise from fouling, downtime, and temperature effects on measurements.

- Usage notes and citation
  - Data should be cleaned and quality-checked before use in analyses.
  - Please cite the dataset as Slavin and Wain (2018): Slavin, E.I., Wain, D.J. 2018. Dissolved Oxygen concentrations from Durleigh Reservoir, 2018.