# Lynx_Dataset_Supporting_Document

## Overview
- A catalogue of motion-activated digital trap camera images (still images and some videos) of Eurasian Lynx (Lynx lynx) in the Ukrainian Chornobyl Exclusion Zone (CEZ), collected 2012–2018.
- Data come from three projects (TREE, NatEnvPr, REDFIRE) with varying study designs; cameras aimed to capture medium-large mammals, not designed for quantitative abundance or density estimates of lynx.
- Images are included with associated metadata and a pole-measuring scale; the dataset supports exploratory spatial analyses but is not a census.

## Study Area and Sites
- CEZ area: ~2600 km2 in northern Ukraine; diverse habitat mosaic including forests (majority), wetlands, rivers, lakes, scrub, and abandoned settlements.
- Environment: extensive floodplains, seasonal water bodies, reeds and willow-dominated zones; limited human activity outside central areas.
- Design: eight study sites within CEZ; camera traps deployed at 394 unique locations (some locations used across projects); most cameras used for 8–12 months per site (TREE used 8–9 weeks per deployment before relocation).
- No bait used in any study.

## Digital Trap Cameras and Deployment
- Camera models used: primarily Ltl Acorn 6210 MC, with several other models (Browning, Bushnell, ScoutGuard, Weltar, etc.).
- Settings: mostly still images, typically three images per triggering event with 0–5 second delay; infrared maximum power; recovery time 3–10 seconds; temperature-dependent sensor sensitivity (seasonally adjusted); some cameras recorded video (notably in 2016–2018 for TREE and others).
- Placement and orientation: cameras placed 3–10 m from activity areas, 0.5–1.1 m above ground; aimed to minimize false activations (facing away from direct sun); vegetation cleared in front of cameras; often on well-marked paths, intersections, or bridges; attempts made to reduce visibility where risk of human detection was high.
- Deployment details: up to 20 measuring poles (1 m, marked every 20 cm) placed in front of the camera during initial deployment to capture scale; poles subsequently removed; TREE deployments were random within sites.
- Data management: images and camera details are catalogued and linked; no universal standardization across models; full documentation of camera settings and deployment periods provided.

## Images and Image Catalogue Structure
- Total: 1570 Lynx still images, 23 Lynx videos, plus 32 measuring pole images.
- Catalogued by triggering event; each event row includes first and last image filenames for that trigger.
- Duplicate rows occur if multiple Lynx are visible in a single image event; separate records may exist for other animals or frames within the same event.
- Lynx identification: uniquely identified Lynx assigned IDs when possible (Camera_Trap_Location_ID + unique number, e.g., p0382-1); Lynx without identifiable features receive no unique ID.
- Image location and naming: images stored in folders named like Setup01_Site1_1396; metadata links to these folders via Image_Location_Folder_Name.
- Quality control: UKCEH staff verified lynx images and addressed any catalogue or site description queries.

## Data Catalogue and Key Fields
- Lynx_2012-2018_Image_Catalogue
  - Project_ID, Study_Site, Setup
  - Camera_Trap_Location_ID, Camera_Trap_Location_ID_Related_To_Project
  - Image_Location_Folder_Name
  - First_Image_Per_Triggering_Event, Last_Image_Per_Triggering_Event
  - Triggering_Event_Number
  - Date_And_Time_Image_Taken, Year, Month
  - Lynx_ID, Lynx_Gender_Age
  - Triggering_Event_Duration_Minutes
  - Day period (Night, Twilight, Day)
  - Number_Trapping_Days_Per_Month, Events_Per_Trapping_Day
  - Notes, Data_Used_For_Analysis_Y_Or_N

- Lynx_Camera_Details
  - Project_ID, Camera_Trap_Location_ID, Camera_Trap_Location_ID_Related_To_Project
  - Camera_Trap_Location_Latitude_WGS84, Camera_Trap_Location_Longitude_WGS84
  - Site, Year, Setup
  - Date_And_Time_Of_Camera_Setup_Eastern_European_Winter_Time
  - Date_And_Time_Of_Last_Day_Of_Camera_Opperation_European_Winter_Time
  - Comments_Relating_To_Date_And_Time_Settings
  - Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour
  - Make_Model_Of_Camera, Camera_ID
  - Duration_Of_Camera_Deployment
  - Total_number_Of_Still_Images_Taken_By_Camera
  - Total_Number_Of_Videos_Taken_By_Camera
  - Height_Of_Camera_Deployment_m, Distance_To_Nearest_Trail_m
  - Orientation_Of_Camera, Tilt_Of_Camera, Generic_Conditions

## Access and Organization
- Images and metadata are organized by project and setup, with linkage through IDs and folder names.
- Data include both Lynx detections and non-detection records to enable estimation of effort and detection probability when integrating with GIS workflows.

## Usage Guidance for GIS Specialists
- Potential uses:
  - Map camera trap locations and overlay with land cover, habitat layers, hydrology, and protected area boundaries.
  - Compute camera effort per site (days of operation, events per day) for effort-aware analyses.
  - Explore spatial patterns of Lynx detections over time (year, month, day vs night).
  - Support occupancy or presence-only modelling with explicit sampling effort and site covariates.
- Important considerations:
  - Not designed for quantitative abundance or density estimates; results should be framed as detections/relative activity or occupancy with caveats.
  - Heterogeneous study designs and camera models across projects. Model deployment duration and camera sensitivity varied, which can influence detectability.
  Use the Date/Time fields, Day period, and Setup to account for sampling effort and seasonal effects.
  Consider integrating ambient dose rate data cautiously; primarily relevant to environmental context rather than lynx detection.

## Data Quality, Limitations, and Ethics
- Variability in camera models, settings, and deployment lengths across sites and projects.
- Some years or setups have short deployments (TREE) versus longer deployments in other setups.
- Image quality depends on camera model, lighting conditions, and animal behaviour; not all lynx were identifiable, and some detections are duplicates across events.
- Data were collected with field safety and biosphere reserve considerations; no baiting was used.

## References and Acknowledgements
- Decree of the President of Ukraine (2016) establishing the Chornobyl radiation and ecological biosphere reserve.
- Development 2006: Forestry project in Chornobyl area.
- Gashchak et al. works on Lynx and other fauna in the CEZ.
- Acknowledgements: field assistance contributions acknowledged.