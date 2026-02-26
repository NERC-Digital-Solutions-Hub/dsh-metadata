# Lynx_Camera_Details

## Overview
- Metadata and measurements for Lynx camera-trap deployments across projects (NatEnvPr, REDFIRE, TREE).
- Captures location (GPS), temporal (setup and operation times), device (camera make/model, ID), deployment context (site, year, setup period), and activity metrics (image/video counts).

## Key fields and purposes
- Project_ID: Identifies the project context for the image set (NatEnvPr, REDFIRE, TREE).
- Camera_Trap_Location_ID: Numerical ID for each camera site; some locations reused across projects (e.g., P0012, P0028, P0042, P0104, P0108).
- Camera_Trap_Location_ID_Related_To_Project: Location ID specific to a given project.
- Camera_Trap_Location_Latitude_WGS84 / Camera_Trap_Location_Longitude_WGS84: GPS coordinates; decimal degrees; ~8 m accuracy.
- Study_Site: Ordinal site indicator (1–8).
- Year: Year of camera deployment.
- Setup: Deployment setup period (1–13).
- Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time / Date_And_Time_Of_Last_Day_Of_Camera_Operation_European_Winter_Time: Timestamps in Eastern European Winter Time (GMT+03:00); DST corrections applied where needed.
- Comments_Relating_To_Date_And_Time_Settings: Explanations for date/time discrepancies (e.g., EXIF vs actual).
- Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour: Ambient radiation level at 1 m height; not consistently recorded (n/r).
- Make_Model_Of_Camera / Camera_ID: Camera hardware details; last four digits sometimes shown on image bar; some records missing.
- Duration_Of_Camera_Deployment: Deployment length in days.
- Total_number_Of_Still_Images_Take_By_Camera / Total_Number_Of_Videos_Taken_By_Camera: Totals per setup; only Lynx-containing images/videos included.
- Height_Of_Camera_Deployment_m / Distance_To_Nearest_Trail_m / Orientation_Of_Camera / Tilt_Of_Camera: Physical deployment characteristics.
- Generic_Site_Description: Brief site description.

## Data quality, gaps, and standardization
- Some fields marked as n/a or n/r; gaps affect completeness and cross-project comparability.
- Time data required careful handling due to DST corrections; standardization to Eastern European Winter Time implemented.
- GPS accuracy ~8 m; consider precision needs for fine-grained spatial analyses.
- Metadata consistency across projects (e.g., site IDs, setup coding) is important for integration.

## Temporal and spatial metadata considerations
- Spatial: GPS coordinates enable site mapping and cross-site coverage assessment.
- Temporal: Setup period, deployment duration, and operation end dates support activity timing analyses; time normalization is critical for multi-project comparisons.
- Site context: Study_Site and Generic_Site_Description aid in understanding habitat or site-specific effects.

## Governance, reuse, and action implications for Data Leaders
- Provenance and discoverability: Clear linkage between projects, sites, and deployments supports data reuse across networks.
- Quality assurance: Document and address gaps (ambient dose data, camera IDs, full metadata for all fields) to improve data quality.
- Standardization: Develop and maintain a metadata dictionary to harmonize field names, units, and coding across projects.
- Collaboration and co-ownership: Shared camera-trap metadata across NatEnvPr, REDFIRE, and TREE supports broader data ecosystems and stakeholder engagement.
- Utilization: Enables assessment of data coverage, camera effort, and animal detection potential, informing data strategy and resource allocation.