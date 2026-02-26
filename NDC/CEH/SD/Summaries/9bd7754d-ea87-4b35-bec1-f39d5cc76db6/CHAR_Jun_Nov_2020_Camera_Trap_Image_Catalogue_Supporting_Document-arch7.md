# CHAR_Jun_Nov_2020_Camera_Trap_Image_Cat alogue_Supporting_Document

- Study context and scope
  - NERC CHAR project studied large mammal activity after the 2020 wildfires within the Ukrainian portion of the Chernobyl Exclusion Zone.
  - Three sites, each ~80 km2 (total ~2600 km2 exclusion zone area affected by fires); June 2020–August 2021 deployment.
  - 13 camera traps per site (total 39 cameras) using Ltl Acorn 6210MC; cameras randomly located at each site with unique camera identifiers and serial numbers.
  - Sites described as: Site 1 northeast (most contaminated), Site 2 western trace (large contamination gradient), Site 3 south (least contaminated).

- Data content and structure
  - Images and metadata collected and compiled into a dataset of 61,736 images (Setup 1: June–November 2020).
  - Images captured day and night via PIR sensor and 940 nm infrared flash; typical 3-image burst per triggering event; 2–4 s recovery between bursts; ~90 s between triggering events.
  - No bait used; camera height ~0.6–0.7 m; most cameras facing north to reduce sun glare; vegetation clearance performed as needed.
  - Poles placed in front of cameras for height/distance estimation (discussed in dataset; removed after calibration).

- Spatial data and geographic references
  - Camera deployment locations include latitude/longitude coordinates in WGS84.
  - Site descriptions and camera information provided with coordinates, habitat descriptions, ambient dose rates, deployment dates, and duration.
  - Ambient dose rate measured at camera locations in June 2020 (µSv h-1) using ATOMEX dosimeters.
  - Data designed for GIS use: spatial joins by Site and Camera_Location_Identifier; coordinates enable mapping of camera locations and site contexts.

- File structure and content details
  - Main data files:
    - CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue.csv
      - Columns include: Site, Camera_Location_Identifier, Setup_Number, Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period, Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Number_Sequential, Young_Animal_In_Image, Notes.
      - Metadata on triggering events, counts per event, and notes. Distinction between images with animals, nothing, people, vehicles, or service-related entries.
      - Disturbance notes for images containing people/vehicles; service entries marked accordingly.
      - Separate rows per species when multiple species appear in a single image.
      - Privacy: images containing people/CHAR team activity excluded from the image set (catalogued but not included).
    - CHAR_Jun_Nov_2020_Camera_Trap_Site_Descriptions.csv
      - Setup_Number, Site, Camera_Location_Identifier, Camera_Location_Latitude_WGS84_Decimal_Degrees, Camera_Location_Longitude_WGS84_Decimal_Degrees, Camera_Location_Description, Ambient_Dose_Rate_At_Camera_Location_Micro_Sievert_Per_Hour_Jun_2020, Description_Of_Animal_Trails_Within_20m_Radius_Of_Camera, Degree_Of_Burn_Of_Area_Affected_By_Fire_Within_200_Metres_Radius_Of_Camera_Location_Jun_2020, Vegetative species list (selected).
    - CHAR_Jun_Nov_2020_Camera_Trap_Details_And_Image_Summary.csv
      - Setup_Number, Site, Camera_Serial_Number_As_Displayed_On_Images, Folder_Name_Where_Images_Are_Located, Start_Date_Time_Camera_Deplyment, End_Date_Time_Camera_Deployment, Number_Of_Days_Camera_Deployed, Number_Of_Images_Taken, Notes.
      - Deployment windows, total days of operation, image counts, and contextual notes.
  - Physical data organization
    - Image folders by site and camera (e.g., Setup1_Site1_1570) with subfolders for each observed species containing image files.
    - Some cameras missing images due to theft (e.g., camera 1556) or not turned on (e.g., 1541).

- Species and imagery data
  - Table 2 (Species observed  June–November 2020): lists mammal, bird, and insect taxa with the number of image rows per species.
    - Notable species: Red deer, Przewalski's horse, Red fox, Roe deer, Red deer (Cervus elaphus), Wild boar, Eurasian elk, Eurasian lynx, among others; many entries are unidentifiable or partially identifiable.
    - Contains both higher-level (e.g., Chiroptera) and species-level identifications; some entries marked as unidentifiable.
  - Table 3 describes image catalogue columns and data interpretation (e.g., triggering events, per-event totals, notes on multiple species, disturbance indicators).
  - Table 4 describes site description columns (deployment summary details, attenuation of burn indicators, and vegetation notes).

- Data quality, limitations, and privacy
  - QA performed by UKCEH and Chornobyl Centre staff; queries resolved with dataset amendments.
  - Privacy: images containing people or CHAR field staff are catalogued but not included in the dataset to protect privacy.
  - Some data gaps: camera 1556 stolen; camera 1541 not switched on; one camera (0851) time zone mis-set (Eastern European Winter Time vs Summer Time).
  - Some images may be challenging to identify to species due to quality; unidentifiable images included in Table 2 as Unidentifiable.

- Usage notes for GIS work
  - Spatial analyses can be performed by linking the image catalogue to site descriptions via Site and Camera_Location_Identifier.
  - Use coordinates for mapping camera placements and habitat context; overlay ambient dose rates for radiation exposure context.
  - Temporal analyses possible using Start_Date_Time_Camera_Deployment and End_Date_Time_Camera_Deployment; consider EE Summer/Winter Time discrepancy for camera 0851.
  - Consider event-based aggregation using Triggering_Event_Number_Sequential and Total_Number_Animals_Per_Triggering_Event for fine-grained activity mapping.
  - Data quality caveats: missing images from some cameras, privacy exclusions, and unidentifiable species entries.

- Acknowledgements and funding
  - CHAR project funded by NERC; collaborating personnel acknowledged; dataset compiled by UKCEH with Chornobyl Centre input.