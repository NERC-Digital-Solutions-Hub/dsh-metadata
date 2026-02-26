# Lynx_Camera_Details

## Overview
- Dataset of Lynx camera trap deployments across projects (NatEnvPr, REDFIRE, TREE).
- Contains per-camera metadata: identifiers, spatial data, deployment timing, imagery/video counts, site context, and environmental measurements.
- Some fields may be missing or recorded inconsistently; date/time may have been corrected to Eastern European Winter Time (GMT+03:00) if needed.

## Key Fields and Explanations

- Project and location identifiers
  - Project_ID: ID of the project the images were collected as part of (NatEnvPr, REDFIRE, TREE)
  - Camera_Trap_Location_ID: Numerical ID of the camera trap location
  - Camera_Trap_Location_ID_Related_To_Project: Numerical ID of the camera location related to the project
  - Study_Site: Study site (1 to 8)
  - Year: Year when the camera was deployed (YYYY)

- Spatial data and site geometry
  - Camera_Trap_Location_Latitude_WGS84: Latitude (decimal degrees), GPS (WGS84); accurate to ~8 m
  - Camera_Trap_Location_Longitude_WGS84: Longitude (decimal degrees), GPS (WGS84); accurate to ~8 m
  - Height_Of_Camera_Deployment_m: Height of camera deployment above ground (m)
  - Distance_To_Nearest_Trail_m: Distance to the main activity location (m)
  - Orientation_Of_Camera: Orientation of the camera (N, S, E, W, and in-between)
  - Tilt_Of_Camera: Tilt of the camera

- Deployment and usage metrics
  - Duration_Of_Camera_Deployment: Duration of deployment (days)
  - Total_number_Of_Still_Images_Take n_By_Camera: Total still images taken by the camera during a setup (only Lynx images included)
  - Total_Number_Of_Videos_Taken_By _Camera: Total video clips obtained during a setup (only Lynx videos included)

- Camera identification and model
  - Make_Model_Of_Camera: Make and model of the camera
  - Camera_ID: Serial number of the camera (last four digits often shown on image information bar)

- Temporal data and time settings
  - Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time: Date and time camera was deployed (Eastern European Winter Time, GMT+03:00); corrections applied if camera times were set incorrectly
  - Date_And_Time_Of_Last_Day_Of_C amera_Opperation_European_Wint er_Time: Last date and time the camera was operating (Eastern European Winter Time)
  - Comments_Relating_To_Date_And_ Time_Settings: Notes about camera date/time settings; discrepancies between EXIF vs actual times; reasons include wrong camera settings or technical issues

- Environmental measurement
  - Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour: Ambient dose rate at a height of 1 m above soil at the camera site; measured during deployment year; not all measurements recorded

- Miscellaneous and notes
  - n/a not applicable; some fields indicate unspecified units
  - Some camera locations were shared across TREE and NATECO projects (e.g., P0012, P0028, P0042, P0104, P0108)

## Data Quality and Handling Notes

- Time consistency: date/time may have been corrected to GMT+03:00 (Eastern European Winter Time) if originally set to another time zone or DST.
- EXIF vs actual times: discrepancies may arise due to incorrect camera settings, camera behavior, or software issues; comments explain reasons.
- Missing data: several fields may be not recorded (n/r) or not available; ambient dose rates are not uniformly captured.
- Cross-project relationships: some camera locations appear in multiple projects, requiring careful joining when integrating datasets.