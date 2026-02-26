# CHAR_November_2020_March_2021_Camera_Trap_Image_Catalogue _Supporting_Document

## Purpose and Scope
- Document supporting a CHAR project study assessing large mammal activity in the Ukrainian part of the Chornobyl Exclusion Zone after extensive wildfires (Nov 2020–Mar 2021).
- Aims to provide a standardized, analysable dataset for environmental monitoring and policy-relevant interpretation of mammal responses to fire within a radiologically exposed landscape.

## Study Design and Sites
- Three sites, each ~80 km², within the Ukrainian Exclusion Zone; sites chosen to reflect a contamination gradient.
  - Site 1: northeast, most contaminated.
  - Site 2: western trace of the release plume, large contamination gradient.
  - Site 3: south, least contaminated.
- Timeframe for the camera deployment in this setup: November 2020–March 2021 (Setup 2; after a 2014–2015 baseline in earlier work).
- Data and images were collected using standardized camera-trap methods described below and were later provided to UKCEH.

## Equipment and Deployment Details
- Cameras: Ltl Acorn 6210MC, motion-activated with passive infrared (PIR) sensor and 940 nm invisible infrared flash; effective range ~10 m.
- Height and orientation: camera mounted at ~0.6–0.7 m, usually facing north to reduce sun-triggered false positives.
- Field setup: clear surrounding vegetation in front of camera (~100 m² clearance) where necessary.
- Triggering and capture: three-image burst per triggering event; 0–1 s between images; ~2–4 s recovery before next burst; new triggering event typically begins after ~90 seconds without activity.
- No bait used. Some camera deployments were affected by field logistics (e.g., theft noted at some camera locations in Site 1).

## Data Collected and File Structure
- Total images: 11,633 trap-camera images captured during Setup 2 (Nov 2020–Mar 2021); 692 images containing people, vehicles, or CHAR staff during setup were catalogued but not included in the image dataset to protect privacy.
- Image metadata and catalogue: stored in CHAR_Nov_2020_Mar_2021_Camera_Trap_Image_Catalogue (Microsoft Excel) with site, camera, setup, image location, date/time, day period, species, counts, triggering events, and notes.
- Folder structure in dataset:
  - Setup2_Site1, Setup2_Site2, Setup2_Site3
  - Within each site: folders named by camera (e.g., Setup2_Site1_1570)
  - Subfolders per species; individual image files are .jpgs.
- Image data fields (per row): Site, Camera_Location_Identifier, Setup_Number, Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period, Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Sequential, Notes.
- Event handling: first row of a triggering event contains the total animals; subsequent rows for that event marked as not applicable (n/a); images labeled with “Nothing” may still be part of a triggering event if later images show identifiable species.
- Privacy and disturbances: images containing people or vehicles catalogued as disturbance but not included in the dataset; disturbing events due to human activity recorded in the notes.

## Metadata and Site Descriptions
- Site Descriptions file: CHAR_Nov_2020_Mar_2021_Camera_Trap_Site_Descriptions
  - Includes: Setup_Number, Site, Camera_Location_Identifier, GPS coordinates (WGS84), camera location descriptions, ambient dose rate at camera location (µSv h⁻¹), camera deployment dates, days in operation, and habitat/vegetation descriptors (e.g., tree species, grasses, water sources).
  - Burn degree around camera within 200 m (None, Low, Medium, High, Very High, Total destruction) to characterize fire impact near camera sites.
  - Vegetation species observed at sites (list includes alder, aspen, birch, oaks, pines, willows, grasses, bilberry, nettle, etc.).
- Camera Details file: CHAR_Nov_2020_Mar_2021_Camera_Trap_Details
  - Includes: Setup_Number, Site, Camera_Location_Identifier, Camera_Serial_Number (as displayed on images), Folder_Name_Where_Images_Are_Located, Start/End DateTime for deployment, Number_Of_Days_Camera_In_Operation, Number_Of_Images_Taken, Notes.
  - Notable events: camera 1575 at Site 1 stolen during Setup 2; camera 2081 stolen (also noted in entries).
- Related reference for Setup 1 data: Barnett et al., 2022 (Wildlife camera trap photographs from the Chornobyl Exclusion Zone, June 2020 – November 2020).

## Data Processing, Quality Assurance, and Access
- Data collection and image metadata were compiled by staff of the Chornobyl Center for Nuclear Safety; subsequent quality checking and queries resolved by UKCEH staff.
- Data management and storage adhered to standardized, auditable processes; datasets prepared for sharing with UKCEH and broader research use.
- Outputs include a comprehensive catalogue of images and associated metadata, suitable for analyses of mammal abundance, presence, and spatial distribution across the three sites.

## Content Highlights and Key Outputs
- Species coverage: mammals and birds with a wide range of taxa identified, plus unidentifiable records when image quality prevented confident identification.
- Table 1 (highlights from the catalogue):
  - Red deer (Cervus elaphus): 4491 total images attributed; 4052 images with species visible.
  - Przewalski’s horse (Equus ferus przewalskii): 771 total; 694 visible.
  - Eurasian elk (Alces alces): 1617 total; 1387 visible.
  - Grey wolf (Canis lupus): 546 total; 375 visible.
  - Red fox (Vulpes vulpes): 201 total; 122 visible.
  - Red squirrel (Sciurus vulgaris): 3 total; 2 visible.
  - Roe deer (Capreolus capreolus): 792 total; 654 visible.
  - Wild boar (Sus scrofa): 639 total; 551 visible.
  - Unidentifiable mammals/birds: substantial counts (e.g., 213 unidentifiable mammals; 9 unidentifiable birds) reflecting image quality limits.
  - Humans/vehicles and service records: present in catalogue metrics but images of people/vehicles are not included; disturbance noted in the dataset.
- Overall dataset volume focuses on Setup 2 period; Setup 1 data are documented in Barnett et al. (2022).

## Funding, Acknowledgements, and Access
- Funded by the Natural Environment Research Council (NERC; grants NE/V009346/1 and EP/V520846/1) with additional support from CERAD (Norway) for data preparation.
- Acknowledgements to field staff and collaborators for assistance during fieldwork.

## Relevance for Environmental Monitoring Analysts
- Demonstrates standardized data collection, verification, and QA across multiple sites with a clear protocol for camera-trap deployment and metadata capture.
- Provides a robust, structured dataset suitable for temporal and spatial monitoring of mammal activity following wildfire within a radiological landscape.
- Highlights data management practices to maximize dataset value beyond a single study (e.g., detailed metadata, site descriptions, burn impact indicators, and accessibility considerations).