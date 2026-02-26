# Lynx_Camera_Details

## Overview
- A metadata-rich dataset documenting Lynx camera-trap deployments across projects (NatEnvPr, REDFIRE, TREE) with eight study sites. 
- The dataset records per-camera deployment details and outputs (images/videos) containing Lynx, enabling presence/occurrence analyses and cross-project comparisons.

## Key fields and data provenance
- Project_ID: identifies the contributing project (NatEnvPr, REDFIRE, TREE); multiple projects may share camera locations.
- Camera_Trap_Location_ID: numeric ID for each camera trap location; notes that some locations are shared between TREE and NATECO projects (examples: P0012, P0028, P0042, P0104, P0108).
- Camera_Trap_Location_ID_Related_To_Project: numeric ID linking a location to a specific project.
- Camera_Trap_Location_Latitude_WGS84 and Camera_Trap_Location_Longitude_WGS84: site coordinates in decimal degrees, GPS-measured, using WGS84; accuracy approximately 8 meters.
- Study_Site: study site identifier (1–8).
- Year: year of camera deployment (YYYY).
- Setup: deployment setup period (1–13).
- Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time: deployment date/time, corrected to Eastern European Winter Time (GMT+03:00) when needed.
- Date_And_Time_Of_Last_Day_Of_Camera_Operation_Eastern_European_Winter_Time: last operation date/time, corrected to E. European Winter Time.
- Comments_Relating_To_Date_And_Time_Settings: notes on date/time settings, including EXIF discrepancies, camera setting issues, and known bugs.
- Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour: ambient radiation level at the site (µSv/h); measured during deployment year; some records are not recorded.
- Make_Model_Of_Camera: camera make and model.
- Camera_ID: camera serial number; formatting details provided; some records marked as not recorded.
- Duration_Of_Camera_Deployment: deployment duration per setup, in days.
- Total_number_Of_Still_Images_Taken_By_Camera: total still images captured per setup; only images containing Lynx are included.
- Total_Number_Of_Videos_Taken_By_Camera: total video clips captured per setup; only Lynx-containing clips are included.
- Height_Of_Camera_Deployment_m: height of camera deployment above ground (meters).
- Distance_To_Nearest_Trail_m: distance from camera to the main activity trail (meters).
- Orientation_Of_Camera: camera facing direction (N, S, E, W, and intermediates).
- Tilt_Of_Camera: tilt angle of the camera.
- Generic_Site_Description: brief description of the site environment.

## Data quality, standards and interoperability
- Well-defined field explanations accompany each attribute, with explicit units where applicable (e.g., coordinates in decimal degrees, µSv/h for ambient dose rate).
- Time data include explicit time zone corrections to Eastern European Winter Time; notes address potential EXIF discrepancies.
- Some fields include values such as “n/r” (not recorded) or “n/a” (not applicable), indicating data gaps or non-applicable fields.
- Cross-project interoperability is supported by Camera_Trap_Location_ID and Camera_Trap_Location_ID_Related_To_Project, enabling linking of locations across TREE and NATECO projects.

## Governance and sharing considerations
- Data should be uploaded to appropriate portals and catalogued with clear metadata to support discoverability by data users.
- Maintain documentation of data provenance, including project associations, site locations, time corrections, and any data quality issues (e.g., EXIF/time discrepancies, missing values).
- Track data updates and versioning, especially where time corrections or location mappings change between projects.
- Include disclosures that datasets contain only Lynx-containing imagery/clips, which is essential for user expectations and downstream analyses.
- Where data are missing (n/r) or not recorded, provide rationale and, if possible, intent to fill gaps in future updates.

## Practical implications for Data Stewards
- Ensure metadata completeness and consistency across fields, especially:
  - Geospatial data (latitude/longitude in WGS84) and associated accuracy.
  - Time-related fields with consistent time zone corrections and notes on any EXIF discrepancies.
  - Cross-project location linkage via related-location IDs.
  - Clear counts for still images and videos per camera deployment, restricted to Lynx content.
  - Camera deployment parameters (height, distance to trail, orientation, tilt) for contextual reuse.
- Standardize interpretations of missing values (n/r vs. n/a) and provide guidance to data creators to minimize ambiguities.
- Validate and harmonize camera identifiers and model information to support reproducibility and cross-dataset analyses.
- Document any data limitations or embargoes and plan for updates to reflect new deployments or corrected timestamps.

## Challenges and considerations for Data Stewards
- Incomplete user needs or evolving downstream uses may require flexible yet well-documented metadata to accommodate diverse analyses.
- Timely data acquisition across multiple projects and formats can lead to gaps or non-interoperable solutions; cross-project linking helps mitigate this but requires ongoing curation.
- Handling large datasets with rich metadata (images/videos, time stamps, GPS) necessitates robust data governance, version control, and clear data sharing policies.