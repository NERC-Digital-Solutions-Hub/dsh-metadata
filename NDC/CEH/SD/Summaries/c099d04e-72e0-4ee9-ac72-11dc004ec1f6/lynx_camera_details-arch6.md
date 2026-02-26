# Lynx_Camera_Details

- Overview
  - Dataset describing Lynx camera trap deployments across multiple projects (NatEnvPr Ukrainian national program of environmental studies, REDFIRE, TREE).
  - Captures per-camera deployment details: location, timing, equipment, and imaging outputs, enabling cross-project comparisons and self-serve data exploration.

- Key fields and meanings (by category)
  - Identifiers and study scope
    - Project_ID: project identifier (NatEnvPr, REDFIRE, TREE)
    - Camera_ID: serial number of camera
    - Study_Site: 1 to 8
    - Year: deployment year (YYYY)
    - Setup: setup period (1–13)
  - Location and site context
    - Camera_Trap_Location_ID: numeric ID for trap location
    - Camera_Trap_Location_ID_Related_To_Project: numeric ID linking to related project location
    - Camera_Trap_Location_Latitude_WGS84 / Camera_Trap_Location_Longitude_WGS84: GPS coordinates (WGS84)
    - Height_Of_Camera_Deployment_m: camera height in meters
    - Distance_To_Nearest_Trail_m: proximity to main activity area
    - Orientation_Of_Camera: cardinal direction
    - Tilt_Of_Camera: tilt angle
    - Generic_Site_Description: brief site description
  - Temporal details and data quality
    - Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time: setup timestamp (GMT+03:00)
    - Date_And_Time_Of_Last_Day_Of_Camera_Operation_European_Winter_Time: last operation timestamp
    - Comments_Relating_To_Date_And_Time_Settings: notes about date/time settings; EXIF vs actual times may differ
    - Year and Setup fields support temporal analyses and alignment with other datasets
  - Measurements and outputs
    - Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour: environmental radiation context (μSv/h); measured during deployment year
    - Total_number_Of_Still_Images_Taken_By_Camera: total still images captured (only Lynx-present images included)
    - Total_Number_Of_Videos_Taken_By_Camera: total video clips captured (only Lynx-present)
  - Camera specifications and deployment mechanics
    - Make_Model_Of_Camera: camera make and model
    - Camera_ID (serial in dataset): camera serial details
    - Duration_Of_Camera_Deployment: deployment duration in days

- Data quality notes and caveats
  - Some fields are not recorded (n/a) or not recorded (n/r); data completeness varies by row
  - Date/time corrections applied to align with Eastern European winter time (GMT+03:00) when cameras mis-set or recorded in summer time
  - EXIF date/time discrepancies can occur due to wrong camera settings, hardware quirks, or bugs
  - Coordinate accuracy is approximately 8 meters
  - Counts include only images/videos containing Lynx, not all content captured by cameras

- Cross-project relationships and scope
  - Some camera locations are shared across TREE and NATECO projects (examples: P0012, P0028, P0042, P0104, P0108)
  - Data spans multiple study sites (1–8) and multiple setup periods, enabling cross-site and cross-project comparative analyses

- Practical uses for data support and product development
  - Build dashboards or pivot-table reports to explore Lynx presence by site, year, and setup period
  - Map camera locations and analyze spatial distribution in relation to site characteristics
  - Combine with environmental measurements (e.g., ambient dose rate) to study context of detections
  - Create self-serve data products for end users to filter by year, site, or setup period
  - Flag and track missing or questionable fields for data cleaning and quality assurance

- Recommendations for data cleaning and integration
  - Verify and harmonize timestamps to a consistent timezone; document any conversions
  - Flag rows with n/a or n/r fields; assess impact on analyses and impute or exclude as appropriate
  - Validate coordinates against site descriptions; adjust if needed and record uncertainty
  - Ensure Lynx-only counts are used for imaging metrics; distinguish from other species if integrated later
  - Document cross-project mappings for Camera_Trap_Location_ID_Related_To_Project to support joined analyses across TREE/NATECO datasets