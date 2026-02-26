# Lynx_Camera_Details

- A dataset describing Lynx camera trap deployments linked to multiple environmental projects (NatEnvPr Ukrainian national program of environmental studies, REDFIRE, TREE).
- Designed to support standardized, monitorable evidence of Lynx presence and site activity over time.

## Data Structure and Key Fields

- Project_ID: Identifier for the project the images were collected under.
- Camera_Trap_Location_ID: Numeric ID of the camera trap location; some locations were shared across projects (e.g., P0012, P0028, P0042, P0104, P0108).
- Camera_Trap_Location_ID_Related_To_Project: Relational ID linking locations across projects.
- Camera_Trap_Location_Latitude_WGS84 & Camera_Trap_Location_Longitude_WGS84: GPS coordinates (decimal degrees; WGS84; ~8 m accuracy).
- Study_Site: Study site number (1 to 8).
- Year: Year of camera deployment.
- Setup: Setup period identifier (1–13).
- Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time: Setup timestamp (Eastern European Winter Time, GMT+03:00); corrections applied if cameras were mis-set.
- Date_And_Time_Of_Last_Day_Of_Camera_Operation_European_Winter_Time: Last operation timestamp (Eastern European Winter Time).
- Comments_Relating_To_Date_And_Time_Settings: Explanations for any discrepancies between EXIF date/time and actual deployment times (e.g., wrong camera settings, bugs).
- Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour: Ambient dose rate at 1 m above ground at the camera site (µSv/h); measured during deployment year; data may be not recorded (n/r).
- Make_Model_Of_Camera: Camera make and model.
- Camera_ID: Serial number of the camera (last four digits typically used); data sometimes not recorded.
- Duration_Of_Camera_Deployment: Length of deployment in days.
- Total_Number_Of_Still_Images_Taken_By_Camera: Total still images captured during a setup; only Lynx-containing images are included.
- Total_Number_Of_Videos_Taken_By_Camera: Total video clips captured during a setup; only Lynx-containing clips are included.
- Height_Of_Camera_Deployment_m: Height of camera deployment above ground (meters).
- Distance_To_Nearest_Trail_m: Distance from camera to location where Lynx activity was anticipated.
- Orientation_Of_Camera: Cardinal/compass orientation of camera.
- Tilt_Of_Camera: Tilt angle of camera.
- Generic_Site_Description: Brief description of the site area.

## Spatial and Temporal Details

- Coordinates, deployment year, and site identifiers enable spatial mapping and temporal analyses of Lynx activity.
- Time data are standardized to Eastern European Winter Time (GMT+03:00); corrections applied if clocks were mis-set.
- Temporal metadata includes setup and last operation dates to define active monitoring windows.

## Data Quality, Standardisation, and Notes

- Some fields are marked as not applicable (n/a) or not recorded (n/r), indicating incompleteness in certain deployments.
- EXIF or camera-trap embedded times may differ from actual deployment times; notes explain adjustments and potential causes (wrong settings, bugs, etc.).
- GPS accuracy is approximate (about 8 m); this informs uncertainty in spatial analyses.
- Data focuses on Lynx-containing imagery/videos; excludes other content.

## Data Management, Access, and Outputs

- Projects and locations are linked to ensure traceability across datasets (e.g., cross-project location reuse).
- Aimed at standardised analysis outputs and the ability to store and share datasets via appropriate portals.
- Outputs suitable for maps, charts, and reports to illustrate environmental monitoring results and policy performance related to Lynx presence.

## Relevance to Environmental Monitoring Aims and Challenges

- Aligns with the Analysts Monitoring the Environment archetype by providing a structured, validated data source to assess environmental health and species monitoring over time.
- Facilitates data verification, cleaning, and transformation to produce standardized outputs for policy scrutiny.
- Highlights key challenges: increasing data value through integration with other data sources, and enabling access to underlying data for broader reuse.