# Lynx_Camera_Details

- Dataset scope
  - Metadata for camera trap deployments used to study Lynx across multiple projects (NatEnvPr Ukrainian national program of environmental studies, REDFIRE, TREE).
  - Only images containing Lynx are included in the dataset.

- Key identifiers and project linkage
  - Project_ID: identifies the project (e.g., NatEnvPr, REDFIRE, TREE).
  - Camera_Trap_Location_ID: numeric ID for each camera trap location; some locations are shared across TREE and NATECO projects (examples: P0012, P0028, P0042, P0104, P0108).
  - Camera_Trap_Location_ID_Related_To_Project: numeric ID linking the trap location to a specific project.

- Location and site details
  - Camera_Trap_Location_Latitude_WGS84 and Camera_Trap_Location_Longitude_WGS84: GPS coordinates in decimal degrees, measured with GPS (WGS84); accuracy around 8 meters.
  - Study_Site: site number (1 to 8).
  - Generic_Site_Description: brief description of the site area.

- Temporal coverage and timing
  - Year: year of camera deployment (YYYY).
  - Setup: setup period indicator (1–13).
  - Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time: deployment date/time in Eastern European Winter Time (GMT+03:00); note: corrected if the camera was set to a different time zone.
  - Date_And_Time_Of_Last_Day_Of_Camera_Operation_European_Winter_Time: last day/time of operation; corrected for DST where needed.
  - Comments_Relating_To_Date_And_Time_Settings: notes about date/time settings; may reflect EXIF discrepancies due to camera settings, bugs, etc.

- Camera specifications
  - Make_Model_Of_Camera: camera brand and model.
  - Camera_ID: serial number (formatting notes indicate partial digits may be shown or omitted; some values may be not recorded).

- Deployment characteristics
  - Duration_Of_Camera_Deployment: deployment length in days for a given setup.
  - Height_Of_Camera_Deployment_m: height of the camera above ground (meters).
  - Distance_To_Nearest_Trail_m: distance from camera to the main activity trail (meters).
  - Orientation_Of_Camera: cardinal orientation (N, S, E, W, and intermediates).
  - Tilt_Of_Camera: tilt angle of the camera.

- Activity and output
  - Total_Number_Of_Still_Images_Take_By_Camera: total Lynx-containing still images captured during the setup.
  - Total_Number_Of_Videos_Taken_By_Camera: total Lynx-containing video clips captured during the setup.

- Data quality notes and gaps
  - n/a = not applicable; n/r = not recorded.
  - Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour: ambient dose rate measured at 1 meter above soil at the camera location; measured during deployment year; some records are not recorded.
  - EXIF vs. actual timestamps may differ; time corrections applied to ensure consistency.

- Use and implications for analysts
  - Enables linking Lynx detections to spatial (GPS coordinates, height, distance to trails) and temporal (deployment year, setup period, operation window) factors.
  - Facilitates cross-project comparisons where locations overlap; coordinates are standardized to WGS84.
  - Handles data quality considerations by accounting for DST corrections, potential EXIF discrepancies, and missing values.
  - Supports model development and hypothesis testing on detection rates in relation to camera model, deployment duration, site characteristics, and environmental context.