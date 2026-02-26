# Dissolved Oxygen concentrations from Durleigh Reservoir, 2018

## Overview
- Dissolved oxygen concentrations measured at Durleigh Reservoir in 2018 using miniDOT loggers with miniWIPER units placed at the bottom of the water column.
- Deployments occurred at two locations between 30/05/2018 and 05/10/2018.
- Measurements were recorded every 10 minutes.
- Data are provided as raw .txt files and include two location-specific data files labeled L2 and L3.
- Measurements were collected by Emily Slavin and Danielle Wain.

## Locations and deployment details
- Location 2
  - Latitude: 51.1210, Longitude: -3.0403
  - Depth: 6 m
  - MiniDOT Logger: Sensor 7392-875323
- Location 3
  - Latitude: 51.1215, Longitude: -3.0445
  - Depth: 4 m
  - MiniDOT Logger: Sensor 7450-701302
- Data are delivered as “Concatenated Data File” for each location with a concatenation date of 2018-Oct-05 17:43:25 BST (Location 2) and 2018-Oct-05 18:04:04 BST (Location 3).

## Data fields and formatting
- Parameters included in the raw data:
  - Unix_Timestamp (seconds)
  - UTC_Date_&_Time
  - Greenwich_Mean_Time
  - Battery (volts)
  - Temperature (°C)
  - Dissolved_Oxygen (mg/L)
  - Dissolved_Oxygen_Saturation (% saturation)
  - Q (quality flag)
- DO concentration is reported as not adjusted for salinity (salinity compensation value shown as 0.0 ppt).
- Saturation calculated at a reference pressure of 1013.0 mbar.

## Data quality and cleaning notes
- The files are raw data and require cleaning before analysis.
- There were periods when sensors were fouled despite miniWIPER operation.
- Some intervals when the sensor was out of the water for battery replacement and cleaning (noted on 13 June and 21 August 2018).
- During fouling, temperatures may be low and DO may appear at 0% saturation.
- These issues indicate the need to identify and address fouling/out-of-water periods prior to any analysis.

## Usage and citation
- Data should be cited as: Slavin, E.I., Wain, D.J. 2018. Dissolved Oxygen concentrations from Durleigh Reservoir, 2018.

## Access and format summary
- Data provided as two raw .txt files (one per location: L2 and L3).
- Each file is a concatenated data record with the listed fields and sensor metadata.