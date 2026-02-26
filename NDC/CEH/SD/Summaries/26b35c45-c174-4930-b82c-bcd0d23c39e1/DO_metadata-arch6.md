# Dissolved Oxygen concentrations from Durleigh Reservoir, 2018

## Overview
- Time-series dataset of dissolved oxygen (DO) measurements from two locations in Durleigh Reservoir during 2018.
- Purpose: provide raw sensor data for analysis of DO conditions and help support water quality assessment.

## Data Files and Structure
- Two data files (concatenated data files) corresponding to two locations:
  - Location 2 (Lat 51.1210, Lon -3.0403; depth 6 m)
    - Sensor: 7392-875323
  - Location 3 (Lat 51.1215, Lon -3.0445; depth 4 m)
    - Sensor: 7450-701302
- Timeframe: 30 May 2018 to 5 Oct 2018
- Sampling: every 10 minutes
- File metadata:
  - Unix_Timestamp (seconds)
  - UTC_Date_&_Time
  - Greenwich_Mean_Time
  - Battery (volt)
  - Temperature (deg C)
  - Dissolved_Oxygen (mg/L)
  - Dissolved_Oxygen_Saturation (% saturation)
  - Q (quality flag)
- Additional notes: temperatures, DO saturation values, and locations provided; raw data, with periods of potential fouling or sensor removal.

## Collection Details
- Method: miniDOT oxygen loggers with miniWIPER devices positioned at the bottom of the water column.
- Deployment period: 30/05/2018 – 05/10/2018.
- Field personnel: Emily Slavin and Danielle Wain.
- Data format: .txt files; datasets are raw and require cleaning prior to analysis.

## Data Quality and Cleaning Needs
- Periods when sensors were fouled or out of the water (e.g., battery replacement/cleaning) lead to unreliable data.
- DO saturation can reach 0% during fouling or very low temperatures; these periods require identification and removal or correction.
- Data should be cleaned and validated before analysis to ensure accuracy and comparability between locations.

## Using the Data
- Recommended workflow:
  - Load both location datasets and align by UTC_Date_&_Time.
  - Identify and remove fouled-out periods using the Q flag and sensor status indicators; consider cross-checking temperatures and DO values for anomalies.
  - Merge Location 2 and Location 3 into a combined time-series for comparative analyses.
  - Convert DO from mg/L and DO Saturation (%) as needed; verify salinity compensation (listed as 0.0 ppt) and pressure reference (1013.0 mbar).
  - Produce cleaned time-series dashboards or pivoted views to explore temporal patterns, diurnal cycles, and site comparisons.
- Potential analyses:
  - DO concentration trends over time at each location.
  - Comparison of DO saturation between locations.
  - Correlation of DO with temperature and battery levels (as data quality indicators).
- Outputs could support broader data-use goals, including dashboards for stakeholders and reports highlighting DO dynamics.

## Provenance and Citation
- Dataset cited as: Slavin and Wain (2018) Slavin, E.I., Wain, D.J. 2018. Dissolved Oxygen concentrations from Durleigh Reservoir, 2018.