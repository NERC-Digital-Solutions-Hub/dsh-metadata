# CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue_Supporting_Document

## Overview
- Document describing the CHAR project camera-trap dataset collected in the Ukrainian exclusion zone following the 1986 Chernobyl accident and 2020 wildfires.
- Objective: assess large mammal activity post-fire; provide a structured image catalogue and metadata for environmental monitoring.
- Timeframe and scope: June–November 2020; three sites (each ~80 km²) within the exclusion zone; 13 cameras per site; total dataset includes 61,736 images (setup 1).
- Data products: image catalogue with species identifications and event counts, site and camera descriptions, and deployment metadata.

## Study Design and Deployment
- Context: Exclusion zone around Chernobyl with varying contamination; three sites chosen to capture gradients of burn and disturbance.
- Equipment and setup:
  - Cameras: Ltl Acorn 6210MC; PIR motion sensors; 940 nm infrared flash; height ~0.6–0.7 m; most cameras faced north.
  - Habitat management: vegetation cleared within ~100 m² in front of each camera where needed; no bait used.
  - Deployment protocol: 13 cameras per site; each camera location had a unique identifier; three-image burst per triggering event; ~2–4 s recovery between bursts.
  - Triggering: new triggering event starts after at least 90 seconds without movement; some events may contain multiple observations.
- Data capture specifics: images captured day, night, and transition; times adjusted to local time zones with one noted exception.

## Data and Metadata Capture
- Data collection and transfer:
  - Images and metadata downloaded November 2020 by Chornobyl Center staff; supplied to UKCEH as .jpeg images and MS Excel files.
  - Image catalogue populated by a single UKCEH staff member with species, counts, triggering events, and notes.
- Roles and quality control:
  - Site descriptions and camera information provided by Chornobyl Centre; QC by UKCEH and Chornobyl Centre; amendments made as needed.
- Privacy considerations:
  - Images containing people or CHAR team members are catalogued but not included in the dataset to protect privacy.
  - Disturbance from human activity documented in notes.

## Data Structure and Content
- Four main CSV files (data tables) describing the dataset:
  - CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue.csv
    - Key fields: Site, Camera_Location_Identifier, Setup_Number, Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period, Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Number_Sequential, Young_Animal_In_Image, Notes.
    - Rules: separate rows per species when multiple species appear; first row of a triggering event shows total animals; images with people/vehicles are documented but do not contribute to animal counts in triggering events.
    - Excludes images containing people or CHAR team members for privacy.
  - CHAR_Jun_Nov_2020_Camera_Trap_Site_Descriptions.csv
    - Key fields: Setup_Number, Site, Camera_Location_Identifier, Camera_Location_Latitude_WGS84, Camera_Location_Longitude_WGS84, Camera_Location_Description, Ambient_Dose_Rate_At_Camera_Location, Description_Of_Animal_Trails_Within_20m_Radius, Degree_Of_Burn_Of_Area_Affected_By_Fire_Within_200_Metre_Radius_Of_Camera_Location, Vegetation and tree species observations.
  - CHAR_Jun_Nov_2020_Camera_Trap_Details_And_Image_Summary.csv
    - Key fields: Setup_Number, Site, Camera_Serial_Number_As_Displayed_On_Images, Folder_Name_Where_Images_Are_Located, Start_Date_Time_Camera_Deployment, End_Date_Time_Camera_Deployment, Number_Of_Days_Camera_Deployed, Number_Of_Images_Taken, Notes.
  - CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue (referenced as the central image index)
- Dataset scale and content:
  - 61,736 images across Setup 1 (June–November 2020).
  - Species categories include a mix of mammals, birds, and invertebrates; numerous identifications are provided, with some images unidentifiable due to quality.
  - Some cameras were missing images due to theft (e.g., camera 1556) or operational errors (e.g., camera 1541).

## Monitoring Framework Considerations
- Metadata richness: extensive fields describing location, time, environmental context, and burn severity to support causal and comparative analyses.
- Data quality and provenance: centralized data capture, cross-checking between field team and data managers, and explicit notes on data limitations.
- Data governance and sharing: underlying data and descriptive metadata are documented; privacy considerations implemented by excluding personal images from the dataset.
- Timeliness and accessibility: data compiled and made available after field deployment; degradation or gaps acknowledged (theft, non-operation, and timezone notes).
- Usability for policy and assessment: structured data enable monitoring of wildlife responses to fire disturbance within a post-nuclear radiological context; supports analyses of species presence/absence, relative abundance, and habitat associations.

## Limitations and Considerations for Use
- Timezone irregularity: one camera (0851) had incorrect time zone setting, affecting time-stamping.
- Identification and quality: some species identifications are unidentifiable due to image quality; multiple species per image require separate rows.
- Data gaps: at least two cameras did not yield images for various reasons (theft, non-operation); September–November windows may have uneven coverage.
- Privacy constraints: images with people or service personnel excluded from the dataset.

## Acknowledgements and Funding
- Acknowledgements to field staff and collaborators (e.g., Igor Chyzhevsky, Maksim Krachkovsky, Sergey Paskevich).
- CHAR project funded by NERC (Grant NE/V009346/1 and EP/V520846/1).