# Dissolved Oxygen concentrations from Durleigh Reservoir, 2018

## Overview
- Dataset describing dissolved oxygen measurements at Durleigh Reservoir in 2018.
- Data collected using miniDOT oxygen loggers with miniWIPER devices positioned at the bottom of the water column.
- Two locations (L2 and L3) were monitored; measurements occur every 10 minutes from 30 May 2018 to 5 October 2018.
- Data are provided as raw .txt files and require cleaning before analysis.

## Deployment and data collection
- miniDOT loggers deployed with miniWIPER units at the bottom of the water column.
- Deployers: Emily Slavin and Danielle Wain.
- Sensor data includes timestamp, UTC/GMT, battery voltage, temperature (°C), dissolved oxygen (mg/L), and dissolved oxygen saturation (%).

## Locations and sensor details
- Location 2
  - Latitude: 51.1210, Longitude: -3.0403
  - Depth: 6 m
  - Sensor: 7392-875323
  - Data file type: Concatenated Data File
  - Concatenation Date: 2018-10-05 17:43:25 BST
  - DO concentration compensated for salinity: 0.0 ppt
  - Pressure: 1013.0 mbar
- Location 3
  - Latitude: 51.1215, Longitude: -3.0445
  - Depth: 4 m
  - Sensor: 7450-701302
  - Data file type: Concatenated Data File
  - Concatenation Date: 2018-10-05 18:04:04 BST
  - DO concentration compensated for salinity: 0.0 ppt
  - Pressure: 1013.0 mbar

## Data structure and variables
- Parameters/columns included in the files:
  - Unix_Timestamp (seconds)
  - UTC_Date_&_Time
  - Greenwich_Mean_Time
  - Battery (volts)
  - Temperature (°C)
  - Dissolved_Oxygen (mg/L)
  - Dissolved_Oxygen_Saturation (% saturation)
  - Q (quality flag)

## Data quality and preprocessing notes
- The provided .txt files are raw data.
- Periods of sensor fouling occurred despite miniWIPER operation.
- Some periods had the sensor out of the water for battery replacement and cleaning (notably 13 June and 21 August 2018).
- During fouling, temperature readings may be low and dissolved oxygen may show 0% saturation.
- Consequently, cleaning and quality assurance are required prior to analysis.

## Usage and citation
- This dataset should be cited as: Slavin and Wain (2018) Slavin, E.I., Wain, D.J. 2018. Dissolved Oxygen concentrations from Durleigh Reservoir, 2018.