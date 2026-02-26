# CHAR_November_2020_March_2021_Camera_Trap_Image_Catalogue Supporting Document

## Overview
- Study context: post-fire mammal activity within the Ukrainian part of the Chornobyl Exclusion Zone (CZ) following severe wildfires in 2020.
- Study design: three 80 km2 sites within the CZ, each with 13 motion-activated cameras (total 39 cameras) deployed June 2020–August 2021.
- Data product: a catalogue of 11,633 trap camera images (setup 2: Nov 2020–Mar 2021) with detailed metadata and habitat/ site descriptions.
- Privacy: images containing people, vehicles, or CHAR personnel excluded from the image dataset (692 images), though catalogued with notes.

## Data structure and main content
- Image catalogue file: CHAR_Nov_2020_Mar_2021_Camera_Trap_Image_Catalogue
  - Core fields per image row include: Site, Camera_Location_Identifier, Setup_Number, Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period, Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Sequential, Notes.
  - Triggering events: sequences typically begin after 90 seconds; first row for an event may contain a summary of total animals; subsequent rows marked n/a where not applicable.
  - Special categories: images with 'Service' (camera setup/maintenance) labeled separately; images with people/vehicles catalogued but not included in dataset.
  - Species data: Table 1 lists mammals and birds observed, with two counts per species (total images attributed vs. images where species was visible); several entries are unidentifiable due to image quality.
  - Folder structure: images stored under Setup2_Site1, Setup2_Site2, Setup2_Site3; within each site, subfolders per camera location (e.g., Setup2_Site1_1570) and further per species.
- Site descriptions file: CHAR_Nov_2020_Mar_2021_Camera_Trap_Site_Descriptions
  - Content per camera deployment: Setup_Number, Site, Camera_Location_Identifier, Camera_Location_Latitude_WGS84, Camera_Location_Longitude_WGS84, Camera_Location_Description, Ambient_Dose_Rate_At_Camera_Location, Description_Of_Animal_Trails_Within_20m_Radius_Of_Camera, Degree_Of_Burn_Of_Area_Affected_By_Fire_Within_200_Metres_Radius, Vegetative species identified at site.
  - Coordinates are in decimal degrees (WGS84); ambient dose rates measured (µSv/h) in June 2020 (with one site measured May 2021).
  - Vegetation and habitat notes are captured; all information recorded by the same field recorder.
- Camera details file: CHAR_Nov_2020_Mar_2021_Camera_Trap_Details
  - Deployment metadata: Setup_Number, Site, Camera_Location_Identifier, Camera_Serial_Number_As_Displayed_On_Images, Folder_Name_Where_Images_Are_Located.
  - Deployment timing: Start_Date_Time_Camera_Deployment, End_Date_Time_Camera_Deployment; Number_Of_Days_Camera_In_Operation; Number_Of_Images_Taken; Notes.
  - Anomalies: some camera locations (e.g., camera 1575 at Site 1) were stolen during setup 2; corresponding serial numbers reflect the disruption.
- Supplementary context
  - Three sites defined within the Ukrainian portion of the CZ, each ~80 km2, with distinct contamination gradients (Site 1 most contaminated, Site 2 western plume, Site 3 least contaminated).
  - Images are part of a larger CHAR project; setup 1 dataset is described in Barnett et al. (2022) for comparative context.
  - Data quality assurance performed by UKCEH; descriptive parameters recorded by the same Chornobyl Center staff member.

## Spatial and data quality context
- Spatial framing
  - Three documented camera deployments with precise latitude/longitude (WGS84) coordinates per camera location.
  - Data include ambient radiation context and burn degree within 200 m, enabling spatial analyses of exposure and fire impact.
- Data quality and curation
  - Images and metadata QA-ed by UKCEH; privacy-preserving handling of images containing people/vehicles.
  - Consistent naming conventions and folder structure to support GIS ingestion and reproducible workflows.
  - Some data limitations noted: camera locations and serial numbers may be missing or compromised due to theft; day/night delineation is camera-driven and somewhat subjective.

## GIS- and data-use implications
- Suitable GIS workflows
  - Import site descriptions to create a point layer of camera locations with attributes: site, camera_id, coordinates, ambient_dose_rate, habitat description, burn degree, and vegetation.
  - Join with image catalogue to produce per-camera time-series: counts by species, triggering events, and presence/absence data.
  - Create species distribution summaries by site (e.g., Red deer, Red fox, Red deer totals) and by setup period.
  - Overlay camera locations with fire impact gradients and Cs-137 deposition (decay-corrected to 2021) for contextual analyses.
- Potential analyses
  - Spatial distribution of mammal and bird detections across the three sites.
  - Relationship between fire burn degree, ambient radiation, habitat type, and wildlife detections.
  - Temporal patterns across setup 2 (Nov 2020–Mar 2021) and integration with setup 1 data from Barnett et al. (2022).
- Data integration considerations
  - Ensure alignment of Image_Location_Folder_Name with the corresponding camera location when mapping images.
  - Use triggering event numbers to aggregate per-event counts and reduce duplicate counting across frames.

## Limitations and caveats
- Privacy-preserving exclusion: 692 images containing people/vehicles are catalogued but not included in the image dataset.
- Data gaps: some camera identifiers and serial numbers were stolen during setup 2, affecting traceability for specific equipment.
- Classification caveats: species identifications may be uncertain for some images (unidentifiable cases noted); day/night/transition classification is automated and subjective.
- Single-recorder notes: habitat and burn-degree observations were recorded by the same individual, which may influence consistency.

## References and acknowledgements
- Primary reference for related setup 1 data: Barnett et al., 2022 (Wildlife camera trap photographs from the Chornobyl Exclusion Zone, Ukraine, June 2020–November 2020).
- Acknowledgements: thanks to field assistants; funding from NERC (Grant NE/V009346/1 and EP/V520846/1) and CERAD (Norway) for data preparation support.