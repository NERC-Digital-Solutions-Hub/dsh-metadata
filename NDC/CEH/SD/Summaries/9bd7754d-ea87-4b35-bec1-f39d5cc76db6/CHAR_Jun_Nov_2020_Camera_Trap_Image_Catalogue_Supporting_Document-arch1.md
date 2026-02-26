# CHAR_Jun_Nov_2020_Camera_Trap_Image_Cat alogue_Supporting_Document

- Context and purpose
  - CHAR project study of large mammal activity in the Ukrainian portion of the Chernobyl exclusion zone after wildfire disturbance (June 2020 – November 2020 for the dataset; extended fieldwork through 2021).
  - Data are collected to identify patterns, correlations, and potential predictors of wildlife responses to post-fire conditions and radiation context.

- Study design and deployment
  - Three sites within the 80 km2 each exclusion zone area (Site 1 northeast, Site 2 western plume, Site 3 south; collectively capturing a contamination gradient).
  - 13 camera traps per site (total 39) using Ltl Acorn 6210MC cameras.
  - Deployment duration for Setup 1: June–November 2020; additional fieldwork occurred June 2020–August 2021.
  - Camera setup details
    - Height 0.6–0.7 m, often mounted on trees; most facing north.
    - Field clearance of ~100 m2 in front of each camera; no bait used.
    - Night/Day capture via PIR sensor and 940 nm infrared flash (up to ~10 m).
    - Calibration poles deployed before first use; images of poles available in the dataset for scaling.
  - Imaging parameters
    - Three-image burst per triggering event; ~0–1 s between images; 2–4 s recovery before next burst.
    - New triggering event after at least 90 seconds since last observation; some sequences may be longer if an animal remains.
    - Some images may miss fast-moving animals due to burst timing.

- Data management and metadata
  - Images and metadata downloaded November 2020; stored as .jpeg images and MS Excel files.
  - Catalogue contains:
    - Image-level data: Site, Camera_Location_Identifier, Setup_Number (Setup 1), Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period, Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Number_Sequential, Young_Animal_In_Image, Notes.
    - Distinction between images of animals/birds vs. disturbances (people/vehicles) and CHAR staff; disturbance images catalogued but not included in the dataset to protect privacy.
  - File structure
    - Dataset folders: Setup1_Site1, Setup1_Site2, Setup1_Site3.
    - Within each site: per-camera folders (e.g., Setup1_Site1_1570) containing sub-folders for each species observed; images stored as .jpg.
  - Additional descriptive and summary data
    - CHAR_Jun_Nov_2020_Camera_Trap_Site_Descriptions.csv: camera location coordinates (WGS84), habitat type, ambient dose rate at camera location (µSv h-1) measured June 2020 (one exception: camera 1559 May 2021), animal trails description, burn degree within 200 m of camera, and lists of vegetative species near sites.
    - CHAR_Jun_Nov_2020_Camera_Trap_Details_And_Image_Summary.csv: deployment start/end times (Eastern European Summer Time), duration (days), total images taken, and related notes; camera serial numbers as displayed on images; folder location for image sets.
    - Overall dataset comprises 61,736 images captured during Setup 1 (June–November 2020).

- Data content and species coverage
  - Table 2 summarizes species observed (mammals, birds, insects), with counts by image rows in the catalogue (note: multiple individuals may appear in a single image).
  - Notable species counts include red deer, Przewalski’s horse, roe deer, wild boar, red fox, and various others; many identifications are noted as unidentifiable due to image quality.
  - Images containing people or vehicles are catalogued but excluded from the dataset to protect privacy; these events are flagged as disturbance.

- Quality control and data limitations
  - All descriptive parameters recorded by a single person; subsequent quality checks by UKCEH and Chornobyl Centre.
  - Some data caveats:
    - Time zone anomalies: one camera (0851) recorded in Eastern European Winter Time in error.
    - Two cameras not functioning or stolen (no images for cameras 1556 and 1541 in certain edges of sites).
    - Some images may not capture all triggering events due to movement speed or timing.
  - Data gaps include lack of images for some cameras and potential misidentifications due to image quality.

- Environmental and contextual variables
  - Ambient dose rate at camera locations in June 2020 (µSv h-1) to contextualize potential radiological influence.
  - Burn degree categories within 200 m of camera location (None to Total destruction), and vegetation descriptions (including broad taxa such as alder, birch, pine, oak, grasses, nettle, and others).
  - Habitat descriptions and trails near camera sites documented to aid interpretation of movement patterns.

- Potential analytic uses for analysts
  - Examine correlations between mammal/bird activity (species counts, triggering event totals) and burn severity, vegetation recovery, or habitat features.
  - Assess spatial patterns of wildlife detections across the contamination gradient and three-site design.
  - Investigate relationships between ambient dose rates and species presence/abundance, controlling for time of day and environmental variables.
  - Evaluate effects of human disturbance (images containing people/vehicles) on wildlife detections.
  - Leverage the detailed metadata and structured CSVs to build predictive models of activity and occupancy under post-fire/radiological contexts.

- Acknowledgements and funding
  - CHAR project funded by the UK Natural Environment Research Council (NERC): NE/V009346/1 and EP/V520846/1.
  - Acknowledgements extended to field collaborators and Chornobyl Centre staff.