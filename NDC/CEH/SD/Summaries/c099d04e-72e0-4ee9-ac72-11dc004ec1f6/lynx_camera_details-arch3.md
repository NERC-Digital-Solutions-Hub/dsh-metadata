# Lynx_Camera_Details

## Summary
- A dataset detailing camera trap deployments used to study Lynx across projects (NatEnvPr Ukrainian national program of environmental studies, REDFIRE, TREE).
- Captures where cameras were placed, when they operated, camera specifications, deployment duration, and counts of Lynx-related still images and videos.
- Includes geospatial coordinates, site descriptions, and basic ambient radiation measurements where available.
- Notes emphasize data time corrections, EXIF discrepancies, and that only Lynx-containing media are included.

## Data structure and key fields
- Project and location identifiers
  - Project_ID; Camera_Trap_Location_ID; Camera_Trap_Location_ID_Related_To_Project; Study_Site; Year; Setup
- Temporal details
  - Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time; Date_And_Time_Of_Last_Day_Of_Camera_Operation_European_Winter_Time; Comments_Relating_To_Date_And_Time_Settings
- Spatial and site context
  - Camera_Trap_Location_Latitude_WGS84; Camera_Trap_Location_Longitude_WGS84; Height_Of_Camera_Deployment_m; Distance_To_Nearest_Trail_m; Orientation_Of_Camera; Tilt_Of_Camera; Generic_Site_Description
- Camera and deployment specifics
  - Make_Model_Of_Camera; Camera_ID; Duration_Of_Camera_Deployment; Total_number_Of_Still_Images_Taken_By_Camera; Total_Number_Of_Videos_Taken_By_Camera
- Data content and scope
  - Notes that only images containing Lynx are included
- Environmental measurements
  - Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour (measured at ~1 m above ground); n/r when not recorded
- Data quality indicators
  - n/a (not applicable) and n/r (not recorded) used for missing or inapplicable fields

## Temporal and geospatial details
- Spatial coordinates provided as latitude and longitude (WGS84) with accuracy notes (approximately 8 m).
- Deployment timing aligned to Eastern European Winter Time (GMT+03:00); some dates/times corrected if camera settings differed (e.g., summer time).
- Site and camera placement characteristics recorded (e.g., height, distance to trail, orientation, tilt) to contextualize detection effort.

## Data quality and processing notes
- Time/date fields may require correction when cameras were misconfigured; corrections convert to Eastern European Winter Time.
- EXIF date/time vs actual recording may differ; comments available for such discrepancies.
- Some fields intentionally populated as n/a (not applicable) or n/r (not recorded), indicating incomplete or inapplicable data for certain deployments.

## Data provenance, sharing, and governance
- Data derive from multiple projects (NatEnvPr, REDFIRE, TREE) with related camera-trap locations and setups.
- Emphasizes that only Lynx-containing media are included, and camera metadata (IDs, locations, deployment duration) are recorded for transparency.
- Ambiguities in data sharing (e.g., certain fields or details) are addressed by noting data quality and processing steps.

## Implications for monitoring frameworks
- Supports assessment of monitoring coverage across sites, times, and camera setups.
- Enables cross-project comparisons of effort (deployment duration, image/video yield) and spatial distribution of Lynx detections.
- Provides baseline metadata for data governance, standardization, and reproducibility in environmental monitoring programs.

## Key limitations and considerations for users
- Missing or non-recorded data in several fields (n/a, n/r) may limit some analyses.
- Metadata standardization across projects is needed to maximize comparability.
- Time corrections and EXIF discrepancies require careful handling during analysis.